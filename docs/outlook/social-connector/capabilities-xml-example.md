---
title: 機能 XML の例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: 'このトピックの xml の例は、ソーシャルネットワークの imethod alprovider:: getcapabilities メソッドを呼び出すと、Outlook Social Connector (.osc) に返される xml 文字列です。 XML は、.osc プロバイダーが、.osc の機能と要件を指定する方法を示しています。'
ms.openlocfilehash: 53bd250432e7b27d984a846d206adc812c47898f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281231"
---
# <a name="capabilities-xml-example"></a>機能 XML の例

このトピックの xml の例は、ソーシャルネットワークの[imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出すと、Outlook Social Connector (.osc) に返される xml 文字列です。 XML は、.osc プロバイダーが、.osc の機能と要件を指定する方法を示しています。 
  
## <a name="capabilities-for-friends"></a>フレンドの機能

この例では、.osc プロバイダーは、フレンド機能をサポートする機能を示す次の要素を指定します。
  
- **** .osc プロバイダーが[iGetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)メソッドをサポートして、プログラムによって友人の情報を取得するように指定するには、 **true**として取得します。 
    
- Outlook の連絡先フォルダー内のフレンドの情報のキャッシュをサポートする場合は、 **cacheFriends**を**true**にします。 
    
- **contactsyncrestartinterval**を60として、エラーが発生した場合、.osc は60分ごとにキャッシュの更新を再試行する必要があることを示します。 
    
- **ユーザー**がソーシャルネットワークにフレンドを追加する機能を示す**場合は true**にします。 
    
- **** .osc クラスが、ソーシャルネットワーク上のフレンドとしてのユーザーの削除をサポートしていないことを示すため、 **false**として表示されます。 
    
- **dynamicContactsLookup**を**false**として、.osc がフレンドの情報をメモリに格納しないように指定します。 
    
## <a name="capabilities-for-activities"></a>アクティビティの機能

.osc プロバイダーは、アクティビティをサポートする機能を示す次の要素を指定します。
  
- プログラムによってフレンドのアクティビティを取得するために、.osc プロバイダーが[iGetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md)メソッドをサポートしていることを示すために、[ **getactivities** ] を**true**とします。 
    
- 非表示の Outlook ニュースフィードフォルダーでのフレンドの処理のキャッシュをサポートするには、 **cacheactivities**を**false**にします。 
    
- **dynamicActivitiesLookupEx**がフレンドのアクティビティをメモリに格納することを示すには、 **true**にします。 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>認証およびアカウント構成の機能

.osc プロバイダーは、認証およびアカウント構成のサポートを示すために、次の要素を指定します。
  
- .osc プロバイダーが基本認証をサポートしていることを示すには、 **uselogonwebauth**を**false**として指定します。 
    
- **supportsAutoConfigure**は、ユーザーのソーシャルネットワークへの自動的な構成およびログオンを行わないようにするため、.osc が**false**として設定されます。 
    
- **uselogoncached**と**hideRememberMyPassword**を**false**として、.osc が毎回パスワードの入力を要求する必要があり、キャッシュされたログオン資格情報を使用してログオンしてはいけないことを示します。 
    
- [アカウント構成] ダイアログボックスで、.osc がソーシャルネットワークの URL を表示しないようにするには、 **displayurl**を**false**として指定します。 
    
- **hidehyperlinks**を**false**に設定して、.osc プロバイダーが既知のパスワードを持つ既存のアカウントのみをサポートすることを示す場合、 **[ここをクリック**してアカウントを作成し、**パスワードを忘れますか?** ] のハイパーリンクを表示しないようにします。[アカウントの構成] ダイアログボックス 
    
## <a name="xml-example"></a>XML の例

次の例は、.osc プロバイダーの**機能**XML を示しています。 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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

- [.osc プロバイダーの XML の例](osc-provider-xml-examples.md)  
- [機能の XML](xml-for-capabilities.md)  
- [Friends XML の例](friends-xml-example.md)  
- [アクティビティフィード XML の例](activity-feed-xml-example.md)  
- [Outlook Social Connector プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)

