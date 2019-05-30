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
# <a name="capabilities-xml-example"></a><span data-ttu-id="bc9bc-104">機能 XML の例</span><span class="sxs-lookup"><span data-stu-id="bc9bc-104">Capabilities XML example</span></span>

<span data-ttu-id="bc9bc-105">このトピックの XML の例は、ソーシャルネットワークの[Imethod Alprovider:: GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出すと、Outlook Social CONNECTOR (.osc) に返される xml 文字列です。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="bc9bc-106">XML は、.OSC プロバイダーが、.OSC の機能と要件を指定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="bc9bc-107">フレンドの機能</span><span class="sxs-lookup"><span data-stu-id="bc9bc-107">Capabilities for friends</span></span>

<span data-ttu-id="bc9bc-108">この例では、.OSC プロバイダーは、フレンド機能をサポートする機能を示す次の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="bc9bc-109">\*\*\*\* .osc プロバイダーが[iGetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)メソッドをサポートして、プログラムによって友人の情報を取得するように指定するには、 **true**として取得します。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="bc9bc-110">Outlook の連絡先フォルダー内のフレンドの情報のキャッシュをサポートする場合は、 **cacheFriends**を**true**にします。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="bc9bc-111">**Contactsyncrestartinterval**を60として、エラーが発生した場合、.osc は60分ごとにキャッシュの更新を再試行する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="bc9bc-112">**ユーザー**がソーシャルネットワークにフレンドを追加する機能を示す**場合は true**にします。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="bc9bc-113">\*\*\*\* .osc クラスが、ソーシャルネットワーク上のフレンドとしてのユーザーの削除をサポートしていないことを示すため、 **false**として表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="bc9bc-114">**dynamicContactsLookup**を**false**として、.osc がフレンドの情報をメモリに格納しないように指定します。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="bc9bc-115">アクティビティの機能</span><span class="sxs-lookup"><span data-stu-id="bc9bc-115">Capabilities for activities</span></span>

<span data-ttu-id="bc9bc-116">.OSC プロバイダーは、アクティビティをサポートする機能を示す次の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="bc9bc-117">プログラムによってフレンドのアクティビティを取得するために、.OSC プロバイダーが[IGetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md)メソッドをサポートしていることを示すために、[ **getactivities** ] を**true**とします。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="bc9bc-118">非表示の Outlook ニュースフィードフォルダーでのフレンドの処理のキャッシュをサポートするには、 **Cacheactivities**を**false**にします。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="bc9bc-119">**dynamicActivitiesLookupEx**がフレンドのアクティビティをメモリに格納することを示すには、 **true**にします。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="bc9bc-120">認証およびアカウント構成の機能</span><span class="sxs-lookup"><span data-stu-id="bc9bc-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="bc9bc-121">.OSC プロバイダーは、認証およびアカウント構成のサポートを示すために、次の要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="bc9bc-122">.OSC プロバイダーが基本認証をサポートしていることを示すには、 **Uselogonwebauth**を**false**として指定します。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="bc9bc-123">**supportsAutoConfigure**は、ユーザーのソーシャルネットワークへの自動的な構成およびログオンを行わないようにするため、.osc が**false**として設定されます。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="bc9bc-124">**Uselogoncached**と**hideRememberMyPassword**を**FALSE**として、.osc が毎回パスワードの入力を要求する必要があり、キャッシュされたログオン資格情報を使用してログオンしてはいけないことを示します。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="bc9bc-125">[アカウント構成] ダイアログボックスで、.OSC がソーシャルネットワークの URL を表示しないようにするには、 **Displayurl**を**false**として指定します。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="bc9bc-126">**Hidehyperlinks**を**false**に設定して、.osc プロバイダーが既知のパスワードを持つ既存のアカウントのみをサポートすることを示す場合、 **[ここをクリック**してアカウントを作成し、**パスワードを忘れますか?** ] のハイパーリンクを表示しないようにします。[アカウントの構成] ダイアログボックス</span><span class="sxs-lookup"><span data-stu-id="bc9bc-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="bc9bc-127">XML の例</span><span class="sxs-lookup"><span data-stu-id="bc9bc-127">XML example</span></span>

<span data-ttu-id="bc9bc-128">次の例は、.OSC プロバイダーの**機能**XML を示しています。</span><span class="sxs-lookup"><span data-stu-id="bc9bc-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="bc9bc-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="bc9bc-129">See also</span></span>

- [<span data-ttu-id="bc9bc-130">.OSC プロバイダーの XML の例</span><span class="sxs-lookup"><span data-stu-id="bc9bc-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="bc9bc-131">機能の XML</span><span class="sxs-lookup"><span data-stu-id="bc9bc-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="bc9bc-132">Friends XML の例</span><span class="sxs-lookup"><span data-stu-id="bc9bc-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="bc9bc-133">アクティビティフィード XML の例</span><span class="sxs-lookup"><span data-stu-id="bc9bc-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="bc9bc-134">Outlook Social Connector プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="bc9bc-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

