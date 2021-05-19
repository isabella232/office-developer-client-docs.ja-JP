---
title: アクティビティ用 XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: このトピックでは、OSC プロバイダーが実装する Outlook Social Connector (OSC) プロバイダー拡張 API 呼び出しと、OSC がアクティビティ情報を取得するために行う呼び出しを示すシナリオの例を示します。 情報は、OSC プロバイダー XML スキーマに準拠した XML 文字列で表されます。
ms.openlocfilehash: a4f1c6ce1f33b59811f6a6fecb737cd1f737946b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409630"
---
# <a name="xml-for-activities"></a><span data-ttu-id="c5bb8-104">アクティビティ用 XML</span><span class="sxs-lookup"><span data-stu-id="c5bb8-104">XML for activities</span></span>

<span data-ttu-id="c5bb8-105">このトピックでは、OSC プロバイダーが実装する Outlook Social Connector (OSC) プロバイダー拡張 API 呼び出しと、OSC がアクティビティ情報を取得するために行う呼び出しを示すシナリオの例を示します。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-105">This topic contains an example scenario that shows the Outlook Social Connector (OSC) provider extensibility API calls that an OSC provider implements and the OSC makes to obtain activities information.</span></span> <span data-ttu-id="c5bb8-106">情報は、OSC プロバイダー XML スキーマに準拠した XML 文字列で表されます。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-106">Information is expressed in XML strings that conform to the OSC provider XML schema.</span></span>
  
<span data-ttu-id="c5bb8-107">OSC プロバイダーの XML スキーマを使用すると、OSC プロバイダーはアクティビティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-107">The OSC provider XML schema allows an OSC provider to define activities.</span></span> <span data-ttu-id="c5bb8-108">アクティビティ情報には、アクティビティ フィード アイテムが発生したソーシャル ネットワーク、各アクティビティ フィード アイテムの詳細 (アクティビティの所有者、種類、発行日など)、アクティビティを表示するテンプレートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-108">Activity information can include the social network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> <span data-ttu-id="c5bb8-109">People Pane または Contact Card でのアクティビティの表示をサポートするには、ソーシャル ネットワークの OSC プロバイダーが正しいアクティビティ XML を実装して返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-109">To support showing activities on the People Pane or Contact Card, a social network's OSC provider must implement and return the correct activities XML.</span></span> <span data-ttu-id="c5bb8-110">アクティビティ フィード XML の例については、「アクティビティ フィード [XML の例」を参照してください](activity-feed-xml-example.md)。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-110">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span> <span data-ttu-id="c5bb8-111">友人のアクティビティの同期の詳細については、「友人とアクティビティの同期 [」を参照してください](synchronizing-friends-and-activities.md)。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-111">For more information about synchronizing friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> <span data-ttu-id="c5bb8-112">OSC プロバイダー XML スキーマの完全な定義 (必須または省略可能な要素を含む) については、「ソーシャル コネクタ プロバイダー XML スキーマOutlook[を参照してください](outlook-social-connector-provider-xml-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-112">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span> 
  
<span data-ttu-id="c5bb8-113">次のシナリオでは、OSC は People Pane で選択されたユーザーのアクティビティを動的に同期し、そのユーザーの詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-113">In the following scenario, the OSC dynamically synchronizes activities for a person selected in the People Pane, and gets details about that person:</span></span>
  
1. <span data-ttu-id="c5bb8-114">アクティビティのオンデマンド同期をサポートする OSC プロバイダーは **、getActivities** 要素と **dynamicActivitiesLookupEx** 要素を使用して OSC に対してそれを示します。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-114">An OSC provider that supports on-demand synchronization of activities indicates that to the OSC by using the **getActivities** and **dynamicActivitiesLookupEx** elements.</span></span> <span data-ttu-id="c5bb8-115">OSC プロバイダーは **、hashFunction 要素も設定** します。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-115">The OSC provider also sets the **hashFunction** element.</span></span> <span data-ttu-id="c5bb8-116">3 つの要素はすべて、機能の子 **要素です**。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-116">All three elements are child elements of **capabilities**.</span></span> 
    
2. <span data-ttu-id="c5bb8-117">OSC プロバイダーは **、ISocialProvider::GetCapabilities** および [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-117">The OSC provider implements the **ISocialProvider::GetCapabilities** and [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) methods.</span></span> 
    
3. <span data-ttu-id="c5bb8-118">OSC は **ISocialProvider::GetCapabilities** を呼び出して **、getActivities** と **dynamicActivitiesLookupEx** の値をチェックして、OSC プロバイダーがアクティビティのオンデマンド同期をサポートしているか確認します。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-118">The OSC calls **ISocialProvider::GetCapabilities** to check the value of **getActivities** and **dynamicActivitiesLookupEx** to verify that the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="c5bb8-119">OSC は、OSC プロバイダーがサポートする **hashFunction** 要素の値もメモします。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-119">The OSC also notes the value of the **hashFunction** element supported by the OSC provider.</span></span> 
    
4. <span data-ttu-id="c5bb8-120">OSC は、ユーザー ウィンドウまたは連絡先カードを更新して、選択したユーザーの最新のアクティビティをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-120">The OSC refreshes the People Pane or Contact Card to let the user see the latest activities of the selected person.</span></span> <span data-ttu-id="c5bb8-121">OSC は **、hashFunction** 要素で指定されたハッシュ関数を使用して、そのユーザーの SMTP アドレスを暗号化し **、hashedAddresses** 要素の XML スキーマ定義に準拠する XML 文字列を形成します。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-121">The OSC encrypts the person's SMTP address by using the hash function specified in the **hashFunction** element, forming an XML string that conforms to the XML schema definition for the **hashedAddresses** element.</span></span> 
    
5. <span data-ttu-id="c5bb8-122">OSC は **ISocialSession2::GetActivitiesEx** を呼び出し、ハッシュされたアドレスのこの XML 文字列を  _hashedAddresses_ パラメーターとして提供し  _、activities_ パラメーター内のそのユーザーのアクティビティの現在のコレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-122">The OSC calls **ISocialSession2::GetActivitiesEx**, providing this XML string of the hashed address as the  _hashedAddresses_ parameter, to get a current collection of activities for that person in the  _activities_ parameter.</span></span> <span data-ttu-id="c5bb8-123">activity  _パラメーター_ 文字列は、activityFeed 要素の XML スキーマ定義 **に準拠** しています。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-123">The  _activities_ parameter string complies with the XML schema definition of the **activityFeed** element.</span></span> 
    
6. <span data-ttu-id="c5bb8-124">**activityFeed** の XML スキーマ定義に基づいて、OSC はアクティビティ文字列をさらに解析して、各アクティビティの種類、発行日、その他の情報、およびアクティビティの表示方法を確認します。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-124">Based on the XML schema definition for **activityFeed**, the OSC further parses the  _activities_ string to find out the type, publish date, and other information about each activity, and how to display the activity.</span></span> 
    
7. <span data-ttu-id="c5bb8-125">選択した人物の詳細を取得するために、OSC は [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)を呼び出し  _、personsAddresses_ パラメーターの引数と同じ XML 文字列のハッシュアドレスを提供します。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-125">To get details about the selected person, the OSC calls [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md), providing the same XML string of hashed addresses as the argument for the  _personsAddresses_ parameter.</span></span> <span data-ttu-id="c5bb8-126">ユーザーに関する詳細は  _、personsCollection パラメーターで返_ されます。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-126">The details about the person are returned in the  _personsCollection_ parameter.</span></span> <span data-ttu-id="c5bb8-127">これらの詳細には **、firstName、lastName、emailAddress\*\*\*\*を含めできます**。 </span><span class="sxs-lookup"><span data-stu-id="c5bb8-127">These details can include **firstName**, **lastName**, and **emailAddress**.</span></span> <span data-ttu-id="c5bb8-128">_personsCollection パラメーター_ は、person 要素の XML スキーマ定義に **準拠** しています。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-128">The  _personsCollection_ parameter conforms to the XML schema definition for the **person** element.</span></span> 
    
<span data-ttu-id="c5bb8-129">アクティビティの XML の指定の詳細については、このセクションの次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5bb8-129">You can find more information about specifying XML for activities in the following topics of this section:</span></span>
  
- [<span data-ttu-id="c5bb8-130">アクティビティ フィード アイテムの XML の概要</span><span class="sxs-lookup"><span data-stu-id="c5bb8-130">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="c5bb8-131">activityDetails 要素</span><span class="sxs-lookup"><span data-stu-id="c5bb8-131">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="c5bb8-132">activityTemplateContainer 要素</span><span class="sxs-lookup"><span data-stu-id="c5bb8-132">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="c5bb8-133">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="c5bb8-133">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="c5bb8-134">アクティビティを適切に表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="c5bb8-134">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a><span data-ttu-id="c5bb8-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="c5bb8-135">See also</span></span>

- [<span data-ttu-id="c5bb8-136">アクティビティ フィード XML の例</span><span class="sxs-lookup"><span data-stu-id="c5bb8-136">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="c5bb8-137">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="c5bb8-137">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="c5bb8-138">機能の XML</span><span class="sxs-lookup"><span data-stu-id="c5bb8-138">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="c5bb8-139">友人のための XML</span><span class="sxs-lookup"><span data-stu-id="c5bb8-139">XML for Friends</span></span>](xml-for-friends.md)
- [<span data-ttu-id="c5bb8-140">OSC XML スキーマを使用したプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="c5bb8-140">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

