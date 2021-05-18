---
title: 機能 XML の要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: このトピックの表では、機能 XML の子要素について説明し、サポートする領域によってグループ化されています。
ms.openlocfilehash: 6816bbdcd24eceffc47d6b9d0835a90c7089c039
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281194"
---
# <a name="capabilities-xml-elements"></a>機能 XML の要素

このトピックの表では、機能 **XML** の子要素について説明し、サポートする領域によってグループ化されています。 各 capabilities 要素の既定値 **は** false **です**。 要素が [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドによって返される機能 **XML** で指定されていない場合、要素の値は false に等 **しくなります**。
  
機能 XML の **概要については** 、「XML [for Capabilities」を参照してください](xml-for-capabilities.md)。 機能 XML の例 **については、「Capabilities** [XML の例」を参照してください](capabilities-xml-example.md)。 必要またはオプションの要素を含む、Microsoft Outlook Social Connector (OSC) プロバイダー XML スキーマの完全な定義については [、「Outlook Social](outlook-social-connector-provider-xml-schema.md)Connector Provider XML スキーマ」を参照してください。
  
## <a name="capabilities-for-supporting-friends"></a>友人をサポートするための機能

次の表は、友人または友人以外の同期の任意の形式に適用される要素を示しています。
  
|**要素**|**説明**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |プロバイダーが [ISocialSession::UnFollowPerson](isocialsession-unfollowperson.md) メソッド呼び出しをサポートするかどうかを示します。  <br/> **followPerson** と **doNotFollowPerson は** 、OSC プロバイダーの独立した機能です。 OSC プロバイダーは、ユーザーをフレンドとして追加できる機能 **(followPerson** を **true** に設定) またはソーシャル ネットワーク アカウントでフレンドとして削除できる機能を示します **(doNotFollowPerson** を **true** に設定します)。 一般に、フォローできるからといって、フォローを停止できるという問題ではありません。 **followPerson** は機能であり、特定のユーザーまたはソーシャル ネットワーク アカウントのすべてのユーザーをフォローするアクションとして誤解される必要はありません。 **followPerson が** **true であること** は **、doNotFollowPerson** が false という意味 **ではありません**。  <br/> |
|**followPerson** <br/> |プロバイダーが [ISocialSession::FollowPerson](isocialsession-followperson.md) メソッド呼び出しをサポートするかどうかを示します。 OSC は **、cacheFriends** が true **(友人** のキャッシュ同期) である場合 **、dynamicContactsLookup** が true **(フレンド** とフレンド以外のオンデマンド同期) の場合、または **cacheFriends** と **dynamicContactsLookup** の両方が true (友人と友人以外のハイブリッド同期) の場合に **followPerson** をチェックします。 プロバイダーが **followPerson** をtrue に設定すると、ユーザーがフォローしているユーザーのネットワーク バッジがユーザー ウィンドウに表示され、ユーザー ウィンドウの [追加] **(+)** メニューで **\< [ネットワーク \>** 名] コマンドを有効にします。 プロバイダーが **followPerson を** **false** に設定すると、ネットワーク バッジは表示されません **\< 。on NetworkName \>** コマンドは非表示になります。  <br/> |
|**getFriends** <br/> |プロバイダーが [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) または [ISocialSession2:::GetPeopleDetails](isocialsession2-getpeopledetails.md) メソッド呼び出しをサポートするかどうかを示します。 プロバイダーが getFriends をtrue に設定した場合、OSC は **cacheFriends** または **dynamicContactsLookup** の値を使用して、ソーシャル ネットワークでフレンドを Outlook 連絡先アイテムまたはメモリに格納できるかどうかを判断します。  プロバイダーが **getFriends** をfalse に設定した場合、ソーシャル ネットワークはフレンドと **ISocialPerson::GetFriendsAndColleagues** メソッドと **ISocialSession2::GetPeopleDetails** メソッドをサポートしません。OSC は **cacheFriends** メソッドと **dynamicContactsLookup** の値を無視します。  <br/> |
   
次の要素は、友人のキャッシュされた同期、または友人と友人以外のハイブリッド同期にのみ適用されます。 友人の同期の詳細については、「友人とアクティビティの [同期」を参照してください](synchronizing-friends-and-activities.md)。
  
|**要素**|**説明**|
|:-----|:-----|
|**cacheFriends** <br/> |OSC プロバイダーが Outlook 連絡先アイテムとしてフレンドを格納できるかどうかを示します。 OSC は **、getFriends が** true の **場合にのみ cacheFriends を** チェック **します**。 プロバイダーが **cacheFriends** を **true** に設定すると、OSC はキャッシュによってフレンドを同期し、フレンド連絡先のユーザーの既定のストアにネットワーク固有の連絡先フォルダーを作成します。 ネットワーク固有の連絡先フォルダーの名前は [、ISocialProvider::SocialNetworkName プロパティの値](isocialprovider-socialnetworkname.md) です。 プロバイダーが **cacheFriends** を **false** に設定した場合、OSC は友人の連絡先が友人を保存するネットワーク固有の連絡先フォルダーを作成しない。  <br/> |
|**contactSyncRestartInterval** <br/> |同期エラーが発生した場合に、ソーシャル ネットワークから友人の情報を同期する試行の間の再試行間隔を分で指定します。 OSC は、OSC プロバイダーがソーシャル ネットワーク固有の連絡先フォルダーへの友人のキャッシュ同期またはハイブリッド同期をサポートしている場合にのみ、この要素を使用します **(cacheFriends は** **true)。**  <br/> 既定の再試行間隔は 30 分です。既定値が下のキーによって  `ContactSyncRestartInterval` 上書きされない限り  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` 。 プロバイダーが **contactSyncRestartInterval** を設定すると、プロバイダー値は既定の再試行間隔 30 分またはレジストリ キー値を上書きします。  <br/> フレンドとフレンド以外の情報をオンデマンドで同期する方法の詳細については、「同期するフレンドとアクティビティ」 [を参照してください](synchronizing-friends-and-activities.md)。  <br/> |
   
次の要素は、友人と友人以外のオンデマンド同期またはハイブリッド同期にのみ適用されます。
  
|**要素**|**説明**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |OSC プロバイダーが [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) 呼び出しをサポートするかどうかを示します。  <br/> OSC は、getFriends が true の場合にのみ **、dynamicContactsLookup を** チェック **します**。 **dynamicContactsLookup の既定の設定は** false **です**。  <br/> OSC プロバイダーが **dynamicContactsLookup** をtrue に指定し **、getFriends** を true に指定すると、ユーザー ウィンドウが更新されるごとに、OSC は **ISocialSession2::GetPeopleDetails** を呼び出します。 ユーザー ウィンドウは、ユーザー ウィンドウまたは Outlook エクスプローラー ウィンドウ内の別のアイテムで別のユーザーを選択するか、Outlook インスペクター ウィンドウを開くと更新されます。 動的な連絡先の参照により、ユーザーは常にユーザー ウィンドウに最新のユーザー画像とプロファイル情報が表示されますが、プロバイダーからソーシャル ネットワークへの呼び出しの数が増えます。  <br/> プロバイダーが **dynamicContactsLookup** を **false** に設定した場合、OSC は **ISocialSession2::GetPeopleDetails** を呼び出して People Pane を更新しません。  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |ユーザー ウィンドウを最小化するときに、OSC がフレンドと非フレンドのオンデマンド同期を実行する必要があるかどうかを示します。  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>アクティビティをサポートする機能

次の要素は、OSC プロバイダーがサポートするアクティビティの任意の形式の同期に適用されます。
  
|**要素**|**説明**|
|:-----|:-----|
|**getActivities** <br/> |プロバイダーが [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) または [ISocialPerson::GetActivities](isocialperson-getactivities.md) メソッド呼び出しをサポートするかどうかを示します。 プロバイダーが getActivities をtrue に設定すると、OSC は **cacheActivities** または **dynamicActivitiesLookupEx** の値を使用して、ソーシャル ネットワーク サイトが Outlook RSS アイテムまたはメモリ内アクティビティとしてアクティビティを格納できるかどうかを判断します。  プロバイダーが **getActivities** をfalse に設定すると、ソーシャル ネットワークはアクティビティと **ISocialSession2::GetActivitiesEx** メソッドと **ISocialPerson::GetActivities** メソッドをサポートし、OSC は cacheActivities メソッドと **dynamicActivitiesLookupEx** の値を無視します。   <br/> |
   
次の要素は、キャッシュされた同期またはアクティビティのハイブリッド同期にのみ適用されます。
  
|**要素**|**説明**|
|:-----|:-----|
|**cacheActivities** <br/> |Outlook Social Connector 2013 以降、OSC は、プロバイダーがユーザーのストア内の非表示フォルダーにキャッシュしてアクティビティを同期できなくなったので、この要素を無視します。  <br/> プロバイダーがアクティビティをサポートしている場合、プロバイダーはオンデマンドでアクティビティの同期をサポートする必要があります。 プロバイダーは **cacheActivities を** **false** に設定し **、dynamicActivitesLookupEx** を true に **設定します**。 OSC は、オンデマンドでアクティビティを同期し、アクティビティをメモリにキャッシュします。 アクティビティのメモリ キャッシュは、30 分間隔で更新されます。  <br/> |
   
次の要素は、オンデマンド同期またはアクティビティのハイブリッド同期にのみ適用されます。
  
|**要素**|**説明**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |OSC 1.1 では非推奨です。  <br/> OSC 1.1 から、OSC は [ISocialSession::GetActivities](isocialsession-getactivities.md) を呼び出さなくなったので **、dynamicActivitiesLookup** の値を無視します。 オンデマンド アクティビティの参照をサポートするには **、cacheActivities** を **false、getActivities、dynamicActivitiesLookupEx** を true に設定し、OSC は **ISocialSession2::GetActivitiesEx** を呼び出します。    <br/> |
|**dynamicActivitiesLookupEx** <br/> |OSC プロバイダーが、アクティビティのオンデマンド同期を求める **ISocialSession2::GetActivitiesEx** 呼び出しをサポートするかどうかを示します。  <br/> OSC プロバイダーがオンデマンド アクティビティの同期をサポートしている場合は **、getActivities** と **dynamicActivitiesLookupEx** を **true** に設定し **、cacheActivities** を false に **設定します**。 OSC は、People Pane が更新されるごとに **ISocialSession2::GetActivitiesEx** を呼び出します。 ユーザーが Outlook エクスプローラー ウィンドウで選択したアイテムを変更するか、Outlook インスペクター ウィンドウを開くと、ユーザー ウィンドウが更新されます。 動的アクティビティの参照により、ユーザーは常に People Pane に最新のアクティビティを表示しますが、プロバイダーからソーシャル ネットワークへの呼び出しの数が増えます。  <br/> プロバイダーが **dynamicActivitiesLookupEx** をfalse に設定した場合、OSC はユーザー ウィンドウに表示されるユーザーに対して **ISocialSession2::GetActivitiesEx** を呼び出す必要があります。  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |ユーザー ウィンドウを最小化するときに、OSC がアクティビティのオンデマンド同期を実行するかどうかを示します。  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>友人、友人以外、およびアクティビティのオンデマンドまたはハイブリッド同期をサポートするための一般的な機能

|**要素**|**説明**|
|:-----|:-----|
|**hashFunction** <br/> | OSC プロバイダーがサポートするハッシュ関数を指定します。 プロバイダーのソーシャル ネットワークまたは業務上のアプリケーションではないユーザーの個人を特定できる情報を保護するために、OSC はハッシュされた電子メール アドレスを **ISocialSession2:::GetPeopleDetails** および **ISocialSession2::GetActivitiesEx** に渡します。  <br/>  **dynamicContactsLookup** が **true** に設定されている場合、または **dynamicActivitiesLookupEx** が **true** に設定されている場合、プロバイダーは **hashFunction** を **SHA1、MD5、** または **CRC32MD5** のいずれかの値に設定する必要があります。  **hashFunction が見** つからないか、正しくない値を指定すると、OSC はエラーを返します。  <br/> **SHA1** は [、[RFC3174]](https://www.rfc-editor.org/rfc/rfc3174.txt)で定義されたインターネット エンジニアリング タスク フォース (IETF) US Secure Hash Algorithm 1 です。 たとえば、メール アドレス **の SHA1** ハッシュ値は次 melissa@contoso.com です  `bb81577b567262a21a4df5f6e335c1250acd7b50` 。  <br/> **MD5** はインターネット エンジニアリング タスク フォース (IETF) MD5 Message-Digest [[RFC1321]](https://www.rfc-editor.org/rfc/rfc1321.txt)で定義されているアルゴリズムです。 たとえば、電子メール アドレス **の MD5** ハッシュ値 melissa@contoso.com です  `c8c39e61ca1662477b39b83d7b0a0615` 。  <br/> **CRC32MD5 は****、次のように定義された CRC32** と **MD5 の** 組み合わせです。  <br/>  先頭と末尾の空白文字を削除し、すべての文字を小文字に変換して、電子メール アドレスを正規化します。  <br/>  正規化された **電子メール アドレスの CRC32** 値を計算し、この値の 10 進整数表記を使用します。 実装が符号付き整数を返す場合は、符号付き整数を符号なし整数に変換する必要があります。  <br/>  正規化された **電子メール アドレスの MD5** 値を計算し、この値の 16 進表記を使用します (A ~ F の場合は小文字を使用)。  <br/>  これら 2 つの値をアンダースコアと組み合わせます。  <br/>  たとえば、電子メール **アドレスの CRC32MD5** ハッシュ値 melissa@contoso.com です  `2149665315_c8c39e61ca1662477b39b83d7b0a0615` 。  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>認証とアカウント構成をサポートする機能

|**要素**|**説明**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |ユーザーがログオンする別の URL を指定するなどの自動構成設定をソーシャル ネットワークで変更できるかどうかを示します。  <br/> |
|**createAccountUrl** <br/> |プロバイダーが **hideHyperlinks** をfalse に設定すると、ユーザーが [アカウント構成]ダイアログ ボックスで [ここをクリックしてアカウントを作成する] をクリックすると **、createAccountUrl** で指定された URL が既定のブラウザーで開きます。   <br/> |
|**displayUrl** <br/> |OSC がソーシャル ネットワークの **[URL アドレス** ] テキスト ボックスを [アカウント構成] ダイアログ ボックスに表示するかどうかを示します。  <br/> |
|**forgotPasswordUrl** <br/> |プロバイダーが **hideHyperlinks** を **false** に設定した場合、ユーザーが [アカウント構成] ダイアログ ボックスで [パスワードを忘れた場合] をクリックすると **、forgotPasswordUrl** で指定された URL が既定のブラウザーで開きます。  <br/> |
|**hideHyperlinks** <br/> |OSC で [ここをクリックしてアカウントを作成する] と [パスワードを忘れた場合 **]** ハイパーリンクを [アカウント構成] ダイアログ ボックスで非表示にするかどうかを示します。  <br/> OSC 1.0 ではこの設定は無視され、ハイパーリンクは常に非表示になります。 OSC 1.1 は、この設定の値を監視します。  <br/> |
|**hideRememberMyPassword** <br/> |OSC が [アカウント構成] ダイアログ ボックスの **[** パスワードを記憶する] チェック ボックスを非表示にするかどうかを示します。  <br/> プロバイダーが **hideRememberMyPassword** を **true** に設定すると、OSCは [パスワードを記憶する] ボックスがオフになっている場合と同様に機能し、パスワードは保存されません。  <br/> プロバイダーが **hideRememberMyPassword** を **false** に設定すると、OSC は [アカウント構成] ダイアログ ボックスに [パスワードを記憶する] チェック ボックスを表示します。   <br/> |
|**supportsAutoConfigure** <br/> |OSC が **ISocialProvider** インターフェイスで **GetAutoConfiguredSession** 関数を呼び出して、自動構成を試み、ユーザーのソーシャル ネットワークにログオンするかどうかを示します。  <br/> |
|**useLogonCached** <br/> |OSC プロバイダーがキャッシュされた資格情報でログオンするための [ISocialSession2::LogonCached](isocialsession2-logoncached.md) 呼び出しをサポートするかどうかを示します。  <br/> プロバイダーが **useLogonCached** を **true** に設定すると、OSC は **useLogonWebAuth** の設定を無視し、OSC は認証のために **ISocialSession2::LogonCached** を呼び出します。  <br/> プロバイダーが **dynamicActivitiesLookupEx** を **false** に設定した場合、OSC は認証のために **ISocialSession2::LogonCached** を呼び出す必要があります。  <br/> |
|**useLogonWebAuth** <br/> |OSC がフォーム ベース認証と [ISocialSession::LogonWeb メソッド](isocialsession-logonweb.md) を使用するかどうかを示します。 プロバイダーが **useLogonWebAuth** を **false** に設定すると、OSC は基本認証を使用し [、ISocialSession::Logon メソッドを呼び出](isocialsession-logon.md) します。 プロバイダーが **useLogonWebAuth** を **true** に設定すると、OSC はフォーム ベース認証を使用し **、ISocialSession::LogonWeb を呼び出します**。  <br/> |
   
**ISocialProvider::GetCapabilities** メソッドのプロバイダーによって返される機能 **XML** に応じて、アカウント構成ダイアログ ボックスが変更されます。 たとえば、図 1 は TestProvider の例のアカウント構成ダイアログ ボックスを示しています。 
  
**図 1.アカウント構成ダイアログ ボックスの TestProvider の例**

![TestProvider の構成情報の例](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)

