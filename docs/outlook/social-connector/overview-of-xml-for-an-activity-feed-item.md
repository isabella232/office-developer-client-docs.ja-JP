---
title: アクティビティ フィード アイテムのための XML の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: アクティビティフィードは、ソーシャルネットワーク上で発生する1つ以上のアクティビティで構成されます。 各アクティビティフィードは activityfeed 要素で表され、次の3つの情報によって特徴付けられます。
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439948"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="77c99-104">アクティビティ フィード アイテムのための XML の概要</span><span class="sxs-lookup"><span data-stu-id="77c99-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="77c99-105">アクティビティフィードは、ソーシャルネットワーク上で発生する1つ以上のアクティビティで構成されます。</span><span class="sxs-lookup"><span data-stu-id="77c99-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="77c99-106">各アクティビティフィードは**activityfeed**要素で表され、次の3つの情報によって特徴付けられます。</span><span class="sxs-lookup"><span data-stu-id="77c99-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="77c99-107">**network**—アクティビティが開始されたソーシャルネットワークの名前。</span><span class="sxs-lookup"><span data-stu-id="77c99-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="77c99-108">**アクティビティ**—ソーシャルネットワークにログオンしているユーザーのアカウントで行われているアクティビティのコンテナー。</span><span class="sxs-lookup"><span data-stu-id="77c99-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="77c99-109">**templates**—**アクティビティ**に対応するアクティビティアイテムを表示するために使用されるテンプレートのコンテナー。</span><span class="sxs-lookup"><span data-stu-id="77c99-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="77c99-110">アクティビティフィードアイテムを作成するには、Outlook Social Connector (.osc) プロバイダ拡張 XML スキーマに準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="77c99-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="77c99-111">図1は、アクティビティフィード XML データ構造を示しています。</span><span class="sxs-lookup"><span data-stu-id="77c99-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="77c99-112">**図1。アクティビティフィード XML データ構造**</span><span class="sxs-lookup"><span data-stu-id="77c99-112">**Figure 1. Activity feed XML structure**</span></span>

![アクティビティ XML の構造](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="77c99-114">アクティビティフィードアイテムごとに、このスキーマの最も重要な2つの部分は**activitydetails**要素と**activitytemplatecontainer**要素です。</span><span class="sxs-lookup"><span data-stu-id="77c99-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="77c99-115">**activitydetails**要素は、アクティビティ所有者の名前や、アップロードされた画像の URL など、アクティビティフィードアイテムごとに固有の情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="77c99-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="77c99-116">**activitytemplatecontainer**要素は、各アクティビティフィードアイテムの形式またはレイアウトを格納します。</span><span class="sxs-lookup"><span data-stu-id="77c99-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="77c99-117">個別の**activitytemplate**要素で表されるテンプレートで構成され、複数のフィードアイテムに再利用できます。</span><span class="sxs-lookup"><span data-stu-id="77c99-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="77c99-118">個別のアクティビティフィードアイテムの場合、 **activitytemplate**要素は次の4つの情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="77c99-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="77c99-119">**icon**—アクティビティフィードアイテムを表示するアイコンの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="77c99-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="77c99-120">[**タイトル**]: アクティビティフィードアイテムを記述します。</span><span class="sxs-lookup"><span data-stu-id="77c99-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="77c99-121">**種類**—状態、写真、ドキュメントの更新など、アクティビティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="77c99-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="77c99-122">**データ**—アクティビティフィードアイテムと共に表示されるその他の情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="77c99-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="77c99-123">アクティビティフィードに表示されるアイコンは、常に、i/////"/"/"/入力された" **networkicon**プロパティによって返されるプロバイダアイコンと同じです。</span><span class="sxs-lookup"><span data-stu-id="77c99-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="77c99-124">**activitydetails**要素、 **activitytemplatecontainer**要素、テンプレートトークン、およびテンプレート変数の詳細については、以下のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="77c99-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="77c99-125">activitydetails 要素</span><span class="sxs-lookup"><span data-stu-id="77c99-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="77c99-126">activitytemplatecontainer 要素</span><span class="sxs-lookup"><span data-stu-id="77c99-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="77c99-127">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="77c99-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="77c99-128">アクティビティを適切に表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="77c99-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="77c99-129">アクティビティフィード xml の例については、「[アクティビティフィード xml の例](activity-feed-xml-example.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77c99-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="77c99-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="77c99-130">See also</span></span>

- [<span data-ttu-id="77c99-131">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="77c99-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="77c99-132">Outlook Social Connector プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="77c99-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="77c99-133">.osc XML スキーマを使用してプロバイダーを開発する</span><span class="sxs-lookup"><span data-stu-id="77c99-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

