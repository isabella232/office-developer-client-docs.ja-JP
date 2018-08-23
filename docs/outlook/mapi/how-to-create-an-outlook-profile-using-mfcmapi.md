---
title: MFCMAPI を使用して Outlook プロファイルを作成する
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI では、Exchange と Outlook の問題の調査を容易にして、MAPI の開発のためのサポートを開発者に提供するのには、MAPI ストアへのアクセスを提供します。
ms.openlocfilehash: 8df9a4c2783829b7f3540046daecb12ce0b6b86a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800225"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>MFCMAPI を使用して Outlook プロファイルを作成する

MFCMAPI では、Exchange と Outlook の問題の調査を容易にして、MAPI の開発のためのサポートを開発者に提供するのには、MAPI ストアへのアクセスを提供します。

**適用されます**: Office 365 |Outlook |Outlook 2016 
  
開発者以外の場合、Outlook のユーザー インターフェイスを使用して、Exchange 2013 のプロファイルを作成することをお勧めします。
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>MFCMAPI を使用して Outlook プロファイルを構成します。

1. [MFCMAPI](https://mfcmapi.codeplex.com/)を開き、[**プロファイル**] メニューの [**プロファイルの表示**] をクリックします。 
    
2. [**アクション**] メニューには、**プロファイルの作成**をクリックします。 
    
3. プロファイルの新しい名前を作成し、[ **OK**] をクリックします。 
    
4. 新しいプロファイルを右クリックし、[**サービス**] メニューの [**サービスの追加**] をクリックします。 
    
5. "サービス UI の表示] ボックスをオフにし、[ **OK**] をクリックします。 
    
6. 新しく作成したプロファイルをダブルクリックし、 **MSEMS**のサービス] をクリックします。 
    
7. Exchange プロファイルのセクションを見つけます。
    
   これは、Outlook で難しいの MAPI では、グローバル プロファイル セクションが不要になった以降で、2010 年のため。 プロファイル セクションを検索するには、プロパティを検索する PR_EMSMDB_SECTION_UID (0x3D150102)。 値は、プロファイル断面の GUID は、以降のステップで使用されるバイナリ形式で永続化されます。 手順 9 では、この値を必要があります。
    
8. **MSEMS**のサービスをダブルクリックします。 
    
9. 手順 7 から UID を使用して**Exchange**プロファイルのセクションを検索し、シングル クリックで行を選択します。 
    
10. [プロパティ] メニューで、**追加のプロパティ**をクリックします。 
    
11. **追加**] をクリックし、次のプロパティを追加します。 
    
    **Outlook 2016 の**:`PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)`と`PR_DISPLAY_NAME_W`
    
    **Outlook を Office 365 の**: `PR_PROFILE_UNRESOLVED_NAME`、 `PR_PROFILE_UNRESOLVED_SERVER`、 `PR_ROH_PROXY_SERVER`、 `PR_ROH_FLAGS`、 `PR_ROH_PROXY_AUTH_SCHEME`、`PR_PROFILE_AUTH_PACKAGE`と`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME`、 `PR_PROFILE_UNRESOLVED_SERVER`、 `PR_ROH_PROXY_SERVER`、 `PR_ROH_FLAGS`、`PR_ROH_PROXY_AUTH_SCHEME`と`PR_PROFILE_AUTH_PACKAGE`。 
    
12. **[Ok]** をクリックしに接続しているバージョンに応じて、次の表に従って、各プロパティを構成します。 
    
13. [**セッション**] メニューで、[**ログオンとストアを表示**、および (それが既に選択されていない場合)、プロファイルを選択します。 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**プロパティ** <br/> |**Tag** <br/> |**説明** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |ユーザーの SMTP アドレス  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |ユーザーの表示名  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |**EMSMDB** ] セクションにある、このプロパティの値を設定して、対応するプロパティに対応する UID を更新  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook を Office 365 の
  
||||
|:-----|:-----|:-----|
|**プロパティ** <br/> |**値** <br/> |**説明** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |メールボックスのエイリアス  <br/> |移動先のメールボックスのエイリアスたとえば、管理者  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |個人用に設定されたサーバー id  <br/> |**自動検出**から取得した値です。 形式の<guid>@tenant.onmicrosoft.com。たとえば、F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *ノードの自動検出*: 応答/アカウント/プロトコル/サーバー (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |outlook.office365.com  <br/> | *ノードの自動検出*: 応答/アカウント/プロトコル/サーバー (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0X1)  <br/> ROH_FLAGS_USE_SSL (0X2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0X4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0X8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0X20)  <br/> |ハイパー テキスト転送プロトコル (HTTP) 経由でリモート プロシージャ コール (RPC) を使用して Microsoft Exchange Server に接続する Outlook で使用するプロファイルの設定が含まれています。 *ノードの自動検出*: 応答/アカウント/プロトコルと SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0X1)  <br/> |このプロファイルの*自動検出] ノード*に使用する認証プロトコルを表します: 応答、アカウント、プロトコルと AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0X0)  <br/> |RPC の*自動検出] ノード*に使用する認証方式を説明します応答、アカウント、プロトコルと AuthPackage (EXCH)) <sup>3</sup> 。 <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |CertPrincipalName 要素  <br/> |相互認証をサポートするために使用msstd:outlook.com*ノードの自動検出*など: 応答、アカウント、プロトコルと CertPrincipalName (EXPR)) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**プロパティ** <br/> |**値** <br/> |**説明** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |メールボックスのエイリアス  <br/> |移動先のメールボックスのエイリアスたとえば、管理者  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |個人用に設定されたサーバー id  <br/> |**自動検出**から取得した値です。 形式の<guid>@tenant.onmicrosoft.com。たとえば、F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *ノードの自動検出*: 応答/アカウント/プロトコル/サーバー (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | クライアント アクセス サーバーのドメイン名  <br/> | 完全修飾ドメイン名 (FQDN) です。e2013cas.contoso.com*ノードの自動検出*など: 応答、アカウント、プロトコルとサーバー (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0X1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0X8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0X20))  <br/> |ハイパー テキスト転送プロトコル (HTTP) の*自動検出のノード*上でリモート プロシージャ コール (RPC) を使用して Microsoft Exchange Server に接続する Outlook で使用するプロファイルの設定が含まれています: 応答、アカウント、プロトコルと SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0X2)  <br/> |このプロファイルの*自動検出] ノード*に使用する認証プロトコルを表します: 応答、アカウント、プロトコルと AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0 XA)  <br/> |RPC の*自動検出] ノード*に使用する認証方式を説明します応答、アカウント、プロトコルと AuthPackage (EXCH)) <sup>3</sup> 。 <br/> |
   
> [!NOTE] 
> - 上で説明したすべてのプロパティ値は、特定の組織の異なる場合があります。 
> - <sup>1</sup> ANSI バージョンではなく、Unicode バージョンを使用する必要があります。 
> - プレーンな古い XML (POX) を使用する必要がありますベースの自動検出します。 これは、Outlook と Exchange プロファイルを構成する唯一のサポートされている自動検出です。
> - Outlook を使用すると、CTRL キーを押しながら**テスト電子メールの自動構成**をクリックするとしているときに**システム トレイ**の Outlook アイコンを右クリックして自分の代わりに、自動検出要求を作成します。 
> - PR_ROH_FLAGS、お客様の環境は、フラグに SSL だけを使用する MAPI ROHFLAGS_SSL_ONLY (0x2) を必要があります。 お客様の環境は、相互認証を必要とする場合は、そのフラグも [ROHFLAGS_MUTUAL_AUTH (0x4)] を設定する必要があります。 設定 (0x4) の ROHFLAGS_MUTUAL_AUTH の PR_ROH_PROXY_PRINCIPAL_NAME プロパティを設定することが必要です。 サーバーのプリンシパル名を設定する必要があります。
> - <sup>2</sup> Outlook 2010 では、する必要が引数 EXPR のプロトコルを使用します。 Outlook 2013 では、EXHTTP プロトコルを使用します。 
> - <sup>3</sup>この値ではありません、自動検出応答します。 指定しない場合、クライアントは kerberos 認証または NTLM を使用してください。 
    
トラブルシューティングのヒントについては、 [Exchange 2013 の MFCMAPI を使用して Outlook プロファイルを構成する方法](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013)を参照してください。
  
## <a name="see-also"></a>関連項目

- [Outlook MAPI リファレンス](https://msdn.microsoft.com/en-us/library/office/cc765775.aspx)  
- [Outlook でプログラムによりプロファイルを作成する](https://msdn.microsoft.com/en-us/library/office/mt707568.aspx)
    

