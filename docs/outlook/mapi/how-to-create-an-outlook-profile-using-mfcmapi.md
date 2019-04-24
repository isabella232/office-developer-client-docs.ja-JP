---
title: MFCMAPI を使用して Outlook プロファイルを作成する
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: mfcmapi は mapi ストアへのアクセスを提供して、Exchange と Outlook の問題を調査し、開発者に mapi 開発のサポートを提供します。
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345991"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>MFCMAPI を使用して Outlook プロファイルを作成する

mfcmapi は mapi ストアへのアクセスを提供して、Exchange と Outlook の問題を調査し、開発者に mapi 開発のサポートを提供します。

**適用**対象: Office 365 |Outlook |Outlook 2016 
  
開発者以外の場合は、Outlook のユーザーインターフェイスを使用して Exchange 2013 のプロファイルを作成することをお勧めします。
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>mfcmapi を使用して Outlook プロファイルを構成する

1. [mfcmapi](https://mfcmapi.codeplex.com/)を開き、[**プロファイル**] メニューの [**プロファイルの表示**] をクリックします。 
    
2. [**操作**] メニューの [**プロファイルの作成**] をクリックします。 
    
3. プロファイルの新しい名前を作成し、[ **OK**] をクリックします。 
    
4. 新しいプロファイルを右クリックし、[**サービス**] メニューの [サービスの**追加**] をクリックします。 
    
5. [サービス UI の表示] チェックボックスをオフにして、[ **OK**] をクリックします。 
    
6. 新しく作成したプロファイルをダブルクリックし、[ **MSEMS** ] サービスをクリックします。 
    
7. [Exchange プロファイル] セクションを探します。
    
   Outlook の MAPI では、2010以降にグローバルプロファイルセクションがなくなったので、これは困難な場合があります。 [プロファイル] セクションを検索するには、プロパティ PR_EMSMDB_SECTION_UID (0x3d150102) を検索します。 この値は、次の手順で使用する、バイナリ形式で保存されたプロファイルセクションの GUID になります。 この値は、手順9で必要になります。
    
8. **MSEMS**サービスをダブルクリックします。 
    
9. 手順7の UID を使用して**Exchange**プロファイルセクションを見つけ、シングルクリックでその行を選択します。 
    
10. [プロパティ] メニューの [**その他のプロパティ**] をクリックします。 
    
11. [**追加**] をクリックし、次のプロパティを追加します。 
    
    **Outlook 2016 の場合**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)`および`PR_DISPLAY_NAME_W`
    
    **Outlook for Office 365 の**場合`PR_PROFILE_UNRESOLVED_NAME`: `PR_PROFILE_UNRESOLVED_SERVER`、 `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME`、、、 `PR_PROFILE_AUTH_PACKAGE`、、、`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **Exchange 2013 の**場合`PR_PROFILE_UNRESOLVED_NAME`: `PR_PROFILE_UNRESOLVED_SERVER`、 `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS`、、 `PR_ROH_PROXY_AUTH_SCHEME`、、 `PR_PROFILE_AUTH_PACKAGE`、。 
    
12. [ **OK**] をクリックし、接続先のバージョンに応じて、以下の表に従って各プロパティを構成します。 
    
13. [**セッション**] メニューで、[**ログオンと表示ストア**] をクリックしてから、プロファイルを選択します (まだ選択されていない場合)。 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Property** <br/> |**Tag** <br/> |**説明** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001f  <br/> |ユーザーの SMTP アドレス  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |ユーザーの表示名  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3d000102  <br/> |**EMSMDB**セクションにあるこのプロパティの値を構成し、一致するプロパティに対応する UID を更新します。  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook for Office 365
  
||||
|:-----|:-----|:-----|
|**プロパティ** <br/> |**値** <br/> |**説明** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |メールボックスのエイリアス  <br/> |ターゲットメールボックスのエイリアス。たとえば、管理者  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |個人用のサーバー id  <br/> |**自動検出**から取得された値。 形式<guid>@tenant onmicrosoft.com。たとえば、F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *自動検出ノード*: Response/Account/Protocol/Server (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |outlook.office365.com  <br/> | *自動検出ノード*: Response/Account/Protocol/Server (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/> ROH_FLAGS_USE_SSL (0x2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0x4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20)  <br/> |ハイパーテキスト転送プロトコル (HTTP) 経由のリモートプロシージャコール (RPC) を使用して Microsoft Exchange Server に接続するために Outlook で使用されるプロファイルの設定が含まれています。 *自動検出ノード*: Response/Account/Protocol/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0x1)  <br/> |このプロファイル*自動検出ノード*に使用される認証プロトコルを表します。 Response/Account/protocol/authpackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0x0)  <br/> |[RPC*自動検出] ノード*で使用する認証方式について説明します。 Response/Account/Protocol/authpackage (EXCH)) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |CertPrincipalName 要素  <br/> |相互認証をサポートするために使用されます。たとえば、msstd: outlook .com*自動検出ノード*: Response/Account/Protocol/CertPrincipalName (EXPR) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**プロパティ** <br/> |**値** <br/> |**説明** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |メールボックスのエイリアス  <br/> |ターゲットメールボックスのエイリアス。たとえば、管理者  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |個人用のサーバー id  <br/> |**自動検出**から取得された値。 形式<guid>@tenant onmicrosoft.com。たとえば、F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *自動検出ノード*: Response/Account/Protocol/Server (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | クライアントアクセスサーバーのドメイン名  <br/> | 完全修飾ドメイン名 (FQDN)。たとえば、e2013cas.contoso.com*自動検出ノード*: Response/Account/Protocol/Server (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20))  <br/> |ハイパーテキスト転送プロトコル (HTTP)*自動検出ノード*経由のリモートプロシージャコール (RPC) を使用して Microsoft Exchange Server に接続するために Outlook で使用されるプロファイルの設定が含まれます。 Response/Account/Protocol/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0x2)  <br/> |このプロファイル*自動検出ノード*に使用される認証プロトコルを表します。 Response/Account/protocol/authpackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0xa)  <br/> |[RPC*自動検出] ノード*で使用する認証方式について説明します。 Response/Account/Protocol/authpackage (EXCH)) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - 前述のすべてのプロパティ値は、特定の組織によって異なる場合があります。 
> - <sup>1</sup> ANSI バージョンではなく、Unicode バージョンを使用する必要があります。 
> - プレーン旧 XML (POX) ベースの自動検出を使用する必要があります。 これは、Outlook/Exchange プロファイルを構成するためにサポートされている自動検出のみです。
> - outlook を使用して、**システムトレイ**の outlook アイコンを右クリックし、CTRL キーを押しながら [**電子メールの構成のテスト**] をクリックすることによって、自動検出要求を行うことができます。 
> - PR_ROH_FLAGS の場合、使用している環境では、SSL のみを使用するように MAPI に通知するフラグ ROHFLAGS_SSL_ONLY (0x2) が必要な場合があります。 環境で相互認証が必要な場合は、そのフラグを設定する必要があります (ROHFLAGS_MUTUAL_AUTH (0x4))。 ROHFLAGS_MUTUAL_AUTH (0x4) を設定すると、プロパティ PR_ROH_PROXY_PRINCIPAL_NAME も設定する必要があります。 これは、サーバーのプリンシパル名に設定する必要があります。
> - <sup>2</sup> Outlook 2010 の場合は、EXPR プロトコルを使用する必要があります。 Outlook 2013 は exhttp プロトコルを使用します。 
> - <sup>3</sup>この値は、自動検出応答に含まれない場合があります。 指定しない場合、クライアントは Kerberos または NTLM を使用する必要があります。 
    
トラブルシューティングのヒントについては、「 [mfcmapi を使用して Exchange 2013 用の Outlook プロファイルを構成する方法](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [Outlook MAPI リファレンス](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Outlook でプログラムによってプロファイルを作成する](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

