---
title: 機能 XML の例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: ここでの XML の例は、ソーシャル ネットワークの ISocialProvider::GetCapabilities メソッドが呼び出された後に、Outlook ソーシャル コネクタ (OSC) が返される XML 文字列です。 XML は、その機能や、OSC の要件に、OSC プロバイダーを指定する方法を示しています。
ms.openlocfilehash: 53bd250432e7b27d984a846d206adc812c47898f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389548"
---
# <a name="capabilities-xml-example"></a>機能 XML の例

ここでの XML の例は、ソーシャル ネットワークの[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドが呼び出された後に、Outlook ソーシャル コネクタ (OSC) が返される XML 文字列です。 XML は、その機能や、OSC の要件に、OSC プロバイダーを指定する方法を示しています。 
  
## <a name="capabilities-for-friends"></a>友人のための機能

OSC プロバイダーは、この例では、フレンド機能をサポートすることでその機能を表示するのには次の要素を指定します。
  
- **true**を示す OSC プロバイダーとして**getFriends**には、プログラムを使用して友人の情報を取得する[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)メソッドがサポートされています。 
    
- **true**の Outlook 連絡先フォルダーのキャッシュの友人の情報をサポートするために**cacheFriends**をします。 
    
- そのエラーを示すために 60 と**contactSyncRestartInterval**が、60 分ごとにキャッシュを更新、OSC が再試行します。 
    
- **followPerson**の**場合は true**をソーシャル ネットワーク上の友人を追加することを示します。 
    
- **false**を示す OSC プロバイダーとして**doNotFollowPerson**では、ソーシャル ネットワークで友達とユーザーを削除することはサポートされていません。 
    
- として**false** OSC によって、メモリ内の友人の情報が格納する必要があることを示すために**dynamicContactsLookup**をします。 
    
## <a name="capabilities-for-activities"></a>活動のための機能

OSC プロバイダーは、活動をサポートするためにその機能を表示するのには次の要素を指定します。
  
- **getActivities**の**場合は true**を示す OSC プロバイダーがプログラムを使用して友人の活動を取得する[ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md)メソッドをサポートするいるとします。 
    
- として**false**非表示のニュース フィードの Outlook フォルダーに友人のキャッシュの動作をサポートするために**cacheActivities**をします。 
    
- **dynamicActivitiesLookupEx**の**場合は true** OSC が、友人の活動をメモリに格納する必要があることを示す。 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>認証およびアカウントの構成のための機能

OSC プロバイダーは、認証およびアカウントの構成のサポートを表示するのには次の要素を指定します。
  
- **useLogonWebAuth**の**場合は false**を示す OSC プロバイダーが基本認証をサポートするいるとします。 
    
- **false**を示すこと、OSC しないように自動的に構成し、ユーザーのソーシャル ネットワークにログオンすると**supportsAutoConfigure**にします。 
    
- **useLogonCached**と**false の場合**は使用しないでください、OSC たびにパスワードを入力する必要があることを示すためとして**hideRememberMyPassword**にログオンするログオン資格情報がキャッシュされます。 
    
- **displayUrl**を**false** OSC がアカウントの構成] ダイアログ ボックスでソーシャル ネットワークの URL を表示しないことを指定するとします。 
    
- として**false** OSC プロバイダーには、既知のパスワードで既存のアカウントのみがサポートされています、OSC に**アカウントを作成するのにはここをクリック**を表示しないことを示すために**hideHyperlinks**と **、パスワードを忘れた?** 内のハイパーリンク、アカウントの構成] ダイアログ ボックスです。 
    
## <a name="xml-example"></a>XML の例

OSC プロバイダーの XML**機能**の例を次に示します。 
  
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

- [OSC プロバイダーの XML の例](osc-provider-xml-examples.md)  
- [機能のための XML](xml-for-capabilities.md)  
- [友人の XML の例](friends-xml-example.md)  
- [アクティビティ フィードの XML の例](activity-feed-xml-example.md)  
- [Outlook ソーシャル コネクタ プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)

