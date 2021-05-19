---
title: MFCMAPI を使用して Outlook プロファイルを作成する
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI は、MAPI ストアへのアクセスを提供し、ExchangeおよびOutlookの調査を容易にし、MAPI 開発のサポートを開発者に提供します。
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345991"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>MFCMAPI を使用して Outlook プロファイルを作成する

MFCMAPI は、MAPI ストアへのアクセスを提供し、ExchangeおよびOutlookの調査を容易にし、MAPI 開発のサポートを開発者に提供します。

**適用対象**: Office 365 |Outlook |Outlook 2016 
  
開発者以外の場合は、2013 年 2013 年Outlookユーザー インターフェイスを使用してプロファイルExchange勧めします。
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>MFCMAPI をOutlookプロファイルを構成する

1. [MFCMAPI を開](https://mfcmapi.codeplex.com/)き、[プロファイル] メニュー **の**[プロファイルの表示 **] をクリックします**。 
    
2. [操作] **メニューの** [プロファイルの作成] **をクリックします**。 
    
3. プロファイルの新しい名前を作成し **、[OK] をクリックします**。 
    
4. 新しいプロファイルを右クリックし、[サービス] メニューの [サービス **の追加]** **をクリックします**。 
    
5. [サービス UI の表示] ボックスのチェックを外し **、[OK] をクリックします**。 
    
6. 新しく作成したプロファイルをダブルクリックし **、MSEMS サービスをクリック** します。 
    
7. [プロファイル] セクションExchange探します。
    
   これは、2010 以降Outlookグローバル プロファイル セクションが存在しなくなったので、2010 年の MAPI では難しい場合があります。 [プロファイル] セクションを見つけるには、プロパティ を検索PR_EMSMDB_SECTION_UID (0x3D150102)。 値は、後続の手順で使用されるバイナリ形式で保持されるプロファイル セクションの GUID になります。 手順 9 でこの値が必要になります。
    
8. **MSEMS サービスをダブルクリック** します。 
    
9. 手順 7 **Exchange** UID を使用して[プロファイル プロファイル] セクションを検索し、シングル クリックして行を選択します。 
    
10. [プロパティ] メニューの [追加のプロパティ] **をクリックします**。 
    
11. [追加 **] を** クリックし、次のプロパティを追加します。 
    
    **このOutlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` and`PR_DISPLAY_NAME_W`
    
    **次OutlookのOffice 365**、 、 、 `PR_PROFILE_UNRESOLVED_NAME` `PR_PROFILE_UNRESOLVED_SERVER` 、 `PR_ROH_PROXY_SERVER` 、 `PR_ROH_FLAGS` 、 `PR_ROH_PROXY_AUTH_SCHEME` `PR_PROFILE_AUTH_PACKAGE` 、`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **2013 Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME` `PR_PROFILE_UNRESOLVED_SERVER` `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME` 、、、、、、 `PR_PROFILE_AUTH_PACKAGE` 。 
    
12. **[OK]** をクリックし、接続するバージョンに応じて、以下の表に従って各プロパティを構成します。 
    
13. [セッション **] メニューの** [ **ログオン** と表示ストア] をクリックし、プロファイルを選択します (まだ選択されていない場合)。 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Property** <br/> |**Tag** <br/> |**説明** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |ユーザーの SMTP アドレス  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |ユーザーの表示名  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |**EMSMDB** セクションにあるこのプロパティの値を構成し、対応する一致するプロパティの UID を更新します。  <br/> |
   
### <a name="outlook-for-office-365"></a>OutlookのOffice 365
  
||||
|:-----|:-----|:-----|
|**プロパティ** <br/> |**値** <br/> |**説明** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |メールボックスエイリアス  <br/> |ターゲット メールボックスのエイリアス。たとえば、Administrator  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |カスタマイズされたサーバー ID  <br/> |自動検出から取得 **される値** です。 形式 <guid> @tenant.onmicrosoft.com;たとえば、F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *自動検出ノード*  : 応答/アカウント/プロトコル/サーバー (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |outlook.office365.com  <br/> | *自動検出ノード*  : 応答/アカウント/プロトコル/サーバー (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/> ROH_FLAGS_USE_SSL (0x2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0x4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20)  <br/> |Hypertext Transfer Protocol (HTTP) をOutlookリモート プロシージャ 呼び出し (RPC) を使用して Microsoft Exchange Server に接続するために使用されるプロファイルの設定が含まれる。 *自動検出ノード*  : 応答/アカウント/プロトコル/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0x1)  <br/> |このプロファイル自動検出ノードに使用する認証プロトコルを表 *します。応答*  /アカウント/プロトコル/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0x0)  <br/> |*RPC* 自動検出ノードに使用する認証スキームについて説明します。応答/アカウント/プロトコル/AuthPackage (EXCH) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |CertPrincipalName 要素  <br/> |相互認証をサポートするために使用されます。たとえば、msstd:outlook.com *自動検出ノード*  : Response/Account/Protocol/CertPrincipalName (EXPR) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**プロパティ** <br/> |**値** <br/> |**説明** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |メールボックスエイリアス  <br/> |ターゲット メールボックスのエイリアス。たとえば、Administrator  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |カスタマイズされたサーバー ID  <br/> |自動検出から取得 **される値** です。 形式 <guid> @tenant.onmicrosoft.com;たとえば、F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *自動検出ノード*  : 応答/アカウント/プロトコル/サーバー (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | クライアント アクセス サーバーのドメイン名  <br/> | 完全修飾ドメイン名 (FQDN)。たとえば、e2013cas.contoso.com  *検出ノード*  : 応答/アカウント/プロトコル/サーバー (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20))  <br/> |hypertext Transfer Protocol (HTTP) 自動検出ノードでのリモート プロシージャ 呼び出し (RPC) を使用して Microsoft Exchange Server に接続するためにOutlook が使用するプロファイルの設定が含まれている : 応答/アカウント/プロトコル/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0x2)  <br/> |このプロファイル自動検出ノードに使用する認証プロトコルを表 *します。応答*  /アカウント/プロトコル/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0xA)  <br/> |*RPC* 自動検出ノードに使用する認証スキームについて説明します。応答/アカウント/プロトコル/AuthPackage (EXCH) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - 上記のすべてのプロパティ値は、特定の組織によって異なる場合があります。 
> - <sup>1</sup> ANSI バージョンではなく、Unicode バージョンを使用する必要があります。 
> - プレーン 古い XML (POX) ベースの自動検出を使用する必要があります。 これは、プロファイルを構成するための唯一のサポートされている自動検出Outlook/Exchangeです。
> - Outlook を使用して、システム トレイの Outlook アイコンを右クリックし、[Ctrl] を押しながら [電子メールの自動構成のテスト] をクリックすることで、代理で自動検出要求を **行うことができます**。 
> - たとえばPR_ROH_FLAGS環境では、MAPI に SSL のみを使用ROHFLAGS_SSL_ONLY (0x2) というフラグが必要な場合があります。 環境で相互認証が必要な場合は、そのフラグも [ROHFLAGS_MUTUAL_AUTH (0x4)] に設定する必要があります。 プロパティROHFLAGS_MUTUAL_AUTH (0x4) を設定するには、プロパティを設定する必要PR_ROH_PROXY_PRINCIPAL_NAME。 これをサーバーのプリンシパル名に設定する必要があります。
> - <sup>2</sup> 2010 Outlook、EXPR プロトコルを使用する必要があります。 Outlook 2013 は EXHTTP プロトコルを使用します。 
> - <sup>3</sup> この値は自動検出応答に含めない場合があります。 指定しない場合、クライアントは Kerberos または NTLM を使用する必要があります。 
    
トラブルシューティングのヒントについては[、「MFCMAPI を使用して 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013)Outlookプロファイルを構成する方法」をExchangeしてください。
  
## <a name="see-also"></a>関連項目

- [Outlook MAPI リファレンス](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [プログラムを使用してプロファイルを作成Outlook](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

