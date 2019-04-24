---
title: 機能 XML の要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: このトピックの表では、機能 XML の子要素について説明し、それらがサポートする領域によってグループ化されています。
ms.openlocfilehash: 6816bbdcd24eceffc47d6b9d0835a90c7089c039
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281194"
---
# <a name="capabilities-xml-elements"></a>機能 XML の要素

このトピックの表では、**機能**XML の子要素について説明し、それらがサポートする領域によってグループ化されています。 各**capabilities**要素の既定値は**false**です。 [imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドによって返される**機能**XML で要素が指定されていない場合、要素の値は**false**となります。
  
**機能**xml の概要の説明については、「 [xml for capabilities](xml-for-capabilities.md)」を参照してください。 **機能**xml の例については、「 [capabilities xml の例](capabilities-xml-example.md)」を参照してください。 Microsoft outlook social connector (.osc) プロバイダ xml スキーマの完全な定義 (必須または任意の要素を含む) については、「 [Outlook social connector プロバイダーの xml スキーマ](outlook-social-connector-provider-xml-schema.md)」を参照してください。
  
## <a name="capabilities-for-supporting-friends"></a>友人をサポートする機能

次の表は、友人または友人以外の任意の形式の同期に適用される要素を示しています。
  
|**要素**|**説明**|
|:-----|:-----|
|**ユーザー** <br/> |プロバイダーが[iruncommand alsession::](isocialsession-unfollowperson.md)メソッド呼び出しをサポートしているかどうかを示します。  <br/> **** この**ユーザー**は、.osc プロバイダーの独立した機能です。 .osc プロバイダーは、ユーザーを友人として追加 (ユーザーには、[**はい**] **** に設定) したり、ソーシャルネットワークアカウントでユーザーを友人として削除したり (「」 **** を**true**に設定) したりできる機能を示します。 一般に、フォローできることは、フォローを停止することを意味しません。 **** [参照] は機能であり、ソーシャルネットワークアカウント上の特定のユーザーまたはすべてのユーザーをフォローするアクションとして誤解されることはありません。 **** **true の場合**は、値が**** **false**であるとは限りません。  <br/> |
|**ユーザー** <br/> |プロバイダーが i/メソッド呼び出し[](isocialsession-followperson.md)をサポートするかどうかを示します。 .osc は、 **** **cacheFriends**が**true**の場合 (キャッシュされたフレンドの同期)、 **dynamicContactsLookup**は**true** (友人と非友人のオンデマンド同期)、または両方 cacheFriends のいずれかをチェックします。 **** **dynamicContactsLookup**は true (友人と非友人のハイブリッド同期) です。 プロバイダーが [ **true**] に設定されている場合は、ユーザーがフォローしているユーザーの [ **** ** \<\> **ユーザー] ウィンドウにネットワークバッジが表示され、people の [**追加] (+)** メニューの [networkname] コマンドが有効になります。ペイン. プロバイダーが [ **true**] に設定した場合、ネットワークバッジは表示されず **、 \<[networkname\> ** ] コマンドは表示されません。 ****  <br/> |
|**getfriends** <br/> |プロバイダーが[iGetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)または[ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)メソッド呼び出しをサポートするかどうかを示します。 プロバイダーが**getfriends**を**true**として設定した場合、.osc は**cacheFriends**または**dynamicContactsLookup**の値を使用して、ソーシャルネットワークが友人を Outlook の連絡先アイテムまたはメモリに保存できるかどうかを判断します。 プロバイダーが**getfriends**を**false**として設定した場合、ソーシャルネットワークはフレンドおよび**iGetFriendsAndColleagues**および**ISocialSession2:: GetPeopleDetails**メソッドをサポートしていません。また、.osc では、次の値は無視されます。**cacheFriends**および**dynamicContactsLookup**。  <br/> |
   
以下の要素は、フレンドのキャッシュ同期、または友人と非友人のハイブリッド同期にのみ適用されます。 フレンドの同期の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。
  
|**要素**|**説明**|
|:-----|:-----|
|**cacheFriends** <br/> |.osc プロバイダーが Outlook の連絡先アイテムとして友人を保存することを許可するかどうかを示します。 .osc は、 **getfriends**が**true**の場合にのみ**cacheFriends**をチェックします。 プロバイダーが**cacheFriends**を**true**に設定した場合、.osc はキャッシュによって友人を同期し、ユーザーの既定のストアに、フレンド連絡先用のネットワーク固有の連絡先フォルダーを作成します。 ネットワーク固有の連絡先フォルダーの名前は、 [i指定 alprovider::](isocialprovider-socialnetworkname.md) /"/" という値です。 プロバイダーが**cacheFriends**を**false**として設定した場合、.osc は友人の連絡先を格納するためのネットワーク固有の連絡先フォルダーを作成しません。  <br/> |
|**contactsyncrestartinterval** <br/> |同期エラーが発生した場合に、ソーシャルネットワークからのフレンド情報の同期試行の間隔を分単位で指定します。 .osc は、この要素を使用します。この要素は、.osc プロバイダーがソーシャルネットワーク固有の連絡先フォルダーへのフレンドのキャッシュ同期またはハイブリッド同期をサポートしている場合にのみ使用されます (**cacheFriends**が**true**)。  <br/> 既定の再試行間隔は30分です。既定値は、の下`ContactSyncRestartInterval` `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`にあるキーによって上書きされています。 プロバイダーが**contactsyncrestartinterval**を設定すると、プロバイダーの値は既定の再試行間隔である30分またはレジストリキーの値より優先されます。  <br/> 友人および友人以外の情報を需要に同期する方法の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。  <br/> |
   
次の要素は、オンデマンド同期または友人および非友人のハイブリッド同期にのみ適用されます。
  
|**要素**|**説明**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |.osc プロバイダーが友人および非友人のオンデマンド同期の[ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)呼び出しをサポートしているかどうかを示します。  <br/> .osc は、 **getfriends**が**true**の場合にのみ**dynamicContactsLookup**をチェックします。**dynamicContactsLookup**の既定の設定は**false**です。  <br/> .osc プロバイダーが**dynamicContactsLookup**を**true**と指定し、 **getfriends**が**true**の場合、[ユーザー] ウィンドウが更新されるたびに、.osc が**ISocialSession2:: GetPeopleDetails**を呼び出します。 ユーザーが別のユーザーを [ユーザー] ウィンドウまたは outlook エクスプローラーウィンドウの他のアイテムで選択するか、outlook インスペクターウィンドウが開くと、[人] ウィンドウが更新されます。 動的連絡先検索では、ユーザーが最新のユーザー画像とプロファイル情報を [ユーザー] ウィンドウに常に表示することができますが、プロバイダーからソーシャルネットワークへの呼び出し回数が増加します。  <br/> プロバイダーが**dynamicContactsLookup**を**false**として設定した場合、.osc は**ISocialSession2:: GetPeopleDetails**を呼び出してユーザーウィンドウを更新しません。  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |ユーザーウィンドウが最小化されている場合に、.osc が友人および非友人に対してオンデマンド同期を実行する必要があるかどうかを示します。  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>サポートアクティビティの機能

次の要素は、.osc プロバイダーによってサポートされるアクティビティのあらゆる形式の同期に適用されます。
  
|**要素**|**説明**|
|:-----|:-----|
|**getactivities** <br/> |プロバイダーが[ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)または[i alperson:: getactivities](isocialperson-getactivities.md)メソッドの呼び出しをサポートしているかどうかを示します。 プロバイダーが**getactivities**を**true**に設定した場合、.osc は**cacheactivities**または**** の値を使用して、ソーシャルネットワークサイトがアクティビティを Outlook RSS アイテムとして保存できるかどうか、またはメモリ内のアクティビティ。 プロバイダーが**getactivities**を**false**に設定した場合、ソーシャルネットワークはアクティビティと**ISocialSession2:: GetActivitiesEx**および**i alperson:: getactivities**メソッドをサポートしておらず、.osc は次の**値を無視します。cacheactivities**と**dynamicActivitiesLookupEx**。  <br/> |
   
次の要素は、アクティビティのキャッシュ同期またはハイブリッド同期にのみ適用されます。
  
|**要素**|**説明**|
|:-----|:-----|
|**cacheactivities** <br/> |Outlook Social Connector 2013 以降では、プロバイダーがユーザーのストアの隠しフォルダーにキャッシュすることによってアクティビティを同期できなくなるため、.osc はこの要素を無視します。  <br/> プロバイダーがアクティビティをサポートする場合、プロバイダーはオンデマンドでの同期アクティビティをサポートする必要があります。 プロバイダーは**cacheactivities**を**false**に設定し、 **dynamicActivitesLookupEx**を**true**に設定します。 .osc は、必要に応じてアクティビティを同期させ、アクティビティをメモリ内にキャッシュします。 アクティビティのメモリキャッシュは、30分間隔で更新されます。  <br/> |
   
以下の要素は、アクティビティのオンデマンド同期またはハイブリッド同期にのみ適用されます。
  
|**要素**|**説明**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |.osc 1.1 では廃止されました。  <br/> .osc 1.1 以降、.osc は[idynamicActivitiesLookup alsession:: getactivities](isocialsession-getactivities.md)を呼び出すことなく、 **** の値を無視します。 オンデマンドアクティビティ検索をサポートするには、 **cacheactivities**を**false**および**getactivities**と**dynamicActivitiesLookupEx**と**** して設定し、.osc は**ISocialSession2:: GetActivitiesEx**を呼び出します。  <br/> |
|**dynamicActivitiesLookupEx** <br/> |アクティビティのオンデマンド同期に対して、.osc プロバイダーが**ISocialSession2:: GetActivitiesEx**呼び出しをサポートしているかどうかを示します。  <br/> .osc プロバイダーがオンデマンドアクティビティの同期をサポートしている場合は、 **getactivities**と**dynamicActivitiesLookupEx**を**true**に設定し、 **cacheactivities**を**false**とします。 .osc は、[人] ウィンドウが更新されるたびに、 **ISocialSession2:: GetActivitiesEx**を呼び出します。 ユーザーが outlook エクスプローラーウィンドウで選択された項目を変更するか、outlook インスペクターウィンドウを開くと、[ユーザー] ウィンドウが更新されます。 動的アクティビティ検索を実行すると、ユーザーは常に最新のアクティビティを [ユーザー] ウィンドウに表示しますが、プロバイダーからソーシャルネットワークへの呼び出しの数は増加します。  <br/> プロバイダーが**dynamicActivitiesLookupEx**を**false**として設定した場合、.osc は**ISocialSession2:: GetActivitiesEx**を呼び出しません。 [人] ウィンドウに表示されている人の場合。  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |People ペインが最小化されている場合に、アクティビティのオンデマンド同期を実行する必要があるかどうかを示します。  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>友人、非友人、および活動のオンデマンドまたはハイブリッド同期をサポートするための一般的な機能

|**要素**|**説明**|
|:-----|:-----|
|**hashfunction** <br/> | .osc プロバイダーがサポートするハッシュ関数を指定します。 プロバイダーのソーシャルネットワークまたは基幹業務アプリケーションに含まれていないユーザーの個人を特定できる情報を保護するために、.osc はハッシュされた電子メールアドレスを**ISocialSession2:: GetPeopleDetails**と**ISocialSession2:: に渡します。GetActivitiesEx**。  <br/>  **dynamicContactsLookup**が**true**に設定されている場合、または**dynamicActivitiesLookupEx**が**true**に設定されている場合、プロバイダーはハッシュ**関数**を**SHA1**、 **MD5**、または**CRC32MD5**のいずれかに設定する必要があります。 **hashfunction**が見つからない場合、または正しくない値が指定された場合、.osc はエラーを返します。  <br/> **SHA1**は、 [[RFC3174]](https://www.rfc-editor.org/rfc/rfc3174.txt)によって定義された、インターネット技術標準化委員会 (IETF) のセキュアハッシュアルゴリズム1です。 たとえば、電子メールアドレス melissa@contoso.com の**SHA1**ハッシュ値は`bb81577b567262a21a4df5f6e335c1250acd7b50`です。  <br/> **md5**は、 [[RFC1321]](https://www.rfc-editor.org/rfc/rfc1321.txt)で定義されているインターネット技術標準化委員会 (IETF) MD5 メッセージダイジェストアルゴリズムです。 たとえば、電子メールアドレス melissa@contoso.com の**MD5**ハッシュ値は`c8c39e61ca1662477b39b83d7b0a0615`になります。  <br/> **CRC32MD5**は、次のように定義された**CRC32**と**MD5**の組み合わせです。  <br/>  先頭および末尾の空白を削除し、すべての文字を小文字に変換して、電子メールアドレスを正規化します。  <br/>  正規化された電子メールアドレスの**CRC32**値を計算し、この値の10進整数表現を使用します。 実装が符号付き整数を返す場合は、符号付き整数を符号なし整数に変換する必要があります。  <br/>  正規化された電子メールアドレスの**MD5**値を計算し、この値の16進表現を使用します (小文字の A ~ F)。  <br/>  これらの2つの値をアンダースコアで結合します。  <br/>  たとえば、電子メールアドレス melissa@contoso.com の**CRC32MD5**ハッシュ値は`2149665315_c8c39e61ca1662477b39b83d7b0a0615`です。  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>認証とアカウントの構成をサポートする機能

|**要素**|**説明**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |ユーザーがソーシャルネットワークで自動構成設定を変更できるようにするかどうかを指定します。これには、ログオンに別の URL を指定するなどがあります。  <br/> |
|**createAccountUrl** <br/> |プロバイダーが**hidehyperlinks**を**false**に設定した場合、ユーザーが [**アカウント構成**] ダイアログボックスで **[アカウントを作成するには、ここをクリック**します] をクリックすると、 **createAccountUrl**で指定されている URL が既定のブラウザーで開きます。  <br/> |
|**displayurl** <br/> |.osc で、[アカウントの構成] ダイアログボックスにソーシャルネットワークの**URL アドレス**テキストボックスを表示するかどうかを示します。  <br/> |
|**forgotPasswordUrl** <br/> |プロバイダーが**hidehyperlinks**を**false**として設定した場合、ユーザーが [ **** **パスワードの確認**] をクリックすると、既定のブラウザーで**forgotPasswordUrl**で指定された URL が開きます。  <br/> |
|**hidehyperlinks** <br/> |[アカウントの構成] ダイアログボックスで、 **[アカウントの作成**と**パスワードの忘れる**] を非表示にするかどうかを指定します。  <br/> .osc 1.0 は、この設定を無視し、ハイパーリンクは常に非表示になります。 .osc 1.1 は、この設定の値を監視します。  <br/> |
|**hideRememberMyPassword** <br/> |[アカウントの構成] ダイアログボックスで、 **[パスワードを記憶**する] チェックボックスをオフにするかどうかを指定します。  <br/> プロバイダーが**hideRememberMyPassword**を**true**に設定すると、 **[パスワードを記憶**する] チェックボックスをオフにし、パスワードを保存しない場合に、.osc が機能します。  <br/> プロバイダーが**hideRememberMyPassword**を**false**に設定すると、[アカウントの構成] ダイアログボックスに [**パスワードを記憶**する] チェックボックスが表示されます。  <br/> |
|**supportsAutoConfigure** <br/> |ユーザーの自動構成を試行し、ソーシャルネットワークにログオンするために、.osc が**iGetAutoConfiguredSession alprovider**インターフェイス上で**** 関数を呼び出す必要があるかどうかを示します。  <br/> |
|**uselogoncached** <br/> |.osc プロバイダーが、キャッシュされた資格情報を使用してログオンするために[ISocialSession2:: logoncached](isocialsession2-logoncached.md)呼び出しをサポートしているかどうかを示します。  <br/> プロバイダーが**uselogoncached**が**true**として設定されている場合、.osc は**uselogonwebauth**および .osc 呼び出しの設定を無視します**ISocialSession2:: logoncached** for authentication。  <br/> プロバイダーが**dynamicActivitiesLookupEx**を**false**に設定した場合、.osc は認証のために**ISocialSession2:: logoncached**を呼び出しません。  <br/> |
|**uselogonwebauth** <br/> |.osc でフォームベース認証を使用する必要があるか[](isocialsession-logonweb.md)どうかを示します。 プロバイダーが**uselogonwebauth**を**false**として設定している場合、.osc は基本認証を使用して、 [iime alsession:: Logon](isocialsession-logon.md)メソッドを呼び出します。 プロバイダーが**uselogonwebauth**を**true**として設定すると、フォームベース認証を使用して、次のように**isocialsession:: logonweb**を呼び出します。  <br/> |
   
**imethod alprovider:: getcapabilities**メソッドでプロバイダーによって返される**機能**の XML に応じて、[アカウントの構成] ダイアログボックスが変更されます。 たとえば、図1は、testprovider の例の [アカウントの構成] ダイアログボックスを示しています。 
  
**図1。[アカウントの構成] ダイアログボックスの testprovider の例**

![TestProvider の構成情報の例](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)

