---
title: 機能 XML の例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: このトピックの XML の例は、ソーシャル ネットワークの ISocialProvider::GetCapabilities メソッドを呼び出した後、Outlook Social Connector (OSC) に返される XML 文字列です。 XML は、OSC プロバイダーが OSC の機能と要件を指定する方法を示しています。
ms.openlocfilehash: 3340f5b1e0718edd1a062ab817c6621c338bee42
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542262"
---
# <a name="capabilities-xml-example"></a><span data-ttu-id="e4b9e-104">機能 XML の例</span><span class="sxs-lookup"><span data-stu-id="e4b9e-104">Capabilities XML example</span></span>

<span data-ttu-id="e4b9e-105">このトピックの XML の例は、ソーシャル ネットワークの[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出した後、Outlook Social Connector (OSC) に返される XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="e4b9e-106">XML は、OSC プロバイダーが OSC の機能と要件を指定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="e4b9e-107">フレンドの機能</span><span class="sxs-lookup"><span data-stu-id="e4b9e-107">Capabilities for friends</span></span>

<span data-ttu-id="e4b9e-108">この例では、OSC プロバイダーは、フレンド機能をサポートする機能を示す次の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="e4b9e-109">**getFriends** **as true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) メソッドを使用して、友人の情報をプログラムで取得します。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="e4b9e-110">**cacheFriends** を **true に** 設定すると、連絡先フォルダーに友人の情報をOutlookできます。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="e4b9e-111">**エラーが発生した場合、OSC** は 60 分ごとにキャッシュの更新を再試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="e4b9e-112">**followPerson** **を true** に設定して、ソーシャル ネットワークにフレンドを追加する機能を示します。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="e4b9e-113">**doNotFollowPerson** **を false** として指定すると、OSC プロバイダーはソーシャル ネットワーク上のフレンドとして人物の削除がサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="e4b9e-114">**dynamicContactsLookup** **を false** として指定すると、OSC はフレンドの情報をメモリに格納しなけれます。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="e4b9e-115">アクティビティの機能</span><span class="sxs-lookup"><span data-stu-id="e4b9e-115">Capabilities for activities</span></span>

<span data-ttu-id="e4b9e-116">OSC プロバイダーは、アクティビティをサポートする機能を示す次の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="e4b9e-117">**getActivities** を **true** に設定すると、OSC プロバイダーが [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) メソッドをサポートして、プログラムによってフレンドのアクティビティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="e4b9e-118">**cacheActivities を** **false** に設定して、非表示の [ニュース フィード] フォルダー内の友人のOutlookをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="e4b9e-119">**dynamicActivitiesLookupEx** **を true** として指定すると、OSC はフレンドのアクティビティをメモリに格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="e4b9e-120">認証とアカウント構成の機能</span><span class="sxs-lookup"><span data-stu-id="e4b9e-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="e4b9e-121">OSC プロバイダーは、認証とアカウント構成のサポートを示す次の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="e4b9e-122">**useLogonWebAuth** **を false として指定** すると、OSC プロバイダーが基本認証をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="e4b9e-123">osC が自動的に構成し、ユーザーのソーシャル ネットワークにログオンしようとしなけれない場合は **、false としてAutoConfigure** をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="e4b9e-124">**useLogonCached** と **hideRememberMyPassword** を **false** として指定すると、OSC は毎回パスワードの入力を求める必要があります。また、キャッシュされたログオン資格情報を使用してログオンする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="e4b9e-125">**displayUrl** を **false** として指定して、OSC がアカウント構成ダイアログ ボックスにソーシャル ネットワークの URL を表示しなかるべきかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="e4b9e-126">**hideHyperlinks** as **false** は、OSC プロバイダーが既知のパスワードを持つ既存のアカウントのみをサポートし、OSCが [アカウントを作成するにはここをクリックしてアカウントを作成する] および [パスワードを忘れた場合] ハイパーリンクをアカウント構成ダイアログ ボックスに表示しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="e4b9e-127">XML の例</span><span class="sxs-lookup"><span data-stu-id="e4b9e-127">XML example</span></span>

<span data-ttu-id="e4b9e-128">次の例は、OSC **プロバイダーの** 機能 XML を示しています。</span><span class="sxs-lookup"><span data-stu-id="e4b9e-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="e4b9e-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4b9e-129">See also</span></span>

- [<span data-ttu-id="e4b9e-130">OSC プロバイダー XML の例</span><span class="sxs-lookup"><span data-stu-id="e4b9e-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="e4b9e-131">機能の XML</span><span class="sxs-lookup"><span data-stu-id="e4b9e-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="e4b9e-132">Friends XML の例</span><span class="sxs-lookup"><span data-stu-id="e4b9e-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="e4b9e-133">アクティビティ フィード XML の例</span><span class="sxs-lookup"><span data-stu-id="e4b9e-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="e4b9e-134">Outlookソーシャル コネクタ プロバイダー XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="e4b9e-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

