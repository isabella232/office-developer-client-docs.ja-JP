---
title: 活動の XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: このトピックには、Outlook ソーシャル コネクタ (OSC) プロバイダーに、OSC プロバイダーを実装し、OSC では、アクティビティの情報を取得する機能拡張 API の呼び出しを表示するシナリオ例にはが含まれています。 情報は、OSC プロバイダーの XML スキーマに準拠する XML 文字列で表されます。
ms.openlocfilehash: 44f74d9e72eec3ff6da7f9967315fc9d75191584
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804475"
---
# <a name="xml-for-activities"></a><span data-ttu-id="d0c93-104">活動の XML</span><span class="sxs-lookup"><span data-stu-id="d0c93-104">XML for activities</span></span>

<span data-ttu-id="d0c93-105">このトピックには、Outlook ソーシャル コネクタ (OSC) プロバイダーに、OSC プロバイダーを実装し、OSC では、アクティビティの情報を取得する機能拡張 API の呼び出しを表示するシナリオ例にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d0c93-105">This topic contains an example scenario that shows the Outlook Social Connector (OSC) provider extensibility API calls that an OSC provider implements and the OSC makes to obtain activities information.</span></span> <span data-ttu-id="d0c93-106">情報は、OSC プロバイダーの XML スキーマに準拠する XML 文字列で表されます。</span><span class="sxs-lookup"><span data-stu-id="d0c93-106">Information is expressed in XML strings that conform to the OSC provider XML schema.</span></span>
  
<span data-ttu-id="d0c93-107">OSC プロバイダーの XML スキーマでは、アクティビティを定義するのには、OSC プロバイダーを許可します。</span><span class="sxs-lookup"><span data-stu-id="d0c93-107">The OSC provider XML schema allows an OSC provider to define activities.</span></span> <span data-ttu-id="d0c93-108">活動の情報は、ソーシャル ネットワーク アクティビティが発生した場合、アイテムをフィードごとのアクティビティ フィードのアイテムの詳細を含めることができます (などの所有者は、入力、発行とアクティビティの日付)、および活動を表示するテンプレートです。</span><span class="sxs-lookup"><span data-stu-id="d0c93-108">Activity information can include the social network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> <span data-ttu-id="d0c93-109">人物情報ウィンドウまたは連絡先カードに表示されているアクティビティをサポートするためにソーシャル ネットワークの OSC プロバイダーが実装し、正しい活動の XML を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0c93-109">To support showing activities on the People Pane or Contact Card, a social network's OSC provider must implement and return the correct activities XML.</span></span> <span data-ttu-id="d0c93-110">アクティビティの例については、フィードの XML、[アクティビティ フィードの XML の例](activity-feed-xml-example.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0c93-110">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span> <span data-ttu-id="d0c93-111">友人の活動を同期の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0c93-111">For more information about synchronizing friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> <span data-ttu-id="d0c93-112">のどの要素には、必須またはオプションを含む、OSC プロバイダーの XML スキーマの完全な定義は、 [Outlook ソーシャル コネクタ プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0c93-112">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span> 
  
<span data-ttu-id="d0c93-113">次のシナリオでは、OSC は動的に、人物情報ウィンドウで選択されているユーザーのアクティビティを同期し、そのユーザーに関する詳細情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="d0c93-113">In the following scenario, the OSC dynamically synchronizes activities for a person selected in the People Pane, and gets details about that person:</span></span>
  
1. <span data-ttu-id="d0c93-114">OSC プロバイダーのアクティビティのオン ・ デマンドの同期をサポートすることを示します、OSC に、 **getActivities**と**dynamicActivitiesLookupEx**の要素を使用しています。</span><span class="sxs-lookup"><span data-stu-id="d0c93-114">An OSC provider that supports on-demand synchronization of activities indicates that to the OSC by using the **getActivities** and **dynamicActivitiesLookupEx** elements.</span></span> <span data-ttu-id="d0c93-115">OSC プロバイダーも**実装しています。** 要素を設定します。</span><span class="sxs-lookup"><span data-stu-id="d0c93-115">The OSC provider also sets the **hashFunction** element.</span></span> <span data-ttu-id="d0c93-116">3 つすべての要素は、**機能**の子要素です。</span><span class="sxs-lookup"><span data-stu-id="d0c93-116">All three elements are child elements of **capabilities**.</span></span> 
    
2. <span data-ttu-id="d0c93-117">OSC プロバイダーは、 **ISocialProvider::GetCapabilities**メソッドと[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d0c93-117">The OSC provider implements the **ISocialProvider::GetCapabilities** and [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) methods.</span></span> 
    
3. <span data-ttu-id="d0c93-118">**GetActivities**および**dynamicActivitiesLookupEx**の値を確認するために、OSC プロバイダー OSC **ISocialProvider::GetCapabilities**の呼び出しには、活動のオン ・ デマンドの同期がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d0c93-118">The OSC calls **ISocialProvider::GetCapabilities** to check the value of **getActivities** and **dynamicActivitiesLookupEx** to verify that the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="d0c93-119">OSC では、OSC プロバイダーでサポートされている**実装しています。** 要素の値もメモします。</span><span class="sxs-lookup"><span data-stu-id="d0c93-119">The OSC also notes the value of the **hashFunction** element supported by the OSC provider.</span></span> 
    
4. <span data-ttu-id="d0c93-120">OSC では、ユーザーが選択したユーザーの最新の活動を確認できるようにするには、人物情報ウィンドウまたは連絡先カードを更新します。</span><span class="sxs-lookup"><span data-stu-id="d0c93-120">The OSC refreshes the People Pane or Contact Card to let the user see the latest activities of the selected person.</span></span> <span data-ttu-id="d0c93-121">OSC は、 **hashedAddresses**要素の XML スキーマ定義に準拠する XML 文字列を形成する、**実装しています。** 要素で指定されているハッシュ関数を使用してユーザーの SMTP アドレスを暗号化します。</span><span class="sxs-lookup"><span data-stu-id="d0c93-121">The OSC encrypts the person's SMTP address by using the hash function specified in the **hashFunction** element, forming an XML string that conforms to the XML schema definition for the **hashedAddresses** element.</span></span> 
    
5. <span data-ttu-id="d0c93-122">OSC では、 **ISocialSession2::GetActivitiesEx**、 _hashedAddresses_のパラメーターとして、ハッシュ化されたアドレスの場合は、この XML 文字列を提供する_活動_のパラメーターでは、その人の活動の現在のコレクションを取得するを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d0c93-122">The OSC calls **ISocialSession2::GetActivitiesEx**, providing this XML string of the hashed address as the  _hashedAddresses_ parameter, to get a current collection of activities for that person in the  _activities_ parameter.</span></span> <span data-ttu-id="d0c93-123">_アクティビティ_パラメーター文字列は、 **activityFeed**要素の XML スキーマ定義に準拠します。</span><span class="sxs-lookup"><span data-stu-id="d0c93-123">The  _activities_ parameter string complies with the XML schema definition of the **activityFeed** element.</span></span> 
    
6. <span data-ttu-id="d0c93-124">**ActivityFeed**の XML スキーマ定義に基づき、OSC をさらには、型を調べるには、日付、およびそれぞれの活動に関するその他の情報およびアクティビティを表示する方法を公開_活動_文字列を解析します。</span><span class="sxs-lookup"><span data-stu-id="d0c93-124">Based on the XML schema definition for **activityFeed**, the OSC further parses the  _activities_ string to find out the type, publish date, and other information about each activity, and how to display the activity.</span></span> 
    
7. <span data-ttu-id="d0c93-125">OSC は、選択したユーザーに関する詳細情報を取得するには、 [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)、 _personsAddresses_パラメーターの引数として、同じ XML 文字列をハッシュ化されたアドレスを提供することを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d0c93-125">To get details about the selected person, the OSC calls [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md), providing the same XML string of hashed addresses as the argument for the  _personsAddresses_ parameter.</span></span> <span data-ttu-id="d0c93-126">_PersonsCollection_パラメーターでは、ユーザーに関する詳細な情報が返されます。</span><span class="sxs-lookup"><span data-stu-id="d0c93-126">The details about the person are returned in the  _personsCollection_ parameter.</span></span> <span data-ttu-id="d0c93-127">これらの詳細については、**姓****姓**、および**emailAddress**を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d0c93-127">These details can include **firstName**, **lastName**, and **emailAddress**.</span></span> <span data-ttu-id="d0c93-128">_PersonsCollection_パラメーターは、**人**の要素の XML スキーマ定義に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="d0c93-128">The  _personsCollection_ parameter conforms to the XML schema definition for the **person** element.</span></span> 
    
<span data-ttu-id="d0c93-129">アクティビティのこのセクションの以下のトピックで、XML を指定する方法の詳細をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d0c93-129">You can find more information about specifying XML for activities in the following topics of this section:</span></span>
  
- [<span data-ttu-id="d0c93-130">フィード アイテムの活動項目の XML の概要</span><span class="sxs-lookup"><span data-stu-id="d0c93-130">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="d0c93-131">activityDetails 要素</span><span class="sxs-lookup"><span data-stu-id="d0c93-131">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="d0c93-132">activityTemplateContainer 要素</span><span class="sxs-lookup"><span data-stu-id="d0c93-132">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="d0c93-133">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="d0c93-133">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="d0c93-134">アクティビティを正しく表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="d0c93-134">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a><span data-ttu-id="d0c93-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="d0c93-135">See also</span></span>

- [<span data-ttu-id="d0c93-136">アクティビティ フィードの XML の例</span><span class="sxs-lookup"><span data-stu-id="d0c93-136">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="d0c93-137">友人や活動を同期します。</span><span class="sxs-lookup"><span data-stu-id="d0c93-137">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="d0c93-138">機能のための XML</span><span class="sxs-lookup"><span data-stu-id="d0c93-138">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="d0c93-139">友人の XML</span><span class="sxs-lookup"><span data-stu-id="d0c93-139">XML for Friends</span></span>](xml-for-friends.md)
- [<span data-ttu-id="d0c93-140">OSC の XML スキーマを使用してプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="d0c93-140">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

