---
title: 機能、認証、構成のテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: このトピックでは、機能を取得するためのテスト、およびソーシャルネットワークのアカウントの構成とユーザーの認証に関するシナリオについて説明します。
ms.openlocfilehash: 218d5c564dd18e1e72820e31079011e6bb81a33c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423504"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>機能、認証、構成のテスト

このトピックでは、機能を取得するためのテスト、およびソーシャルネットワークのアカウントの構成とユーザーの認証に関するシナリオについて説明します。
  
## <a name="getting-capabilities"></a>機能の取得

Outlook Social Connector (.osc) プロバイダーは[isocialprovider:: getcapabilities](isocialprovider-getcapabilities.md)を実装し、.osc は**getcapabilities**を呼び出して、プロバイダーがサポートする機能を取得します。 ソーシャルネットワークに対してプロバイダーがサポートする機能は、実装時に把握しておく必要があり、リアルタイムでのソーシャルネットワークへの通話に依存しないようにする必要があります。 たとえば、outlook ユーザーは outlook をオフラインで起動することができ、 **getcapabilities**は outlook の起動時にネットワーク接続を利用できません。 
  
プロバイダーをテストするときは、 **getcapabilities**によって返される_結果_文字列パラメーターが、.osc プロバイダ XML スキーマで定義されている**capabilities**要素に準拠していることを確認する必要があります。 詳細については、「[機能 XML 要素](capabilities-xml-elements.md)」を参照してください。
  
## <a name="configuring-an-account"></a>アカウントを構成する

.osc でアカウントを構成する場合は、ソーシャルネットワークのアイコンと名前が表示されているかどうかを確認し、プロバイダーによって指定されているように、[アカウント構成] ダイアログボックスに [アカウントの作成] または [パスワードを忘れた] のハイパーリンクが表示されることを確認する必要があります。
  
### <a name="social-network-icon-and-name"></a>ソーシャルネットワークのアイコンと名前

機能を取得したら、次に、ソーシャルネットワークのアイコンと名前を取得するために、次のようにします。これには[](isocialprovider-socialnetworkname.md)、 [isocialprovider::](isocialprovider-socialnetworkicon.md) "/"/"/"/"という名前を使用します。 次のテストを実行して、これらのメソッドの呼び出しが成功したことを確認します。
  
|**テストするアイテム**|**予期される動作**|
|:-----|:-----|
|ソーシャルネットワークアイコン  <br/> | [ソーシャルネットワーク] アイコンは、.osc の次の場所に正しく表示されます。  <br/>  **ソーシャルネットワークアカウント**の [.osc] ダイアログボックス  <br/>  ユーザーをフレンドとして追加しようとすると、ドロップダウンメニューに表示されます。  <br/>  フレンドのフォロー時のバッジ。  <br/> <br/>**注**:**ソーシャルネットワークアカウント**のダイアログボックスにアクセスするには、Outlook の [**表示**] タブをクリックし、[**ユーザー] ウィンドウ**の [**ユーザー] ウィンドウ**をクリックして、[**アカウント設定**] をクリックします。           |
|ソーシャルネットワーク名  <br/> | ソーシャルネットワーク名は、.osc の次の場所に正しく表示されます。  <br/>  **ソーシャルネットワークアカウント**の [.osc] ダイアログボックス  <br/>  ユーザーをフレンドとして追加しようとすると、ドロップダウンメニューに表示されます。  <br/>  既存のパスワードを変更しようとしたときに、[パスワード] ダイアログボックスのタイトルとして。  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>構成ダイアログでのハイパーリンクの表示

**isocialprovider:: getcapabilities**を呼び出すと、.osc は、 **[ここをクリック**してアカウント__ を作成し、それを忘れる] を非表示にするかどうかを判断します。 **** **パスワード**[アカウントの構成] ダイアログボックス内のハイパーリンク。 **hidehyperlinks**が**false**の場合は、アカウント構成にこれらの url が表示されることを確認します。
  
### <a name="support-to-create-account"></a>アカウントの作成のサポート

**icreateAccountUrl alprovider:: getcapabilities**メソッド呼び出しの_結果_パラメーターに、 **hidehyperlinks**要素が**false**に設定されていて、 **** 要素が**true**に設定されているかどうかを確認し、URL をクリックします。既定の web ブラウザーでページを開きます。
  
### <a name="support-for-forgotten-password"></a>パスワードを忘れた場合のサポート

**iforgotPasswordUrl alprovider:: getcapabilities**メソッド呼び出しの_結果_パラメーターに、 **hidehyperlinks**要素が**false**に設定されていて、 **** 要素が**true**に設定されているかどうかを確認し、URL をクリックします。既定の web ブラウザーでページを開きます。
  
## <a name="authenticating-users"></a>ユーザーの認証

.osc プロバイダーが基本認証またはフォームベース認証をサポートしているかどうかにかかわらず、以下のシナリオをテストします。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|最初にログオンしたとき。  <br/> |ユーザーは、ソーシャルネットワークに正常にログオンできます。  <br/> |
|句読点や Unicode 文字など、さまざまな文字で構成されたパスワードを使用してログオンします。  <br/> |ユーザーは、パスワードで使用されている文字の種類に関係なく、ソーシャルネットワークに正常にログオンできます。  <br/> |
|ユーザー名または ID が表示される**ソーシャルネットワークアカウント**のダイアログボックス。  <br/> |ユーザーがネットワークに正常にログオンした後、**ソーシャルネットワークアカウント**の [.osc] ダイアログボックスに、ログオンしているユーザー名または ID が表示されます。  <br/> |
|認証が失敗します。  <br/> |.osc では、**ユーザー名またはパスワードが無効**であるというエラーが表示されます。  <br/> |
|ソーシャルネットワークに接続できません。  <br/> |.osc にエラーサーバーが**見つからないこと**が表示されます。  <br/> |
|アイテムを取得することができます。  <br/> |ユーザーが認証されたら、すべてのアクティビティを許可する必要があります。 フレンドのデータやアクティビティを取得するときにエラーは発生しません。  <br/> |
|Outlook を再起動した後、ソーシャルネットワークにログオンします。  <br/> |.osc プロバイダーでパスワードのキャッシュが許可されている場合は、ユーザーが初めて認証を行った後、.osc がソーシャルネットワークからデータを取得しようとするたびに資格情報を求めるメッセージが表示されません。  <br/> |
   
また、.osc プロバイダーがフォームベース認証をサポートしている場合は、次のシナリオもテストしてください。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|フォームへの URL を取得するために、ユーザーが[i' getlogonalsession:: getlogonurl](isocialsession-getlogonurl.md)を呼び出したときに、フォームへの URL を取得します。  <br/> |.osc は、ユーザーの既定のブラウザーで URL を開き、web ページを使用して、ソーシャルネットワークにログオンするための資格情報の入力をユーザーに許可します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [機能 XML 要素](capabilities-xml-elements.md)  
- [基本認証](basic-authentication.md) 
- [フォームベース認証](forms-based-authentication.md)
- [.osc プロバイダーをリリースする準備をする](getting-ready-to-release-an-osc-provider.md)

