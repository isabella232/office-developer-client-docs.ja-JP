---
title: ロードするのには MAPI の特定のバージョンを選択します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c5a7ba301d61468c0ff43a7e99d05976d55d239d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576672"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>ロードするのには MAPI の特定のバージョンを選択します。

**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI の実装を明示的にリンクする場合、ロードする実装を慎重に選択する必要があります。 
  
MAPI の実装を明示的にリンクする 2 つの方法もあります。 
  
1. MAPI スタブ ライブラリをロードし、カスタム DLL をロードし、MAPI をディスパッチする呼び出しを行って、レジストリで指定できます。
    
2. 既定のメール クライアントで使用されている MAPI のバージョンを検索するのには、MAPI クライアントの検索アルゴリズムを実装し、それをロードできます。
    
MAPI の実装を使用するようにアプリケーションに指示する[Mapi32.dll スタブのレジストリ設定](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx)を変更することができます、ため、アプリケーションをテストしている MAPI の実装を使用するを指示することをお勧めします。 明示的なリンクの両方の方法を次に示します。 
  
## <a name="reading-from-the-registry"></a>レジストリからの読み取り

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>MAPI 実装に関する情報をレジストリから読み取れません

1. メール クライアントのカスタム DLL を指定するレジストリ キーが下にある、`HKLM\Software\Clients\Mail`メール クライアントのキーです。 
    
   次の表では、これらのキーについて説明します。
    
   |**キー**|**説明**|
   |:-----|:-----|
   |MSIComponentID  <br/> |Windows インストーラー PublishComponent カテゴリ ID (GUID) シンプル MAPI、または MAPI をエクスポートする DLL を識別するを呼び出します。 場合はセットでは、このキーは、 **DLLPath**または**DLLPathEx**キーよりも優先されます。  <br/> |
   |MSIApplicationLCID  <br/> |アプリケーションのロケール識別子 (LCID) です。 最初の文字列から下位のキーを識別する値`HKLM\Software`し、後続の文字列の値がこのキーの下のロケール情報が含まれているレジストリ値を識別します。  <br/> |
   |MSIOfficeLCID  <br/> |Microsoft Office の Lcid です。 最初の文字列から下位のキーを識別する値`HKLM\Software`し、後続の文字列の値がこのキーの下にあるレジストリの値を識別します。  <br/> |
   
   これらのキーから情報を取得します。
    
2. [FGetComponentPath](fgetcomponentpath.md)関数に前の手順から取得した値を渡します。 Mapistub.dll MAPI スタブ ライブラリによってエクスポートされる関数は、 **FGetComponentPath**です。 カスタム MAPI のバージョンのパスを返します。 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>既定としてマークされている MAPI の実装をロードするには

1. 読み取り、`HKLM\Software\Clients\Mail::(default)`のレジストリ値です。 
    
2. 前述したように、指定されたクライアントの情報を検索します。
    
> [!NOTE]
> 既定のメール クライアントが MAPI の拡張を実装可能性があることに注意してください。 
  
#### <a name="example"></a>例

下にレジストリ キーを参照して Outlook に実装された、MAPI を読み込み、 `HKLM\Software\Clients\Mail\Microsoft Outlook` **FGetComponentPath**に渡すとします。 **FGetComponentPath**では、Outlook の MAPI 実装へのパスを返します。 
  
**MSIComponentID**、 **MSIApplicationLCID**、および**MSIOfficeLCID**キーが設定されていない場合は、 **DLLPathEx**レジストリ値を確認してください。 キーが設定されている場合**FGetComponentPath**は、mapi クライアントの実装のパスを示します。 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>MAPI クライアントの検索アルゴリズムを実装します。

MFCMAPI から MAPI のカスタム実装のパスを検索に使用される 4 つの機能を次の表に一覧します。
  
|**関数**|**説明**|
|:-----|:-----|
| `GetMAPIPath` <br/> |MAPI ライブラリのパスを取得します。  <br/> |
| `GetMailKey` <br/> |MAPI メールのレジストリ キーを取得します。  <br/> |
| `GetMapiMsiIds` <br/> |Windows インストーラーの識別子を取得します。  <br/> |
| `GetComponentPath` <br/> |[FGetComponentPath](fgetcomponentpath.md)を使用してコンポーネントのパスを取得します。  <br/> |
   
MFCMAPI では、MAPI の別の実装を使用する場合、既定では、MAPI の既定の実装が読み込まれる、ために割り当てる必要が明示的にそのようにします。 これは、 **MAPI の Session\Load**ルーチンを使用してによって実行されます。 
  
### <a name="how-these-functions-work"></a>これらの関数のしくみ

1. MFCMAPI 呼び出し`GetMAPIPath`、既定の MAPI 実装をロードするのには、クライアント パラメーターの受け渡しが NULL です。
    
2.  `GetMAPIPath`呼び出し`GetMapiMsiIds` **MSIComponentID**、 **MSIApplicationLCID**、および**MSIOfficeLCID**の値を読み取る。
    
3.  `GetMapiMsiIds`呼び出し`GetMailKey`を既定のメール クライアントのレジストリ キーを開きます。 
    
4.  `GetMapiMsiIds`によって返されるレジストリ ハンドルを使用して`GetMailKey` **MSIComponentID**、 **MSIApplicationLCID**、および**MSIOfficeLCID**の値を検索します。
    
5. **MSIComponentID**、 **MSIApplicationLCID**、 **MSIOfficeLCID**の値が返されます`GetMAPIPath`。  `GetMAPIPath`渡されたに`GetComponentPath`。
    
6.  `GetComponentPath`システム ディレクトリから、Mapi32.dll、MAPI スタブ ライブラリを読み込みます。 
    
7.  `GetComponentPath`Mapi32.dll、Mapi32.dll が**FGetComponentPath**をエクスポートすると仮定してから、 **FGetComponentPath**関数のアドレスを取得します。
    
8. Mapi32.dll が失敗した場合から**FGetComponentPath**のアドレスを取得する場合`GetComponentPath`Mapistub.dll からアドレスを取得します。 
    
9.  `GetComponentPath`**FGetComponentPath**MAPI の既定のバージョンのパスを取得するを呼び出します。
    
10.  `GetMAPIPath`呼び出し元、MAPI をロードし、明示的にリンクしている[MAPI の関数へのリンク](how-to-link-to-mapi-functions.md)で説明したようにこのパスを返します。
    
> [!NOTE] 
> - 英語と英語以外のロケールのローカライズされたコピー MAPI をサポートするために`GetMAPIPath` **MSIApplicationLCID**と**MSIOfficeLCID**のサブキーの値を読み取ります。  `GetMAPIPath`**FGetComponentPath**を最初として、 **szQualifier**、 **MSIApplicationLCID**を指定して、再び**szQualifier**として**MSIOfficeLCID**を指定するを呼び出します。 英語以外の言語をサポートするメール クライアントのレジストリ キーの詳細については、[設定の [MSI のキーの MAPI DLL](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx)を参照してください。   
> - MFCMAPI が MAPI を使用するためのパスを受信していないかどうか`GetMAPIPath`、システム ディレクトリから MAPI スタブ ライブラリが読み込まれます。
> - [MAPI 呼び出しを明示的に MAPI Dll へのマッピング](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx)で説明されている**MSMapiApps**レジストリ値は、MAPI スタブ ライブラリを使用する場合にのみ適用されます。 MAPI の特定の実装をロードまたは既定の実装をロードするアプリケーションは、 **MSMapiApps**レジストリ キーを設定する必要はありません。 
    
## <a name="see-also"></a>関連項目

- [FGetComponentPath](fgetcomponentpath.md)
- [MAPI �v���O���~���O�̊T�v](mapi-programming-overview.md)
- [MAPI 機能へのリンク](how-to-link-to-mapi-functions.md)
- [Mapi32.dll スタブのレジストリ設定](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx)
- [MAPI DLL の MSI のキーの設定](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx)
- [MAPI MAPI Dll への呼び出しを明示的にマッピング](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx)

