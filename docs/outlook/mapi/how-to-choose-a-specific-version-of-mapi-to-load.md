---
title: 読み込む MAPI の特定のバージョンを選択する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b410d53dee76a7f812f270d5f81f15bc691431ec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580133"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a>読み込む MAPI の特定のバージョンを選択する

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI の実装に明示的にリンクする場合は、読み込む実装を慎重に選択する必要があります。 
  
MAPI の実装に明示的にリンクする 2 つのメソッドがあります。 
  
1. MAPI スタブ ライブラリを読み込み、MAPI 呼び出しを読み込み、ディスパッチするカスタム DLL をレジストリに指定できます。
    
2. MAPI クライアント参照アルゴリズムを実装して、既定のメール クライアントで使用される MAPI のバージョンを検索し、読み込みできます。
    
[Mapi32.dll ス](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)タブ レジストリ 設定 を変更して、アプリケーションに MAPI の実装を使用することを指示することができますので、テストした MAPI の実装を使用するアプリケーションに指示することをお勧めします。 次に、両方のリンク方法を明示的に説明します。 
  
## <a name="reading-from-the-registry"></a>レジストリからの読み取り

### <a name="to-read-mapi-implementation-information-from-the-registry"></a>レジストリから MAPI 実装情報を読み取る方法

1. メール クライアントのカスタム DLL を示すレジストリ キーは、メール クライアントのキー  `HKLM\Software\Clients\Mail` の下に置きます。 
    
   次の表では、これらのキーについて説明します。
    
   |**キー**|**説明**|
   |:-----|:-----|
   |MSIComponentID  <br/> |単純Windows MAPI 呼び出しをエクスポートする DLL を識別する、インストーラー PublishComponent カテゴリ ID (GUID) です。 設定されている場合、このキーは **DLLPath** キーまたは **DLLPathEx キーよりも優先** されます。  <br/> |
   |MSIApplicationLCID  <br/> |アプリケーションのロケール識別子 (LCID)。 最初の文字列値はサブキーを識別し、以降の文字列値は、ロケール情報を含むこのキーの下にあるレジストリ値  `HKLM\Software` を識別します。  <br/> |
   |MSIOfficeLCID  <br/> |LCIDs for Microsoft Office。 最初の文字列値はサブキーを識別し、以降の文字列値は、このキーの下のレジストリ値  `HKLM\Software` を識別します。  <br/> |
   
   これらのキーから情報を取得します。
    
2. 前の手順で取得した値を [FGetComponentPath 関数に渡](fgetcomponentpath.md) します。 **FGetComponentPath** は、MAPI スタブ ライブラリによってエクスポートされる関数Mapistub.dll。 MAPI のカスタム バージョンのパスを返します。 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a>既定としてマークされている MAPI の実装を読み込むには

1. レジストリ値  `HKLM\Software\Clients\Mail::(default)` を読み取る。 
    
2. 前述のように、指定されたクライアントの情報を参照します。
    
> [!NOTE]
> 既定のメール クライアントは拡張 MAPI を実装しない場合があります。 
  
#### <a name="example"></a>例

MAPI を読み込むには、Outlookでレジストリ キーを検索し、 `HKLM\Software\Clients\Mail\Microsoft Outlook` **それらを FGetComponentPath に渡します**。 **FGetComponentPath** は、MAPI のOutlookパスを返します。 
  
キー MSIComponentID、MSIApplicationLCID、および **MSIOfficeLCID** が設定されていない場合は **、DLLPathEx** レジストリ値を確認します。   キーが設定されている場合 **、FGetComponentPath は** クライアントの MAPI 実装のパスを提供します。 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a>MAPI クライアント 参照アルゴリズムの実装

次の表に、MAPI のカスタム実装のパスを検索するために使用される MFCMAPI の 4 つの関数を示します。
  
|**関数**|**説明**|
|:-----|:-----|
| `GetMAPIPath` <br/> |MAPI ライブラリ パスを取得します。  <br/> |
| `GetMailKey` <br/> |MAPI メール レジストリ キーを取得します。  <br/> |
| `GetMapiMsiIds` <br/> |インストーラー識別子Windows取得します。  <br/> |
| `GetComponentPath` <br/> |[FGetComponentPath を使用してコンポーネント パスを取得します](fgetcomponentpath.md)。  <br/> |
   
MFCMAPI は既定で MAPI の既定の実装を読み込むため、MAPI の別の実装を使用する場合は、明示的に指示する必要があります。 これは **、Session\Load MAPI ルーチンを使用して実行** されます。 
  
### <a name="how-these-functions-work"></a>これらの関数の動作

1. MFCMAPI は、既定の MAPI 実装を読み込むには、クライアント パラメーター  `GetMAPIPath` に NULL を渡します。
    
2.  `GetMAPIPath``GetMapiMsiIds` **MSIComponentID、MSIApplicationLCID、****および MSIOfficeLCID** の値を読み取 **る呼び出し**。
    
3.  `GetMapiMsiIds` 既定  `GetMailKey` のメール クライアントのレジストリ キーを開く呼び出し。 
    
4.  `GetMapiMsiIds``GetMailKey` **MSIComponentID、MSIApplicationLCID、および** **MSIOfficeLCID** の値を検索するために返されるレジストリ ハンドルを使用します。 
    
5. MSIComponentID、MSIApplicationLCID、**および MSIOfficeLCID** の値がに返されます `GetMAPIPath` 。  `GetMAPIPath` 次に、それらをに渡します  `GetComponentPath` 。
    
6.  `GetComponentPath` システム ディレクトリから MAPI スタブ ライブラリMapi32.dll読み込まれます。 
    
7.  `GetComponentPath` 次に **、FGetComponentPath** 関数のアドレスを取得Mapi32.dll **FGetComponentPath** をエクスポートMapi32.dll仮定します。
    
8. **FGetComponentPath** のアドレスを取得すると、Mapi32.dllからアドレス `GetComponentPath` を取得Mapistub.dll。 
    
9.  `GetComponentPath` 次に、既定のバージョンの MAPI のパスを取得する **FGetComponentPath** を呼び出します。
    
10.  `GetMAPIPath` 次に、このパスを呼び出し元に返し、MAPI を読み込み、MAPI 関数へのリンクの説明に従って明示的に [リンクします](how-to-link-to-mapi-functions.md)。
    
> [!NOTE] 
> - 英語および英語以外のロケール用に MAPI のローカライズされたコピーをサポートするには  `GetMAPIPath` **、MSIApplicationLCID** サブキーと **MSIOfficeLCID** サブキーの値を読み取ります。  `GetMAPIPath` 次に **、FGetComponentPath** を呼び出し、まず **MSIApplicationLCID** を **szQualifier** として指定し **、MSIOfficeLCID** を **szQualifier** として指定します。 英語以外の言語をサポートするメール クライアントのレジストリ キーの詳細については、「MAPI DLL の MSI キーのセットアップ」 [を参照してください](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)。   
> - MFCMAPI が MAPI のパスを使用して受信しない場合は、システム ディレクトリから MAPI スタブ  `GetMAPIPath` ライブラリが読み込まれます。
> - 「MAPI 呼び出しを [MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) DLL に明示的にマッピングする」で説明されている **MSMapiApps** レジストリ値は、MAPI スタブ ライブラリが使用されている場合にのみ適用されます。 MAPI の特定の実装を読み込むアプリケーション、または既定の実装を読み込むアプリケーションは **、MSMapiApps** レジストリ キーを設定する必要があります。 
    
## <a name="see-also"></a>関連項目

- [FGetComponentPath](fgetcomponentpath.md)
- [MAPI プログラミングの概要](mapi-programming-overview.md)
- [MAPI 関数へのリンク](how-to-link-to-mapi-functions.md)
- [Mapi32.dllスタブ レジストリ 設定](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [MAPI DLL の MSI キーのセットアップ](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [MAPI 呼び出しを MAPI DLL に明示的にマッピングする](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

