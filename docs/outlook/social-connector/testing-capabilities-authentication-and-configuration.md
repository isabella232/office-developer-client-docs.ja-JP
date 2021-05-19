---
title: 機能、認証、構成のテスト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: このトピックでは、機能を取得するためのテストと、アカウントの構成とソーシャル ネットワークのユーザー認証に関するシナリオについて説明します。
ms.openlocfilehash: 218d5c564dd18e1e72820e31079011e6bb81a33c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423504"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>機能、認証、構成のテスト

このトピックでは、機能を取得するためのテストと、アカウントの構成とソーシャル ネットワークのユーザー認証に関するシナリオについて説明します。
  
## <a name="getting-capabilities"></a>機能の取得

ソーシャル Outlook (OSC) プロバイダーは [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)を実装し、OSC は **GetCapabilities** を呼び出して、プロバイダーがサポートする機能を取得します。 プロバイダーがソーシャル ネットワークに対してサポートする機能は、実装時点で知られている必要があります。また、ソーシャル ネットワークの呼び出しにリアルタイムで依存する必要があります。 たとえば、OutlookユーザーはオフラインOutlook開始できます **。GetCapabilities** は、デバイスの起動時にネットワーク接続Outlookできません。 
  
プロバイダーをテストする場合は **、GetCapabilities** によって返される結果文字列パラメーターが、OSC プロバイダー XML スキーマで定義されている **capabilities** 要素に準拠している必要があります。  詳細については [、「Capabilities XML 要素」を参照してください](capabilities-xml-elements.md)。
  
## <a name="configuring-an-account"></a>アカウントの構成

OSC がアカウントを構成する場合は、ソーシャル ネットワーク のアイコンと名前が表示されるかどうか、およびプロバイダーによって指定されたアカウント構成ダイアログ ボックスに作成アカウントとパスワード忘れパスワードのハイパーリンクが表示されるかどうかを確認する必要があります。
  
### <a name="social-network-icon-and-name"></a>ソーシャル ネットワークのアイコンと名前

機能を取得した後、OSC は [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) と [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md)を呼び出して、ソーシャル ネットワークのアイコンと名前を取得できます。 次のテストを実行して、これらのメソッド呼び出しが成功したことを確認します。
  
|**テストするアイテム**|**予期される動作**|
|:-----|:-----|
|ソーシャル ネットワーク アイコン  <br/> | ソーシャル ネットワーク アイコンは、OSC の次の場所に正しく表示されます。  <br/>  [ソーシャル ネットワーク アカウント] の [OSC] **ダイアログ ボックスで、 をクリックします**。  <br/>  ユーザーを友人として追加しようとすると、ドロップダウン メニューに表示されます。  <br/>  友人に従う場合のバッジ。  <br/> <br/>**メモ**: ソーシャル ネットワーク アカウントのダイアログ ボックスにアクセスするには、Outlook の [表示] タブをクリックし、[ユーザーウィンドウ] グループで [ユーザー ウィンドウ] をクリックし、[アカウント] をクリック **設定。**           |
|ソーシャル ネットワーク名  <br/> | ソーシャル ネットワーク名は、OSC の次の場所に正しく表示されます。  <br/>  [ソーシャル ネットワーク アカウント] の [OSC] **ダイアログ ボックスで、 をクリックします**。  <br/>  ユーザーを友人として追加しようとすると、ドロップダウン メニューに表示されます。  <br/>  既存のパスワードを変更しようとするときに、パスワード ダイアログ ボックスのタイトルとして指定します。  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>構成ダイアログでのハイパーリンクの表示

**ISocialProvider::GetCapabilities** を呼び出した後、OSC は _results_ パラメーターの **hideHyperlinks** 要素の値を使用して、[ここをクリックしてアカウントを作成する] と [パスワードを忘れた場合] ハイパーリンクをアカウント構成ダイアログ ボックスに表示するかどうかを決定します。 **hideHyperlinks が** falseの場合は、アカウント構成にこれらの URL が表示されます。
  
### <a name="support-to-create-account"></a>アカウントを作成するサポート

**ISocialProvider::GetCapabilities** メソッド呼び出しの results パラメーターに **hideHyperlinks** 要素が **false** に設定され **、createAccountUrl** 要素が true に設定されている場合は、URL をクリックすると、既定の Web ブラウザーでページが開きます。  
  
### <a name="support-for-forgotten-password"></a>パスワードを忘れた場合のサポート

**ISocialProvider::GetCapabilities** メソッド呼び出しの results パラメーターに **hideHyperlinks** 要素が **false** に設定され **、forgotPasswordUrl** 要素が true に設定されている場合は、URL をクリックすると、既定の Web ブラウザーでページが開きます。  
  
## <a name="authenticating-users"></a>ユーザーの認証

OSC プロバイダーが基本認証またはフォーム ベース認証をサポートするかどうかに関係なく、次のシナリオをテストします。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|初めてログオンします。  <br/> |ユーザーはソーシャル ネットワークに正常にログオンできます。  <br/> |
|句読点や Unicode 文字など、さまざまな文字で構成されたパスワードでログオンします。  <br/> |ユーザーは、パスワードで使用される文字の種類とは別に、ソーシャル ネットワークに正常にログオンできます。  <br/> |
|ユーザー名または ID **を表示するソーシャル** ネットワーク アカウントのダイアログ ボックス。  <br/> |ユーザーがネットワークに正常にログオンすると、ソーシャル ネットワーク アカウントの OSC のダイアログ ボックスに、ログオンしているユーザー名または ID が表示されます。  <br/> |
|認証は失敗します。  <br/> |OSC は、エラー [無効 **なユーザー名またはパスワード] を表示します**。  <br/> |
|ソーシャル ネットワークに接続できません。  <br/> |OSC は、サーバーが見 **つからないというエラーを表示します**。  <br/> |
|アイテムを取得できる。  <br/> |ユーザーが認証されると、すべてのアクティビティを許可する必要があります。 友人のデータやアクティビティを取得するエラーはありません。  <br/> |
|再起動後にソーシャル ネットワークにログオンOutlook。  <br/> |OSC プロバイダーがパスワードのキャッシュを許可する場合、ユーザーが初めて認証を行った後、OSC がソーシャル ネットワークからデータを取得しようとするたびに、ユーザーに資格情報の入力を求めるメッセージは表示されません。  <br/> |
   
さらに、OSC プロバイダーがフォーム ベース認証をサポートしている場合は、次のシナリオもテストします。
  
|**シナリオ**|**予期される動作**|
|:-----|:-----|
|ユーザーが [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md)を呼び出してログオンするためのフォームへの URL を取得する OSC 。  <br/> |OSC はユーザーの既定のブラウザーで URL を開き、Web ページで資格情報を入力してソーシャル ネットワークにログオンできます。  <br/> |
   
## <a name="see-also"></a>関連項目

- [機能 XML 要素](capabilities-xml-elements.md)  
- [基本認証](basic-authentication.md) 
- [フォーム ベース認証](forms-based-authentication.md)
- [OSC プロバイダーをリリースする準備](getting-ready-to-release-an-osc-provider.md)

