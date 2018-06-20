---
title: 機能、認証、および構成のテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: このトピックでは、機能、およびアカウントの構成とソーシャル ネットワークのユーザーの認証のシナリオを取得するためのテストについて説明します。
ms.openlocfilehash: ac294291e2226dbb73f822b2a641fe2bf67ce5eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804464"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>機能、認証、および構成のテスト

このトピックでは、機能、およびアカウントの構成とソーシャル ネットワークのユーザーの認証のシナリオを取得するためのテストについて説明します。
  
## <a name="getting-capabilities"></a>機能を取得します。

Outlook ソーシャル コネクタ (OSC) プロバイダーでは、 [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)、および、OSC **GetCapabilities**を取得する呼び出し、プロバイダーがサポートする機能を実装します。 ソーシャル ネットワーク プロバイダーをサポートしている機能では、実装の時点で認識されている必要があり、リアルタイムでソーシャル ネットワークへの呼び出しに依存する必要があります。 たとえば、Outlook ユーザーがオフラインで Outlook を起動でき、 **GetCapabilities**は、Outlook の起動時にネットワーク接続を利用できません。 
  
プロバイダーをテストするとき、OSC プロバイダーの XML スキーマで定義されている**機能**の要素に**GetCapabilities**によって返される_結果_の文字列パラメーターが準拠しているかを確認してください。 詳細については、[機能の XML 要素](capabilities-xml-elements.md)を参照してください。
  
## <a name="configuring-an-account"></a>アカウントの構成

OSC では、アカウントを構成、ときに名前とソーシャル ネットワークのアイコンを表示するか、および、プロバイダーによって指定されたアカウントの構成] ダイアログ ボックスでアカウントの作成とパスワードを忘れた場合、ハイパーリンクが表示されることを確認してください。
  
### <a name="social-network-icon-and-name"></a>ソーシャル ネットワークのアイコンと名前

機能を取得するには後の OSC は、 [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md)と[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md)を呼び出すことによって、ソーシャル ネットワークの名前とアイコンを取得するのには続行できます。 これらのメソッド呼び出しが成功することを確認するのには次のテストを実行します。
  
|**項目をテストするには**|**予想される動作**|
|:-----|:-----|
|ソーシャル ネットワークのアイコン  <br/> | ソーシャル ネットワークのアイコンは、OSC では、次の場所で正しく表示されます。  <br/>  OSC] ダイアログの [**ソーシャル ネットワーク アカウント**にします。  <br/>  で人を友人として追加しようとするときは、ドロップ ダウン メニューです。  <br/>  友人に従うときのバッジ。  <br/> <br/>**注**: Outlook では、[**表示**] タブの [**人物情報ウィンドウ**のグループをクリックすると、**人物情報ウィンドウ**をクリックし、**アカウントの設定**で**ソーシャル ネットワーク アカウント**のダイアログ ボックスを表示できます。           |
|ソーシャル ネットワーク名  <br/> | ソーシャル ネットワーク名が正しく、OSC では、次の場所に表示されます。  <br/>  OSC] ダイアログの [**ソーシャル ネットワーク アカウント**にします。  <br/>  で人を友人として追加しようとするときは、ドロップ ダウン メニューです。  <br/>  として既存のパスワードを変更しようとしたときに、[パスワード] ダイアログ ボックスのタイトル。  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>構成] ダイアログ ボックス内のハイパーリンクを表示

OSC **ISocialProvider::GetCapabilities**を呼び出した後、**ここをクリックすると、アカウントを作成して****の再設定を表示または非表示にするかどうかを決定する_結果_パラメーター内の**hideHyperlinks**要素の値を使用して、パスワード?** アカウントの構成] ダイアログ ボックス内のハイパーリンク。 **HideHyperlinks**が**false**の場合は、アカウントの設定がこれらの Url を表示することを確認します。
  
### <a name="support-to-create-account"></a>アカウントを作成するためのサポート

**HideHyperlinks**要素を**false**に設定し、 **createAccountUrl**要素を設定する**場合は true**URL をクリックすると、 **ISocialProvider::GetCapabilities**メソッドの呼び出しからの_結果_のパラメーターがある場合のことを確認します。既定の web ブラウザーでページを開きます。
  
### <a name="support-for-forgotten-password"></a>パスワード ディスクの作成のサポート

**HideHyperlinks**要素を**false**に設定し、 **forgotPasswordUrl**要素を設定する**場合は true**URL をクリックすると、 **ISocialProvider::GetCapabilities**メソッドの呼び出しからの_結果_のパラメーターがある場合のことを確認します。既定の web ブラウザーでページを開きます。
  
## <a name="authenticating-users"></a>ユーザーの認証

OSC プロバイダーが基本認証またはフォーム ベース認証をサポートしているかどうかに関係なく次のシナリオをテストします。
  
|**シナリオ**|**予想される動作**|
|:-----|:-----|
|最初にログオンします。  <br/> |ソーシャル ネットワークにログオン成功しています。  <br/> |
|さまざまな記号や Unicode 文字を含む文字のパスワードでログオンします。  <br/> |パスワードで使用される文字の種類に関係なく、ソーシャル ネットワークにログオン成功しています。  <br/> |
|**ソーシャル ネットワーク アカウント**のユーザー名または ID を表示するためのダイアログ ボックス  <br/> |ユーザーがネットワークに正常にログオン、OSC の**ソーシャル ネットワーク**アカウント] ダイアログ ボックスが表示されますユーザーのログオン名または id。  <br/> |
|認証は失敗します。  <br/> |OSC では、**無効なユーザー名またはパスワード**のエラーが表示されます。  <br/> |
|ソーシャル ネットワークに接続できません。  <br/> |OSC では、**サーバーが見つからない**エラーが表示されます。  <br/> |
|アイテムを取得できること。  <br/> |ユーザーが認証されると、すべてのアクティビティを許可する必要があります。 友人のデータやアクティビティを取得中にエラーはありません。  <br/> |
|Outlook を再起動した後、ソーシャル ネットワークへのログオンします。  <br/> |OSC プロバイダーは、ユーザーが最初に認証した後に、パスワードのキャッシュを許可している場合、その後表示されませんの資格情報を OSC ソーシャル ネットワークからデータを取得しようとするたびにします。  <br/> |
   
さらに、OSC プロバイダーでは、フォーム ベース認証をサポートする場合は、次のシナリオにもテストします。
  
|**シナリオ**|**予想される動作**|
|:-----|:-----|
|OSC から[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md)を呼び出すことでログオンするユーザーのフォームへの URL を取得します。  <br/> |OSC は、ユーザーの既定のブラウザーで URL を開くし、web ページには、ソーシャル ネットワークにログオンする資格情報を入力できます。  <br/> |
   
## <a name="see-also"></a>関連項目

- [XML 要素の機能](capabilities-xml-elements.md)  
- [基本認証](basic-authentication.md) 
- [フォーム ベースの認証](forms-based-authentication.md)
- [OSC プロバイダーをリリースする準備をします。](getting-ready-to-release-an-osc-provider.md)

