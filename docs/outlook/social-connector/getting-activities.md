---
title: 活動を取得します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: OSC では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する ISocialProvider::GetCapabilities メソッドを呼び出します。
ms.openlocfilehash: 82bb5322118fa3ebd7610f56b8f34ae95b59a40f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804332"
---
# <a name="getting-activities"></a><span data-ttu-id="7e916-103">活動を取得します。</span><span class="sxs-lookup"><span data-stu-id="7e916-103">Getting activities</span></span>

<span data-ttu-id="7e916-104">OSC では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7e916-104">The OSC calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="7e916-105">**GetActivities**と**dynamicActivitiesLookupEx** **機能**の返された XML 要素では、OSC プロバイダーが要求と活動をメモリに格納することで取得の活動をサポートしていることを示す、OSC、次のことができます。呼び出しシーケンスです。</span><span class="sxs-lookup"><span data-stu-id="7e916-105">If the **getActivities** and **dynamicActivitiesLookupEx** elements in the returned **capabilities** XML indicate that the OSC provider supports getting activities on demand and storing activities in memory, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="7e916-106">OSC では、ハッシュ関数を**実装しています。** 要素で XML の**機能**を指定もメモします。</span><span class="sxs-lookup"><span data-stu-id="7e916-106">The OSC also notes the hash function specified in the **hashFunction** element in the **capabilities** XML.</span></span> <span data-ttu-id="7e916-107">OSC では、活動と情報を取得 ( [ISocialPerson](isocialpersoniunknown.md)インターフェイスでサポートされている)、ソーシャル ネットワーク上の非友人や友人を次の順序でメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7e916-107">The OSC calls methods in the following sequence to get activities and information (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends and non-friends on the social network:</span></span> 
  
1. <span data-ttu-id="7e916-108">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) -、OSC は認証プロセスの最後に、ユーザーが認証されるための[ISocialProfile](isocialprofileisocialperson.md)インターフェイスを取得するのには**GetLoggedOnUser**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7e916-108">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —At the end of the authentication process, the OSC calls **GetLoggedOnUser** to obtain an [ISocialProfile](isocialprofileisocialperson.md) interface for the user being authenticated.</span></span> <span data-ttu-id="7e916-109">認証の詳細については、[基本認証](basic-authentication.md)と[フォーム ベース認証](forms-based-authentication.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e916-109">For more information on authentication, see [Basic Authentication](basic-authentication.md) and [Forms-Based Authentication](forms-based-authentication.md).</span></span>
    
2. <span data-ttu-id="7e916-110">[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) -、OSC を取得 Outlook 人物情報ウィンドウに表示されている担当者、およびに返されたハッシュの SMTP アドレスを**ISocialSession2::GetActivitiesEx**を呼び出して、(メモリ内) のアクティビティ データを格納します。これらの担当者。</span><span class="sxs-lookup"><span data-stu-id="7e916-110">[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) —For the persons displayed in the Outlook People Pane, the OSC obtains and hashes their SMTP addresses, calls **ISocialSession2::GetActivitiesEx**, and stores (in memory) the activities data returned for these persons.</span></span> <span data-ttu-id="7e916-111">OSC は、_アクティビティ_、ログオン中のユーザーの友人の活動のコレクションを格納する文字列には、出力パラメーターを取得します。</span><span class="sxs-lookup"><span data-stu-id="7e916-111">The OSC gets in an output parameter,  _activities_, which is a string that contains a collection of activities for friends of the logged-on user.</span></span> <span data-ttu-id="7e916-112">この文字列は、 **activityFeed**要素のスキーマ定義に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="7e916-112">This string conforms to the schema definition for the **activityFeed** element.</span></span> 
    
3. <span data-ttu-id="7e916-113">[ISocialSession::GetPerson](isocialsession-getperson.md) - **activityFeed** **GetActivitiesEx**から返された XML 内の**activityDetails**要素ごとには、その活動を所有する人物の**ownerID**要素です。</span><span class="sxs-lookup"><span data-stu-id="7e916-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each **activityDetails** element in the **activityFeed** XML returned by **GetActivitiesEx**, there is an **ownerID** element that indicates the person who owns that activity.</span></span> <span data-ttu-id="7e916-114">OSC では、その**ownerID**値を使用して、その人の**ISocialPerson**インターフェイスを取得するのには**GetPerson**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7e916-114">The OSC uses that **ownerID** value to call **GetPerson** to get an **ISocialPerson** interface for that person.</span></span> 
    
4. <span data-ttu-id="7e916-115">[ISocialPerson::GetDetails](isocialperson-getdetails.md) -、OSC 3 のステップから取得された**ISocialPerson**オブジェクトに基づき、名、姓、名など、その人の詳細を取得する**GetDetails**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7e916-115">[ISocialPerson::GetDetails](isocialperson-getdetails.md) —Based on the **ISocialPerson** object obtained from step 3, the OSC calls **GetDetails** to get details for that person, such as the first name and last name.</span></span> <span data-ttu-id="7e916-116">OSC **activityFeed**手順 2 で、 **GetActivitiesEx**から返された XML 内の**activityDetails**要素で指定されているそれぞれのアクティビティで同じことが行えます。</span><span class="sxs-lookup"><span data-stu-id="7e916-116">The OSC can do the same for each activity specified in an **activityDetails** element in the **activityFeed** XML returned by **GetActivitiesEx** in step 2.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="7e916-117">OSC では、既定の間隔で活動のキャッシュを更新します。</span><span class="sxs-lookup"><span data-stu-id="7e916-117">The OSC refreshes the activities cache at a default interval.</span></span> <span data-ttu-id="7e916-118">活動キャッシュの更新の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e916-118">For more information about refreshing the activities cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7e916-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="7e916-119">See also</span></span>

- [<span data-ttu-id="7e916-120">機能のための XML</span><span class="sxs-lookup"><span data-stu-id="7e916-120">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="7e916-121">OSC の典型的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="7e916-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

