---
title: 機能 XML の例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: このトピックの XML の例は、ソーシャル ネットワークの ISocialProvider::GetCapabilities メソッドを呼び出した後、Outlook Social Connector (OSC) に返される XML 文字列です。 XML は、OSC プロバイダーが OSC の機能と要件を指定する方法を示しています。
ms.openlocfilehash: 7ab0e08739e77964fcea4874e2422d12c65d753a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608915"
---
# <a name="capabilities-xml-example"></a>機能 XML の例

このトピックの XML の例は、ソーシャル ネットワークの[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出した後、Outlook Social Connector (OSC) に返される XML 文字列です。 XML は、OSC プロバイダーが OSC の機能と要件を指定する方法を示しています。 
  
## <a name="capabilities-for-friends"></a>フレンドの機能

この例では、OSC プロバイダーは、フレンド機能をサポートする機能を示す次の要素を指定します。
  
- **getFriends** **as true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) メソッドを使用して、友人の情報をプログラムで取得します。 
    
- **cacheFriends** を **true に** 設定すると、連絡先フォルダーに友人の情報をOutlookできます。 
    
- **エラーが発生した場合、OSC** は 60 分ごとにキャッシュの更新を再試行する必要があります。 
    
- **followPerson** **を true** に設定して、ソーシャル ネットワークにフレンドを追加する機能を示します。 
    
- **doNotFollowPerson** **を false** として指定すると、OSC プロバイダーはソーシャル ネットワーク上のフレンドとして人物の削除がサポートされていません。 
    
- **dynamicContactsLookup** **を false** として指定すると、OSC はフレンドの情報をメモリに格納しなけれます。 
    
## <a name="capabilities-for-activities"></a>アクティビティの機能

OSC プロバイダーは、アクティビティをサポートする機能を示す次の要素を指定します。
  
- **getActivities** を **true** に設定すると、OSC プロバイダーが [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) メソッドをサポートして、プログラムによってフレンドのアクティビティを取得できます。 
    
- **cacheActivities を** **false** に設定して、非表示の [ニュース フィード] フォルダー内の友人のOutlookをサポートします。 
    
- **dynamicActivitiesLookupEx** **を true** として指定すると、OSC はフレンドのアクティビティをメモリに格納する必要があります。 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>認証とアカウント構成の機能

OSC プロバイダーは、認証とアカウント構成のサポートを示す次の要素を指定します。
  
- **useLogonWebAuth** **を false として指定** すると、OSC プロバイダーが基本認証をサポートします。 
    
- osC が自動的に構成し、ユーザーのソーシャル ネットワークにログオンしようとしなけれない場合は **、false としてAutoConfigure** をサポートします。 
    
- **useLogonCached** と **hideRememberMyPassword** を **false** として指定すると、OSC は毎回パスワードの入力を求める必要があります。また、キャッシュされたログオン資格情報を使用してログオンする必要はありません。 
    
- **displayUrl** を **false** として指定して、OSC がアカウント構成ダイアログ ボックスにソーシャル ネットワークの URL を表示しなかるべきかどうかを示します。 
    
- **hideHyperlinks** as **false** は、OSC プロバイダーが既知のパスワードを持つ既存のアカウントのみをサポートし、OSCが [アカウントを作成するにはここをクリックしてアカウントを作成する] および [パスワードを忘れた場合] ハイパーリンクをアカウント構成ダイアログ ボックスに表示しない必要があります。 
    
## <a name="xml-example"></a>XML の例

次の例は、OSC **プロバイダーの** 機能 XML を示しています。 
  
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

- [OSC プロバイダー XML の例](osc-provider-xml-examples.md)  
- [機能の XML](xml-for-capabilities.md)  
- [Friends XML の例](friends-xml-example.md)  
- [アクティビティ フィード XML の例](activity-feed-xml-example.md)  
- [Outlookソーシャル コネクタ プロバイダー XML スキーマ](outlook-social-connector-provider-xml-schema.md)

