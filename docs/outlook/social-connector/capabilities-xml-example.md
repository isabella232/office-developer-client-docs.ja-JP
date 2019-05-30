---
title: 機能 XML の例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: 'このトピックの XML の例は、ソーシャルネットワークの Imethod Alprovider:: GetCapabilities メソッドを呼び出すと、Outlook Social Connector (.OSC) に返される XML 文字列です。 XML は、.OSC プロバイダーが、.OSC の機能と要件を指定する方法を示しています。'
ms.openlocfilehash: 3340f5b1e0718edd1a062ab817c6621c338bee42
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542262"
---
# <a name="capabilities-xml-example"></a>機能 XML の例

このトピックの XML の例は、ソーシャルネットワークの[Imethod Alprovider:: GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出すと、Outlook Social CONNECTOR (.osc) に返される xml 文字列です。 XML は、.OSC プロバイダーが、.OSC の機能と要件を指定する方法を示しています。 
  
## <a name="capabilities-for-friends"></a>フレンドの機能

この例では、.OSC プロバイダーは、フレンド機能をサポートする機能を示す次の要素を指定します。
  
- **** .osc プロバイダーが[iGetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)メソッドをサポートして、プログラムによって友人の情報を取得するように指定するには、 **true**として取得します。 
    
- Outlook の連絡先フォルダー内のフレンドの情報のキャッシュをサポートする場合は、 **cacheFriends**を**true**にします。 
    
- **Contactsyncrestartinterval**を60として、エラーが発生した場合、.osc は60分ごとにキャッシュの更新を再試行する必要があることを示します。 
    
- **ユーザー**がソーシャルネットワークにフレンドを追加する機能を示す**場合は true**にします。 
    
- **** .osc クラスが、ソーシャルネットワーク上のフレンドとしてのユーザーの削除をサポートしていないことを示すため、 **false**として表示されます。 
    
- **dynamicContactsLookup**を**false**として、.osc がフレンドの情報をメモリに格納しないように指定します。 
    
## <a name="capabilities-for-activities"></a>アクティビティの機能

.OSC プロバイダーは、アクティビティをサポートする機能を示す次の要素を指定します。
  
- プログラムによってフレンドのアクティビティを取得するために、.OSC プロバイダーが[IGetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md)メソッドをサポートしていることを示すために、[ **getactivities** ] を**true**とします。 
    
- 非表示の Outlook ニュースフィードフォルダーでのフレンドの処理のキャッシュをサポートするには、 **Cacheactivities**を**false**にします。 
    
- **dynamicActivitiesLookupEx**がフレンドのアクティビティをメモリに格納することを示すには、 **true**にします。 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>認証およびアカウント構成の機能

.OSC プロバイダーは、認証およびアカウント構成のサポートを示すために、次の要素を指定します。
  
- .OSC プロバイダーが基本認証をサポートしていることを示すには、 **Uselogonwebauth**を**false**として指定します。 
    
- **supportsAutoConfigure**は、ユーザーのソーシャルネットワークへの自動的な構成およびログオンを行わないようにするため、.osc が**false**として設定されます。 
    
- **Uselogoncached**と**hideRememberMyPassword**を**FALSE**として、.osc が毎回パスワードの入力を要求する必要があり、キャッシュされたログオン資格情報を使用してログオンしてはいけないことを示します。 
    
- [アカウント構成] ダイアログボックスで、.OSC がソーシャルネットワークの URL を表示しないようにするには、 **Displayurl**を**false**として指定します。 
    
- **Hidehyperlinks**を**false**に設定して、.osc プロバイダーが既知のパスワードを持つ既存のアカウントのみをサポートすることを示す場合、 **[ここをクリック**してアカウントを作成し、**パスワードを忘れますか?** ] のハイパーリンクを表示しないようにします。[アカウントの構成] ダイアログボックス 
    
## <a name="xml-example"></a>XML の例

次の例は、.OSC プロバイダーの**機能**XML を示しています。 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <getFriends>true</getFriends>
  <cacheFriends>true</cacheFriends>
  <followPerson>true</followPerson>
  <doNotFollowPerson>false</doNotFollowPerson>
  <getActivities>true</getActivities>
  <cacheActivities>false</cacheActivities>
  <displayUrl>false</displayUrl>
  <useLogonWebAuth>false</useLogonWebAuth>
  <hideHyperlinks>false</hideHyperlinks>
  <supportsAutoConfigure>false</supportsAutoConfigure>
  <contactSyncRestartInterval>60</contactSyncRestartInterval>
  <dynamicActivitiesLookupEx>true</dynamicActivitiesLookupEx>
  <dynamicContactsLookup>false</dynamicContactsLookup>
  <useLogonCached>false</useLogonCached>
  <hideRememberMyPassword>false</hideRememberMyPassword>
  <createAccountUrl>https://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>https://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a>関連項目

- [.OSC プロバイダーの XML の例](osc-provider-xml-examples.md)  
- [機能の XML](xml-for-capabilities.md)  
- [Friends XML の例](friends-xml-example.md)  
- [アクティビティフィード XML の例](activity-feed-xml-example.md)  
- [Outlook Social Connector プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)

