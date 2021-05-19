---
title: アクティビティの取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: OSC は ISocialProvider::GetCapabilities メソッドを呼び出して、ソーシャル ネットワークの OSC プロバイダーの機能を決定します。
ms.openlocfilehash: 9d504fb64368a6910feaa38f0ef19ed631b4d4e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420578"
---
# <a name="getting-activities"></a><span data-ttu-id="6b5c2-103">アクティビティの取得</span><span class="sxs-lookup"><span data-stu-id="6b5c2-103">Getting activities</span></span>

<span data-ttu-id="6b5c2-104">OSC は [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) メソッドを呼び出して、ソーシャル ネットワークの OSC プロバイダーの機能を決定します。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-104">The OSC calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="6b5c2-105">返される機能 XML の **getActivities** 要素と **dynamicActivitiesLookupEx** 要素 **が、OSC** プロバイダーがオンデマンドでアクティビティを取得し、アクティビティをメモリに格納するサポートを示している場合、OSC は次の呼び出しシーケンスを実行できます。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-105">If the **getActivities** and **dynamicActivitiesLookupEx** elements in the returned **capabilities** XML indicate that the OSC provider supports getting activities on demand and storing activities in memory, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="6b5c2-106">OSC は、機能 XML の **hashFunction** 要素で指定されたハッシュ **関数もメモします** 。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-106">The OSC also notes the hash function specified in the **hashFunction** element in the **capabilities** XML.</span></span> <span data-ttu-id="6b5c2-107">OSC は、次の順序でメソッドを呼び出して、ソーシャル ネットワーク上の友人や友人以外のアクティビティと情報を取得します [(ISocialPerson](isocialpersoniunknown.md) インターフェイスでサポートされています)。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-107">The OSC calls methods in the following sequence to get activities and information (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends and non-friends on the social network:</span></span> 
  
1. <span data-ttu-id="6b5c2-108">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —認証プロセスの最後に、OSC は **GetLoggedOnUser** を呼び出して、認証されるユーザーの [ISocialProfile](isocialprofileisocialperson.md) インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-108">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —At the end of the authentication process, the OSC calls **GetLoggedOnUser** to obtain an [ISocialProfile](isocialprofileisocialperson.md) interface for the user being authenticated.</span></span> <span data-ttu-id="6b5c2-109">認証の詳細については [、「Basic Authentication and](basic-authentication.md) [Forms-Based Authentication」を参照してください](forms-based-authentication.md)。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-109">For more information on authentication, see [Basic Authentication](basic-authentication.md) and [Forms-Based Authentication](forms-based-authentication.md).</span></span>
    
2. <span data-ttu-id="6b5c2-110">[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) —Outlook People Pane に表示されるユーザーの場合、OSC は SMTP アドレスを取得してハッシュし **、ISocialSession2::GetActivitiesEx** を呼び出し、これらのユーザーに対して返されるアクティビティ データを (メモリ内に) 格納します。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-110">[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) —For the persons displayed in the Outlook People Pane, the OSC obtains and hashes their SMTP addresses, calls **ISocialSession2::GetActivitiesEx**, and stores (in memory) the activities data returned for these persons.</span></span> <span data-ttu-id="6b5c2-111">OSC は、ログオンしているユーザーの友人のアクティビティのコレクションを含む文字列である出力パラメーター activities を取得します。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-111">The OSC gets in an output parameter,  _activities_, which is a string that contains a collection of activities for friends of the logged-on user.</span></span> <span data-ttu-id="6b5c2-112">この文字列は **、activityFeed** 要素のスキーマ定義に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-112">This string conforms to the schema definition for the **activityFeed** element.</span></span> 
    
3. <span data-ttu-id="6b5c2-113">[ISocialSession::GetPerson](isocialsession-getperson.md) **—GetActivitiesEx** によって返される **activityFeed** XML の **activityDetails** 要素ごとに、そのアクティビティを所有するユーザーを示す **ownerID** 要素があります。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each **activityDetails** element in the **activityFeed** XML returned by **GetActivitiesEx**, there is an **ownerID** element that indicates the person who owns that activity.</span></span> <span data-ttu-id="6b5c2-114">OSC は、 **その ownerID 値** を使用して **GetPerson** を呼び出して、そのユーザー **の ISocialPerson** インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-114">The OSC uses that **ownerID** value to call **GetPerson** to get an **ISocialPerson** interface for that person.</span></span> 
    
4. <span data-ttu-id="6b5c2-115">[ISocialPerson::GetDetails](isocialperson-getdetails.md) —手順 3 から取得した **ISocialPerson** オブジェクトに基づいて、OSC は **GetDetails** を呼び出して、名や名など、その人物の詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-115">[ISocialPerson::GetDetails](isocialperson-getdetails.md) —Based on the **ISocialPerson** object obtained from step 3, the OSC calls **GetDetails** to get details for that person, such as the first name and last name.</span></span> <span data-ttu-id="6b5c2-116">OSC は、手順 2 の **GetActivitiesEx** によって返される **activityFeed** XML の **activityDetails** 要素で指定されたアクティビティごとに同じ操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-116">The OSC can do the same for each activity specified in an **activityDetails** element in the **activityFeed** XML returned by **GetActivitiesEx** in step 2.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="6b5c2-117">OSC は、既定の間隔でアクティビティ キャッシュを更新します。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-117">The OSC refreshes the activities cache at a default interval.</span></span> <span data-ttu-id="6b5c2-118">アクティビティ キャッシュの更新の詳細については、「友人とアクティビティの [同期」を参照してください](synchronizing-friends-and-activities.md)。</span><span class="sxs-lookup"><span data-stu-id="6b5c2-118">For more information about refreshing the activities cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b5c2-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b5c2-119">See also</span></span>

- [<span data-ttu-id="6b5c2-120">機能の XML</span><span class="sxs-lookup"><span data-stu-id="6b5c2-120">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="6b5c2-121">OSC の一般的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="6b5c2-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

