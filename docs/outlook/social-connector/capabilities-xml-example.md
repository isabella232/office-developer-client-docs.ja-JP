---
title: 機能の XML の例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: ここでの XML の例は、ソーシャル ネットワークの ISocialProvider::GetCapabilities メソッドが呼び出された後に、Outlook ソーシャル コネクタ (OSC) が返される XML 文字列です。 XML は、その機能や、OSC の要件に、OSC プロバイダーを指定する方法を示しています。
ms.openlocfilehash: 5cafd6d29de8b4357e9e0ce6dab30b125f53b8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804335"
---
# <a name="capabilities-xml-example"></a><span data-ttu-id="6067c-104">機能の XML の例</span><span class="sxs-lookup"><span data-stu-id="6067c-104">Capabilities XML example</span></span>

<span data-ttu-id="6067c-105">ここでの XML の例は、ソーシャル ネットワークの[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドが呼び出された後に、Outlook ソーシャル コネクタ (OSC) が返される XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="6067c-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="6067c-106">XML は、その機能や、OSC の要件に、OSC プロバイダーを指定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6067c-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="6067c-107">友人のための機能</span><span class="sxs-lookup"><span data-stu-id="6067c-107">Capabilities for friends</span></span>

<span data-ttu-id="6067c-108">OSC プロバイダーは、この例では、フレンド機能をサポートすることでその機能を表示するのには次の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="6067c-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="6067c-109">**true**を示す OSC プロバイダーとして**getFriends**には、プログラムを使用して友人の情報を取得する[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)メソッドがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6067c-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="6067c-110">**true**の Outlook 連絡先フォルダーのキャッシュの友人の情報をサポートするために**cacheFriends**をします。</span><span class="sxs-lookup"><span data-stu-id="6067c-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="6067c-111">そのエラーを示すために 60 と**contactSyncRestartInterval**が、60 分ごとにキャッシュを更新、OSC が再試行します。</span><span class="sxs-lookup"><span data-stu-id="6067c-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="6067c-112">**followPerson**の**場合は true**をソーシャル ネットワーク上の友人を追加することを示します。</span><span class="sxs-lookup"><span data-stu-id="6067c-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="6067c-113">**false**を示す OSC プロバイダーとして**doNotFollowPerson**では、ソーシャル ネットワークで友達とユーザーを削除することはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6067c-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="6067c-114">として**false** OSC によって、メモリ内の友人の情報が格納する必要があることを示すために**dynamicContactsLookup**をします。</span><span class="sxs-lookup"><span data-stu-id="6067c-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="6067c-115">活動のための機能</span><span class="sxs-lookup"><span data-stu-id="6067c-115">Capabilities for activities</span></span>

<span data-ttu-id="6067c-116">OSC プロバイダーは、活動をサポートするためにその機能を表示するのには次の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="6067c-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="6067c-117">**getActivities**の**場合は true**を示す OSC プロバイダーがプログラムを使用して友人の活動を取得する[ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md)メソッドをサポートするいるとします。</span><span class="sxs-lookup"><span data-stu-id="6067c-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="6067c-118">として**false**非表示のニュース フィードの Outlook フォルダーに友人のキャッシュの動作をサポートするために**cacheActivities**をします。</span><span class="sxs-lookup"><span data-stu-id="6067c-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="6067c-119">**dynamicActivitiesLookupEx**の**場合は true** OSC が、友人の活動をメモリに格納する必要があることを示す。</span><span class="sxs-lookup"><span data-stu-id="6067c-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="6067c-120">認証およびアカウントの構成のための機能</span><span class="sxs-lookup"><span data-stu-id="6067c-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="6067c-121">OSC プロバイダーは、認証およびアカウントの構成のサポートを表示するのには次の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="6067c-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="6067c-122">**useLogonWebAuth**の**場合は false**を示す OSC プロバイダーが基本認証をサポートするいるとします。</span><span class="sxs-lookup"><span data-stu-id="6067c-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="6067c-123">**false**を示すこと、OSC しないように自動的に構成し、ユーザーのソーシャル ネットワークにログオンすると**supportsAutoConfigure**にします。</span><span class="sxs-lookup"><span data-stu-id="6067c-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="6067c-124">**useLogonCached**と**false の場合**は使用しないでください、OSC たびにパスワードを入力する必要があることを示すためとして**hideRememberMyPassword**にログオンするログオン資格情報がキャッシュされます。</span><span class="sxs-lookup"><span data-stu-id="6067c-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="6067c-125">**displayUrl**を**false** OSC がアカウントの構成] ダイアログ ボックスでソーシャル ネットワークの URL を表示しないことを指定するとします。</span><span class="sxs-lookup"><span data-stu-id="6067c-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="6067c-126">として**false** OSC プロバイダーには、既知のパスワードで既存のアカウントのみがサポートされています、OSC に**アカウントを作成するのにはここをクリック**を表示しないことを示すために**hideHyperlinks**と **、パスワードを忘れた?** 内のハイパーリンク、アカウントの構成] ダイアログ ボックスです。</span><span class="sxs-lookup"><span data-stu-id="6067c-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="6067c-127">XML の例</span><span class="sxs-lookup"><span data-stu-id="6067c-127">XML example</span></span>

<span data-ttu-id="6067c-128">OSC プロバイダーの XML**機能**の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6067c-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
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
  <createAccountUrl>http://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>http://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a><span data-ttu-id="6067c-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="6067c-129">See also</span></span>

- [<span data-ttu-id="6067c-130">OSC プロバイダーの XML の例</span><span class="sxs-lookup"><span data-stu-id="6067c-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="6067c-131">機能のための XML</span><span class="sxs-lookup"><span data-stu-id="6067c-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="6067c-132">友人の XML の例</span><span class="sxs-lookup"><span data-stu-id="6067c-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="6067c-133">アクティビティ フィードの XML の例</span><span class="sxs-lookup"><span data-stu-id="6067c-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="6067c-134">Outlook ソーシャル コネクタ プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="6067c-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

