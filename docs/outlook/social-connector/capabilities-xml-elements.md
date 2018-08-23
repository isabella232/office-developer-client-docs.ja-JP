---
title: 機能 XML の要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: このトピックの表は、機能の XML 子要素を説明しをサポートしている領域ごとにグループ化します。
ms.openlocfilehash: 53bce69bbe22f6e950302a92b0ada21ed0f5a1f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804328"
---
# <a name="capabilities-xml-elements"></a>機能 XML の要素

このトピックの表は、**機能**XML の子要素を説明しをサポートしている領域ごとにグループ化します。 **機能**の各要素の既定値は、 **false を指定**します。 **機能**、 [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドによって返される XML 要素を指定しない場合は、要素の値は**false**です。
  
XML の**機能**の概要説明、[機能のための XML](xml-for-capabilities.md)を参照してください。 XML の**機能**の使用例は、[機能の XML の例](capabilities-xml-example.md)を参照してください。 のどの要素には、必須またはオプションを含む、Microsoft Outlook ・ ソーシャル コネクタ (OSC) プロバイダーの XML スキーマの完全な定義は、 [Outlook ソーシャル コネクタ プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)を参照してください。
  
## <a name="capabilities-for-supporting-friends"></a>友人をサポートするための機能

次の表は、同期の友人の友人以外の任意のフォームに適用する要素を示しています。
  
|**要素**|**説明**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |[ISocialSession::UnFollowPerson](isocialsession-unfollowperson.md)メソッドの呼び出しをプロバイダーがサポートしているかどうかを示します。  <br/> **followPerson**と**doNotFollowPerson**は、OSC プロバイダーのそれぞれ独立した機能です。 OSC プロバイダーは、(設定**followPerson**を**true**に) 友達とユーザーを追加することや、ソーシャル ネットワーク アカウント (設定**doNotFollowPerson**を**true**に) に友人としてユーザーを削除することの機能を示すことができます。 一般に、理解することがわけのフォローを停止することです。 **followPerson**は、機能、および、ソーシャル ネットワーク アカウントの特定のユーザーまたはすべての人は、次の動作として解釈されるものとでは。 **followPerson**が**true**では、 **doNotFollowPerson**が**false の場合**は意味しません。  <br/> |
|**followPerson** <br/> |[ISocialSession::FollowPerson](isocialsession-followperson.md)メソッドの呼び出しをプロバイダーがサポートしているかどうかを示します。 OSC では、 **cacheFriends**がの場合**は true** (友人のキャッシュの同期) **followPerson**がチェックされ、 **dynamicContactsLookup**が**true** (オン ・ デマンドの友人と友人ではない)、同期または両方の**cacheFriends** **dynamicContactsLookup**が true の場合 (ハイブリッドの同期の友人と友人ではない)。 プロバイダーでは、 **true**として**followPerson**を設定、する場合、OSC バッジが表示されますネットワーク人物情報ウィンドウで、ユーザーがフォローして可能にする方のため、**の\<チーム\>** 人の**追加 (+)** メニューのコマンドウィンドウです。 ネットワークのバッジが表示されていない場合は、プロバイダーでは、 **followPerson**が**false**に設定と**の\<ネットワーク名リソース\>** コマンドが非表示にします。  <br/> |
|**getFriends** <br/> |プロバイダーが[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)または[ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)メソッドの呼び出しをサポートしているかどうかを示します。 プロバイダーでは、 **true**として**getFriends**を設定、OSC はソーシャル ネットワークの友人を保存する Outlook 連絡先アイテム、およびメモリができるかどうかを判断するのには**cacheFriends**または**dynamicContactsLookup**の値を使用します。 ソーシャル ネットワークは友人と**ISocialPerson::GetFriendsAndColleagues**および**ISocialSession2::GetPeopleDetails**のメソッドをサポートしていませんし、OSC の値を無視する場合は、プロバイダーでは、 **getFriends**が**false**に設定、**cacheFriends**と**dynamicContactsLookup**。  <br/> |
   
次の要素は、友人のキャッシュの同期や友人と友人ではないのハイブリッド同期にのみ適用されます。 友人の同期の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。
  
|**要素**|**説明**|
|:-----|:-----|
|**cacheFriends** <br/> |OSC プロバイダーによって、Outlook 連絡先アイテムとして友人を保存することができるかどうかを示します。 OSC は、 **getFriends**が**true**の場合にのみ、 **cacheFriends**をチェックします。 プロバイダーでは、 **true**として**cacheFriends**を設定、OSC は友人をキャッシュするには、同期し、友人の連絡先のユーザーの既定のストアに特定のネットワークの連絡先フォルダーを作成します。 特定のネットワークの連絡先フォルダーの名前は、 [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md)プロパティの値です。 プロバイダーでは、 **cacheFriends**が**false**に設定、OSC では、友人を保存するのには友人の連絡先の特定のネットワークの連絡先フォルダーは作成されません。  <br/> |
|**contactSyncRestartInterval** <br/> |同期エラーが発生した場合は、ソーシャル ネットワークからの友人の情報を同期する間隔を分単位では、再試行の間隔を決定します。 OSC プロバイダーは、キャッシュの同期をサポートしているか、友人をソーシャル ネットワークに固有のハイブリッド同期連絡先フォルダーである場合にのみ、OSC がこの要素に使用 (されます**cacheFriends**が**true**になる)。  <br/> によって既定値がオーバーライドされない限り、既定の再試行間隔は、30 分、`ContactSyncRestartInterval`の下にキー `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`。 プロバイダーは、 **contactSyncRestartInterval**を設定、プロバイダーの値は 30 分間またはレジストリ キーの値の既定の再試行間隔が上書きされます。  <br/> 友人と友人ではない情報を必要に応じて同期についての詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。  <br/> |
   
次の要素は、オンデマンド同期または以外の友人や友人のハイブリッド同期のみに適用されます。
  
|**要素**|**説明**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |OSC プロバイダーがオンデマンドの同期の友人と友人ではないの[ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)の呼び出しをサポートするかどうかを示します。  <br/> OSC は、 **getFriends**が**true**の場合にのみ、 **dynamicContactsLookup**をチェックします。**DynamicContactsLookup**の既定の設定は、 **false を指定**します。  <br/> OSC プロバイダーでは、 **true**と**true**として**getFriends**として**dynamicContactsLookup**を指定した場合、人物情報ウィンドウが更新されるたびに、OSC は**ISocialSession2::GetPeopleDetails**を呼び出します。 人物情報ウィンドウが更新されるは、人物情報ウィンドウ、または Outlook エクスプ ローラー ウィンドウで別のアイテムに別のユーザーを選択するか、Outlook のインスペクター ウィンドウを開きます。 動的なメンバー参照では、ユーザーが常にユーザーの最新の画像と、人物情報ウィンドウにプロファイル情報が表示が、ソーシャル ネットワーク プロバイダーからの呼び出しの数が増加ことを保証します。  <br/> プロバイダーでは、 **dynamicContactsLookup**が**false**に設定、OSC 人物情報ウィンドウを更新するのには**ISocialSession2::GetPeopleDetails**が呼び出されません。  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |OSC 人物情報ウィンドウが最小化したとき以外の友人や友人たちは、オンデマンド同期を実行する必要があることを示します。  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>活動をサポートするための機能

OSC プロバイダーでサポートされているアクティビティの同期の任意のフォームに、次の要素が適用されます。
  
|**要素**|**説明**|
|:-----|:-----|
|**getActivities** <br/> |プロバイダーが[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)または[ISocialPerson::GetActivities](isocialperson-getactivities.md)メソッドの呼び出しをサポートしているかどうかを示します。 ソーシャル ネットワーク サイトでは、アクティビティを格納する Outlook の RSS アイテムとしてできるかどうかを判断するのには、OSC が**cacheActivities**または**dynamicActivitiesLookupEx**の値を使用して設定した場合、プロバイダー **getActivities** **は**、メモリ内のアクティビティです。 **False**として**getActivities**を設定するプロバイダーに、ソーシャル ネットワークが活動し、 **ISocialSession2::GetActivitiesEx**と**ISocialPerson::GetActivities**メソッドの場合をサポートしていません、OSC が**の値を無視cacheActivities**と**dynamicActivitiesLookupEx**。  <br/> |
   
次の要素は、キャッシュの同期または活動のハイブリッド同期のみに適用されます。
  
|**要素**|**説明**|
|:-----|:-----|
|**cacheActivities** <br/> |プロバイダーは不要になったユーザーのストア内の非表示のフォルダーにそれらをキャッシュすることによって動作を同期するため、この要素の無視を OSC Outlook ソーシャル コネクタ 2013 で開始、します。  <br/> プロバイダーのサポート活動、プロバイダーがサポートする必要がある場合は、オン ・ デマンドの活動を同期します。 プロバイダーは、 **cacheActivities**を**false**に設定し、 **dynamicActivitesLookupEx**を**true**に設定します。 OSC では、アクティビティ、オンデマンドでの同期をとり、メモリ内のアクティビティをキャッシュします。 活動のメモリ キャッシュは、30 分間隔で更新されます。  <br/> |
   
次の要素は、オン ・ デマンドの同期または活動のハイブリッド同期のみに適用されます。
  
|**要素**|**説明**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |OSC 1.1 では使用されなくなりました。  <br/> OSC を不要になったは OSC 1.1 以降では、 [ISocialSession::GetActivities](isocialsession-getactivities.md)を呼び出すし、 **dynamicActivitiesLookup**の値は無視されます。 オン ・ デマンドでのアクティビティの参照をサポートするには、 **false を指定**し、 **getActivities**と**true** **dynamicActivitiesLookupEx**と、OSC に**ISocialSession2::GetActivitiesEx**を呼び出すと**cacheActivities**を設定します。  <br/> |
|**dynamicActivitiesLookupEx** <br/> |OSC プロバイダーがオンデマンドの同期アクティビティのための**ISocialSession2::GetActivitiesEx**の呼び出しをサポートしているかどうかを示します。  <br/> OSC プロバイダーでは、オンデマンド アクティビティ同期をサポートする場合、 **getActivities**および**dynamicActivitiesLookupEx**として設定**true**および**false**として**cacheActivities**します。 OSC では、人物情報ウィンドウが更新されるたびに**ISocialSession2::GetActivitiesEx**をが呼び出されます。 人物情報ウィンドウは、Outlook エクスプ ローラー ウィンドウで選択した項目を変更するか、Outlook のインスペクター ウィンドウを開くときに更新されます。 参照の動的な活動により、ユーザーは、人物情報ウィンドウには、最新の活動を常に表示されますが、ソーシャル ネットワーク プロバイダーからの呼び出しの数が増加します。  <br/> 場合は、プロバイダーでは、 **dynamicActivitiesLookupEx**が**false**に設定、OSC では、人物情報ウィンドウに表示されている人は、 **ISocialSession2::GetActivitiesEx**は呼び出しません。  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |かどうか、OSC を完了しておく活動のオン ・ デマンドの同期、人物情報ウィンドウが最小化されるときを示します。  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>友人、友人以外の場合、および活動のオン ・ デマンドまたはハイブリッドの同期をサポートするための一般的な機能

|**要素**|**説明**|
|:-----|:-----|
|**実装しています。** <br/> | OSC プロバイダーをサポートするハッシュ関数を指定します。 OSC プロバイダーのソーシャル ネットワークや基幹業務アプリケーションに登録されていないユーザーの個人情報保護のため、 **ISocialSession2::GetPeopleDetails**と**ISocialSession2 にハッシュ化された e メール アドレスを渡されます。GetActivitiesEx**。  <br/>  プロバイダーが使用可能な値のいずれかに**実装しています。** を設定する必要があります**dynamicContactsLookup**が**true**に設定、または**dynamicActivitiesLookupEx**が**true**に設定されて、: **SHA1**、 **MD5**、または**CRC32MD5**。 **実装しています。** が存在しないか不適切な値を指定する場合、OSC はエラーを返します。  <br/> **SHA1**は、インターネット技術標準化委員会 (IETF) 米国のセキュリティで保護されたハッシュ アルゴリズム[[RFC3174]](http://www.rfc-editor.org/rfc/rfc3174.txt)で定義されている 1 です。 電子メール アドレス melissa@contoso.com の**SHA1**ハッシュ値は、たとえば、 `bb81577b567262a21a4df5f6e335c1250acd7b50`。  <br/> **MD5**は、 [[RFC1321]](http://www.rfc-editor.org/rfc/rfc1321.txt)で定義されている、インターネット技術標準化委員会 (IETF) MD5 メッセージ ダイジェスト アルゴリズムです。 電子メール アドレス melissa@contoso.com の**MD5**ハッシュ値は、たとえば、 `c8c39e61ca1662477b39b83d7b0a0615`。  <br/> **CRC32MD5**は**CRC32**の組み合わせであり、 **MD5**は次のように定義されています。  <br/>  先頭および末尾の空白文字とすべての文字を小文字に変換を削除することによって電子メール アドレスを正規化します。  <br/>  正規化された電子メール アドレスの**CRC32**の値を計算し、この値の 10 進の整数表現を使用します。 実装では、符号付き整数が返された場合は、符号なし整数の符号付き整数を変換する必要があります。  <br/>  正規化された電子メール アドレスの**MD5**値を計算し、この値を使用して小文字の A F から) の 16 進表現を使用します。  <br/>  アンダー スコアでこれら 2 つの値を結合します。  <br/>  電子メール アドレス melissa@contoso.com の**CRC32MD5**のハッシュ値は、たとえば、 `2149665315_c8c39e61ca1662477b39b83d7b0a0615`。  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>認証およびアカウントの構成をサポートするための機能

|**要素**|**説明**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |ソーシャル ネットワークにログオンする別の URL を提供するなど、自動構成の設定を変更するユーザーができるかどうかを示します。  <br/> |
|**createAccountUrl** <br/> |プロバイダーでは、**ここをクリックすると、アカウントを作成する****アカウントの構成**] ダイアログ ボックスをしてユーザーがクリックしたときに**false**として**hideHyperlinks**を設定、 **createAccountUrl**で指定された URL は既定のブラウザーで開きます。  <br/> |
|**displayUrl** <br/> |アカウントの構成] ダイアログ ボックスで、OSC がソーシャル ネットワークの**URL アドレス**] ボックスを表示する必要があるかどうかを示します。  <br/> |
|**forgotPasswordUrl** <br/> |プロバイダーは、ユーザーがクリックしたときに**false**として**hideHyperlinks**を設定する場合 **、パスワードを忘れた?** **アカウントの構成**] ダイアログ ボックスで、 **forgotPasswordUrl**によって指定された URL が既定のブラウザーで開きます。  <br/> |
|**hideHyperlinks** <br/> |OSC の**ここをクリックしてアカウントを作成**するして必要があります非表示かどうかを示すと**パスワードを忘れた場合ですか?** アカウントの構成] ダイアログ ボックス内のハイパーリンク。  <br/> OSC 1.0 は、この設定を無視し、ハイパーリンクが常に非表示。 OSC 1.1 は、この設定の値を監視します。  <br/> |
|**hideRememberMyPassword** <br/> |OSC がアカウントの構成] ダイアログ ボックスで、 **[パスワードの保存**] チェック ボックスを非表示にする必要があるかどうかを示します。  <br/> 場合は、プロバイダーでは、 **hideRememberMyPassword**を設定**は**、 **[パスワード**] ボックスがチェックされていないと、パスワードは保存されません、OSC が動作します。  <br/> 場合は、プロバイダーでは、 **hideRememberMyPassword**が**false**に設定、OSC は、アカウントの構成] ダイアログ ボックスで、 **[パスワードの保存**] チェック ボックスを表示します。  <br/> |
|**supportsAutoConfigure** <br/> |OSC が自動構成を試みるし、ユーザーのソーシャル ネットワークにログオンする**ISocialProvider**インターフェイスで、 **GetAutoConfiguredSession**関数を呼び出す必要があるかどうかを示します。  <br/> |
|**useLogonCached** <br/> |OSC プロバイダーがキャッシュされた資格情報でログオンするのには[ISocialSession2::LogonCached](isocialsession2-logoncached.md)の呼び出しをサポートしているかどうかを示します。  <br/> 場合は、プロバイダーでは、 **true**として**useLogonCached**が設定を OSC **useLogonWebAuth**の設定は無視され、OSC が認証のために**ISocialSession2::LogonCached**を呼び出します。  <br/> 場合は、プロバイダーでは、 **dynamicActivitiesLookupEx**が**false**に設定、OSC では、認証には、 **ISocialSession2::LogonCached**は呼び出しません。  <br/> |
|**useLogonWebAuth** <br/> |OSC でフォーム ベースの認証と、 [ISocialSession::LogonWeb](isocialsession-logonweb.md)メソッドを使用する必要があるかどうかを示します。 プロバイダーでは、 **useLogonWebAuth**が**false**に設定、OSC は基本認証を使用し、 [ISocialSession::Logon](isocialsession-logon.md)メソッドを呼び出します。 プロバイダーでは、 **useLogonWebAuth**を設定**は**場合、OSC はフォーム ベース認証を使用し、 **ISocialSession::LogonWeb**を呼び出します。  <br/> |
   
**機能**によって XML プロバイダーによって返される、メソッドでは、 **ISocialProvider::GetCapabilities**アカウントの構成] ダイアログ ボックスが変化します。 たとえば、図 1 は、TestProvider などのアカウントの構成] ダイアログ ボックスを示しています。 
  
**図 1 です。アカウントの構成] ダイアログ ボックスで、TestProvider の使用例**

![TestProvider の構成情報の例](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>関連項目

- [機能のための XML](xml-for-capabilities.md)

