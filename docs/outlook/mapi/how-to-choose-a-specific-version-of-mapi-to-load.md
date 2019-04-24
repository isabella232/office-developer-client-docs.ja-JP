---
title: 読み込む MAPI の特定のバージョンを選択する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344521"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>読み込む MAPI の特定のバージョンを選択する

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI の実装に明示的にリンクする場合は、読み込む実装を慎重に選択する必要があります。 
  
MAPI の実装に明示的にリンクするには、2つの方法があります。 
  
1. mapi スタブライブラリを読み込み、レジストリにカスタム DLL を指定して、mapi 呼び出しを読み込んでディスパッチすることができます。
    
2. mapi クライアント参照アルゴリズムを実装すると、既定のメールクライアントで使用される mapi のバージョンを検索し、それを読み込むことができます。
    
[Mapi32 スタブのレジストリ設定](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)を変更して、mapi の実装を使用するようにアプリケーションに指示することができるため、テストした mapi の実装を使用するようにアプリケーションを指示することをお勧めします。 次に、両方の方法で明示的にリンクする方法について説明します。 
  
## <a name="reading-from-the-registry"></a>レジストリからの読み取り

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>レジストリから MAPI 実装情報を読み取るには

1. メールクライアントのカスタム DLL を示すレジストリキーは、メールクライアントの`HKLM\Software\Clients\Mail`キーの下にあります。 
    
   次の表で、これらのキーについて説明します。
    
   |**キー**|**説明**|
   |:-----|:-----|
   |MSIComponentID  <br/> |簡易 MAPI または mapi 呼び出しをエクスポートする DLL を識別する Windows Installer publishcomponent カテゴリ ID (GUID)。 設定すると、このキーは**DLLPath**または**dllpathex**キーよりも優先されます。  <br/> |
   |msiapplicationlcid  <br/> |アプリケーションのロケール識別子 (LCID)。 最初の文字列値は、サブキー `HKLM\Software`とそれに続く文字列値を識別し、ロケール情報を含むこのキーの下にあるレジストリ値を識別します。  <br/> |
   |msiofficelcid  <br/> |Microsoft Office の lcid。 最初の文字列値は、このキーの下`HKLM\Software`にあるレジストリ値を識別するために、サブキーとそれに続く文字列値を識別します。  <br/> |
   
   これらのキーから情報を取得します。
    
2. 前の手順で取得した値を[FGetComponentPath](fgetcomponentpath.md)関数に渡します。 **FGetComponentPath**は、MAPI スタブライブラリ Mapistub によってエクスポートされる関数です。 このメソッドは、MAPI のカスタムバージョンのパスを返します。 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>既定として設定されている MAPI の実装を読み込むには

1. レジストリ値`HKLM\Software\Clients\Mail::(default)`を読み取ります。 
    
2. 前述の説明に従って、指定したクライアントの情報を検索します。
    
> [!NOTE]
> 既定のメールクライアントでは、拡張 MAPI が実装されていない場合があることに注意してください。 
  
#### <a name="example"></a>例

Outlook で実装された MAPI を読み込むには、で`HKLM\Software\Clients\Mail\Microsoft Outlook`レジストリキーを検索し、 **FGetComponentPath**に渡します。 **FGetComponentPath**は、Outlook の MAPI の実装のパスを返します。 
  
キー **MSIComponentID**、 **msiapplicationlcid**、および**msiofficeelcid**が設定されていない場合は、 **dllpathex**レジストリ値を確認してください。 キーが設定されている場合、 **FGetComponentPath**はクライアントの MAPI の実装のパスを示します。 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>MAPI クライアント参照アルゴリズムの実装

次の表は、MAPI のカスタム実装のパスを検索するために使用される、mfcmapi の4つの関数を示しています。
  
|**Function**|**説明**|
|:-----|:-----|
| `GetMAPIPath` <br/> |MAPI ライブラリのパスを取得します。  <br/> |
| `GetMailKey` <br/> |MAPI メールのレジストリキーを取得します。  <br/> |
| `GetMapiMsiIds` <br/> |Windows インストーラー識別子を取得します。  <br/> |
| `GetComponentPath` <br/> |[FGetComponentPath](fgetcomponentpath.md)を使用してコンポーネントのパスを取得します。  <br/> |
   
mfcmapi は既定で mapi の既定の実装を読み込むため、mapi の別の実装を使用する場合は、明示的に指定する必要があります。 これは、 **session¥ Load MAPI**ルーチンを使用して実行されます。 
  
### <a name="how-these-functions-work"></a>これらの関数のしくみ

1. mfcmapi は`GetMAPIPath`、クライアントパラメーターに NULL を渡すことで、既定の MAPI 実装を読み込むことができます。
    
2.  `GetMAPIPath`MSIComponentID `GetMapiMsiIds` 、 **msiapplicationlcid**、 **** および**msiofficeelcid**の値を読み取る呼び出し。
    
3.  `GetMapiMsiIds`[ `GetMailKey`呼び出し] 既定のメールクライアントのレジストリキーを開きます。 
    
4.  `GetMapiMsiIds`で返されるレジストリハンドルを`GetMailKey`使用して、 **MSIComponentID**、 **msiapplicationlcid**、および**msiofficeelcid**の値を検索します。
    
5. **MSIComponentID**、 **msiapplicationlcid**、および**msiofficeelcid**の値はに`GetMAPIPath`戻されます。  `GetMAPIPath`を`GetComponentPath`渡します。
    
6.  `GetComponentPath`システムディレクトリから MAPI スタブライブラリ Mapi32 を読み込みます。 
    
7.  `GetComponentPath`その後、Mapi32 が**FGetComponentPath**をエクスポートすると仮定して、Mapi32 から**FGetComponentPath**関数のアドレスを取得します。
    
8. Mapi32 のアドレスを取得**** できない場合は、 `GetComponentPath` Mapistub からアドレスを取得します。 
    
9.  `GetComponentPath`その後、 **FGetComponentPath**を呼び出して、MAPI の既定のバージョンのパスを取得します。
    
10.  `GetMAPIPath`次に、mapi 関数への[リンク](how-to-link-to-mapi-functions.md)に説明されているように、このパスを呼び出し元に返します。その後、mapi と明示的なリンクを読み込みます。
    
> [!NOTE] 
> - 英語および英語以外のロケール用に MAPI のローカライズコピーをサポート`GetMAPIPath`するには、 **msiapplicationlcid**および**msiofficeelcid**サブキーの値を読み取ります。  `GetMAPIPath`その後、 **FGetComponentPath**を呼び出し、最初に**msiapplicationlcid**を**szqualifier**として指定してから、 **msiofficeelcid**を**szqualifier**として指定します。 英語以外の言語をサポートするメールクライアントのレジストリキーの詳細については、「 [Setting Up the MSI keys for the MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)」を参照してください。   
> - mfcmapi が mapi を使用`GetMAPIPath`するためのパスを受信しない場合は、システムディレクトリから mapi スタブライブラリを読み込みます。
> - mapi [dll への mapi 呼び出しの明示的なマッピング](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)で説明されている**MSMapiApps**レジストリ値は、mapi スタブライブラリが使用されている場合にのみ適用されます。 特定の MAPI の実装をロードしたり、既定の実装を読み込んだアプリケーションでは、 **MSMapiApps**レジストリキーを設定する必要はありません。 
    
## <a name="see-also"></a>関連項目

- [FGetComponentPath](fgetcomponentpath.md)
- [MAPI プログラミングの概要](mapi-programming-overview.md)
- [MAPI 関数へのリンク](how-to-link-to-mapi-functions.md)
- [Mapi32 スタブのレジストリ設定](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [MAPI DLL の MSI キーを設定する](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [mapi 呼び出しを mapi dll に明示的にマッピングする](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

