---
title: アクティビティの取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: '.osc は、ソーシャルネットワークの .osc プロバイダーの機能を判断するために、imethod alprovider:: getcapabilities メソッドを呼び出します。'
ms.openlocfilehash: 9d504fb64368a6910feaa38f0ef19ed631b4d4e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420578"
---
# <a name="getting-activities"></a><span data-ttu-id="df651-103">アクティビティの取得</span><span class="sxs-lookup"><span data-stu-id="df651-103">Getting activities</span></span>

<span data-ttu-id="df651-104">.osc は、ソーシャルネットワークの .osc プロバイダーの機能を判断するために、 [imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="df651-104">The OSC calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="df651-105">返された**機能**XML の**getactivities**要素と**dynamicActivitiesLookupEx**要素が、.osc プロバイダーが必要に応じてアクティビティを取得し、アクティビティをメモリに格納していることを示している場合、.osc は次のことを行うことができます。呼び出しシーケンス。</span><span class="sxs-lookup"><span data-stu-id="df651-105">If the **getActivities** and **dynamicActivitiesLookupEx** elements in the returned **capabilities** XML indicate that the OSC provider supports getting activities on demand and storing activities in memory, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="df651-106">また、.osc は、 **capabilities** XML の**hashfunction**要素で指定されているハッシュ関数についても注意してください。</span><span class="sxs-lookup"><span data-stu-id="df651-106">The OSC also notes the hash function specified in the **hashFunction** element in the **capabilities** XML.</span></span> <span data-ttu-id="df651-107">.osc は、ソーシャルネットワーク上の友人および友人以外のアクティビティと情報 (isocial [alperson](isocialpersoniunknown.md)インターフェイスでサポートされる) を取得するために、次のシーケンスのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="df651-107">The OSC calls methods in the following sequence to get activities and information (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends and non-friends on the social network:</span></span> 
  
1. <span data-ttu-id="df651-108">[iGetLoggedOnUser alsession::](isocialsession-getloggedonuser.md) —認証プロセスの最後に、.osc が**GetLoggedOnUser**を呼び出して、認証されているユーザーの[i alprofile](isocialprofileisocialperson.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="df651-108">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —At the end of the authentication process, the OSC calls **GetLoggedOnUser** to obtain an [ISocialProfile](isocialprofileisocialperson.md) interface for the user being authenticated.</span></span> <span data-ttu-id="df651-109">認証の詳細については、「[基本認証](basic-authentication.md)」および「[フォームベース認証](forms-based-authentication.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df651-109">For more information on authentication, see [Basic Authentication](basic-authentication.md) and [Forms-Based Authentication](forms-based-authentication.md).</span></span>
    
2. <span data-ttu-id="df651-110">[ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) — [Outlook People] ウィンドウに表示されている人の場合、このアクティビティは SMTP アドレスを取得してハッシュし、 **ISocialSession2::::: GetActivitiesEx**、およびストア (メモリ) を呼び出します。返されるアクティビティデータこれらの人物。</span><span class="sxs-lookup"><span data-stu-id="df651-110">[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) —For the persons displayed in the Outlook People Pane, the OSC obtains and hashes their SMTP addresses, calls **ISocialSession2::GetActivitiesEx**, and stores (in memory) the activities data returned for these persons.</span></span> <span data-ttu-id="df651-111">.osc は、出力パラメーター [_アクティビティ_] を取得します。これは、ログオンしているユーザーのフレンドのアクティビティのコレクションを含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="df651-111">The OSC gets in an output parameter,  _activities_, which is a string that contains a collection of activities for friends of the logged-on user.</span></span> <span data-ttu-id="df651-112">この文字列は、 **activityfeed**要素のスキーマ定義に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="df651-112">This string conforms to the schema definition for the **activityFeed** element.</span></span> 
    
3. <span data-ttu-id="df651-113">[iGetActivitiesEx alsession:: getperson](isocialsession-getperson.md) — \*\*\*\* によって返される**activitydetails** XML 内の各**activitydetails**要素に、そのアクティビティを所有しているユーザーを示す**ownerID**要素があります。</span><span class="sxs-lookup"><span data-stu-id="df651-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each **activityDetails** element in the **activityFeed** XML returned by **GetActivitiesEx**, there is an **ownerID** element that indicates the person who owns that activity.</span></span> <span data-ttu-id="df651-114">.osc は、その**ownerID**値を使用して**getperson**を呼び出し、その人物の**i alperson**インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="df651-114">The OSC uses that **ownerID** value to call **GetPerson** to get an **ISocialPerson** interface for that person.</span></span> 
    
4. <span data-ttu-id="df651-115">[ichanged alperson:: getdetails](isocialperson-getdetails.md) —手順3で取得した**i指定 alperson**オブジェクトに基づき、.osc は**getdetails**を呼び出して、その人物 (名や姓など) の詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="df651-115">[ISocialPerson::GetDetails](isocialperson-getdetails.md) —Based on the **ISocialPerson** object obtained from step 3, the OSC calls **GetDetails** to get details for that person, such as the first name and last name.</span></span> <span data-ttu-id="df651-116">この .osc は、手順2で**GetActivitiesEx**によって返される**activitydetails** XML の**activitydetails**要素で指定されている各アクティビティに対して同じ操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="df651-116">The OSC can do the same for each activity specified in an **activityDetails** element in the **activityFeed** XML returned by **GetActivitiesEx** in step 2.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="df651-117">.osc は、アクティビティキャッシュを既定の間隔で更新します。</span><span class="sxs-lookup"><span data-stu-id="df651-117">The OSC refreshes the activities cache at a default interval.</span></span> <span data-ttu-id="df651-118">アクティビティキャッシュの更新の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df651-118">For more information about refreshing the activities cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df651-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="df651-119">See also</span></span>

- [<span data-ttu-id="df651-120">機能の XML</span><span class="sxs-lookup"><span data-stu-id="df651-120">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="df651-121">通常の呼び出しシーケンスの .osc</span><span class="sxs-lookup"><span data-stu-id="df651-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

