---
title: アクティビティ用 XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: このトピックには、アクティビティ情報を取得するために、.osc プロバイダーが実装する Outlook Social Connector (.osc) プロバイダーの機能拡張 API 呼び出しを示すシナリオの例が含まれています。 情報は、.osc プロバイダ xml スキーマに準拠する xml 文字列で表されます。
ms.openlocfilehash: a4f1c6ce1f33b59811f6a6fecb737cd1f737946b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409630"
---
# <a name="xml-for-activities"></a><span data-ttu-id="fe3de-104">アクティビティ用 XML</span><span class="sxs-lookup"><span data-stu-id="fe3de-104">XML for activities</span></span>

<span data-ttu-id="fe3de-105">このトピックには、アクティビティ情報を取得するために、.osc プロバイダーが実装する Outlook Social Connector (.osc) プロバイダーの機能拡張 API 呼び出しを示すシナリオの例が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fe3de-105">This topic contains an example scenario that shows the Outlook Social Connector (OSC) provider extensibility API calls that an OSC provider implements and the OSC makes to obtain activities information.</span></span> <span data-ttu-id="fe3de-106">情報は、.osc プロバイダ xml スキーマに準拠する xml 文字列で表されます。</span><span class="sxs-lookup"><span data-stu-id="fe3de-106">Information is expressed in XML strings that conform to the OSC provider XML schema.</span></span>
  
<span data-ttu-id="fe3de-107">.osc プロバイダ XML スキーマを使用すると、.osc プロバイダーはアクティビティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="fe3de-107">The OSC provider XML schema allows an OSC provider to define activities.</span></span> <span data-ttu-id="fe3de-108">アクティビティ情報には、アクティビティフィードアイテムが送信されたソーシャルネットワーク、各アクティビティフィードアイテムの詳細 (アクティビティの所有者、種類、発行日など)、およびアクティビティを表示するためのテンプレートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fe3de-108">Activity information can include the social network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> <span data-ttu-id="fe3de-109">ユーザーウィンドウまたは連絡先カードでのアクティビティの表示をサポートするには、ソーシャルネットワークの .osc プロバイダーが適切なアクティビティ XML を実装して返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe3de-109">To support showing activities on the People Pane or Contact Card, a social network's OSC provider must implement and return the correct activities XML.</span></span> <span data-ttu-id="fe3de-110">アクティビティフィード xml の例については、「[アクティビティフィード xml の例](activity-feed-xml-example.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe3de-110">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span> <span data-ttu-id="fe3de-111">フレンドのアクティビティの同期の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe3de-111">For more information about synchronizing friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> <span data-ttu-id="fe3de-112">必要な要素やオプションの要素を含む、.osc プロバイダ XML スキーマの完全な定義については、「 [Outlook Social Connector プロバイダーの xml スキーマ](outlook-social-connector-provider-xml-schema.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe3de-112">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span> 
  
<span data-ttu-id="fe3de-113">次のシナリオでは、[人] ウィンドウで選択したユーザーのアクティビティを、.osc が動的に同期し、その人物に関する詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="fe3de-113">In the following scenario, the OSC dynamically synchronizes activities for a person selected in the People Pane, and gets details about that person:</span></span>
  
1. <span data-ttu-id="fe3de-114">アクティビティのオンデマンド同期をサポートする .osc プロバイダーは、getactivities 要素と**dynamicActivitiesLookupEx**要素を使用\*\*\*\* して、.osc に対してを指定します。</span><span class="sxs-lookup"><span data-stu-id="fe3de-114">An OSC provider that supports on-demand synchronization of activities indicates that to the OSC by using the **getActivities** and **dynamicActivitiesLookupEx** elements.</span></span> <span data-ttu-id="fe3de-115">.osc プロバイダーは、 **hashfunction**要素も設定します。</span><span class="sxs-lookup"><span data-stu-id="fe3de-115">The OSC provider also sets the **hashFunction** element.</span></span> <span data-ttu-id="fe3de-116">3つすべての要素は、**機能**の子要素です。</span><span class="sxs-lookup"><span data-stu-id="fe3de-116">All three elements are child elements of **capabilities**.</span></span> 
    
2. <span data-ttu-id="fe3de-117">.osc プロバイダーは、 **iISocialSession2 alprovider:: getcapabilities**メソッドと[:: GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="fe3de-117">The OSC provider implements the **ISocialProvider::GetCapabilities** and [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) methods.</span></span> 
    
3. <span data-ttu-id="fe3de-118">.osc は**idynamicActivitiesLookupEx alprovider:: getcapabilities**を呼び出して、.osc プロバイダー \*\*\*\* がアクティビティの\*\*\*\* オンデマンド同期をサポートしているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="fe3de-118">The OSC calls **ISocialProvider::GetCapabilities** to check the value of **getActivities** and **dynamicActivitiesLookupEx** to verify that the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="fe3de-119">.osc は、.osc プロバイダーでサポートされている**hashfunction**要素の値もメモします。</span><span class="sxs-lookup"><span data-stu-id="fe3de-119">The OSC also notes the value of the **hashFunction** element supported by the OSC provider.</span></span> 
    
4. <span data-ttu-id="fe3de-120">.osc は、ユーザーウィンドウまたは連絡先カードを更新して、選択されている人物の最新のアクティビティをユーザーに表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="fe3de-120">The OSC refreshes the People Pane or Contact Card to let the user see the latest activities of the selected person.</span></span> <span data-ttu-id="fe3de-121">.osc は、 **hashfunction**要素で指定されたハッシュ関数を使用して、その人物の SMTP アドレスを暗号化し、 **hashedAddresses**要素の xml スキーマ定義に準拠した xml 文字列を形成します。</span><span class="sxs-lookup"><span data-stu-id="fe3de-121">The OSC encrypts the person's SMTP address by using the hash function specified in the **hashFunction** element, forming an XML string that conforms to the XML schema definition for the **hashedAddresses** element.</span></span> 
    
5. <span data-ttu-id="fe3de-122">.osc は**ISocialSession2:: GetActivitiesEx**を呼び出して、ハッシュ化されたアドレスのこの XML 文字列を_hashedAddresses_パラメーターとして提供し、その人物の現在のアクティビティのコレクションを_交際_パラメーターで取得します。</span><span class="sxs-lookup"><span data-stu-id="fe3de-122">The OSC calls **ISocialSession2::GetActivitiesEx**, providing this XML string of the hashed address as the  _hashedAddresses_ parameter, to get a current collection of activities for that person in the  _activities_ parameter.</span></span> <span data-ttu-id="fe3de-123">_アクティビティ_パラメーター文字列は、 **activityfeed**要素の XML スキーマ定義に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="fe3de-123">The  _activities_ parameter string complies with the XML schema definition of the **activityFeed** element.</span></span> 
    
6. <span data-ttu-id="fe3de-124">アクティビティ**フィード**の XML スキーマ定義に基づいて、_アクティビティ_文字列をさらに解析して、各アクティビティに関する型、発行日、その他の情報を見つけ、アクティビティを表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="fe3de-124">Based on the XML schema definition for **activityFeed**, the OSC further parses the  _activities_ string to find out the type, publish date, and other information about each activity, and how to display the activity.</span></span> 
    
7. <span data-ttu-id="fe3de-125">選択した人物に関する詳細を取得するために、.osc は[ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)を呼び出し、ハッシュされたアドレスの同じ XML 文字列を、_個人_情報パラメーターの引数として提供します。</span><span class="sxs-lookup"><span data-stu-id="fe3de-125">To get details about the selected person, the OSC calls [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md), providing the same XML string of hashed addresses as the argument for the  _personsAddresses_ parameter.</span></span> <span data-ttu-id="fe3de-126">個人に関する詳細は、個人_コレクション_パラメーターで返されます。</span><span class="sxs-lookup"><span data-stu-id="fe3de-126">The details about the person are returned in the  _personsCollection_ parameter.</span></span> <span data-ttu-id="fe3de-127">これらの詳細には、 **firstName**、 **lastName**、 **emailAddress**を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="fe3de-127">These details can include **firstName**, **lastName**, and **emailAddress**.</span></span> <span data-ttu-id="fe3de-128">個人_コレクション_パラメーターは、 **person**要素の XML スキーマ定義に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="fe3de-128">The  _personsCollection_ parameter conforms to the XML schema definition for the **person** element.</span></span> 
    
<span data-ttu-id="fe3de-129">アクティビティの XML を指定する方法の詳細については、このセクションの次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe3de-129">You can find more information about specifying XML for activities in the following topics of this section:</span></span>
  
- [<span data-ttu-id="fe3de-130">アクティビティフィードアイテムの XML の概要</span><span class="sxs-lookup"><span data-stu-id="fe3de-130">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="fe3de-131">activitydetails 要素</span><span class="sxs-lookup"><span data-stu-id="fe3de-131">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="fe3de-132">activitytemplatecontainer 要素</span><span class="sxs-lookup"><span data-stu-id="fe3de-132">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="fe3de-133">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="fe3de-133">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="fe3de-134">アクティビティを適切に表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="fe3de-134">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a><span data-ttu-id="fe3de-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe3de-135">See also</span></span>

- [<span data-ttu-id="fe3de-136">アクティビティフィード XML の例</span><span class="sxs-lookup"><span data-stu-id="fe3de-136">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="fe3de-137">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="fe3de-137">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="fe3de-138">機能の XML</span><span class="sxs-lookup"><span data-stu-id="fe3de-138">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="fe3de-139">Friends の XML</span><span class="sxs-lookup"><span data-stu-id="fe3de-139">XML for Friends</span></span>](xml-for-friends.md)
- [<span data-ttu-id="fe3de-140">.osc XML スキーマを使用してプロバイダーを開発する</span><span class="sxs-lookup"><span data-stu-id="fe3de-140">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

