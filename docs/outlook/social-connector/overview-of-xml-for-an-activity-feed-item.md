---
title: アクティビティ フィード アイテムのための XML の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: アクティビティ フィードは、ソーシャル ネットワーク上で発生する 1 つまたは複数のアクティビティで構成されています。 各アクティビティ フィードは、activityFeed 要素によって表されるし、の特徴は、これら 3 つの情報。
ms.openlocfilehash: 318875aeb6312a3710654d129f3f48139ff7ef12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804472"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="0dc14-104">アクティビティ フィード アイテムのための XML の概要</span><span class="sxs-lookup"><span data-stu-id="0dc14-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="0dc14-105">アクティビティ フィードは、ソーシャル ネットワーク上で発生する 1 つまたは複数のアクティビティで構成されています。</span><span class="sxs-lookup"><span data-stu-id="0dc14-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="0dc14-106">各アクティビティ フィードは、 **activityFeed**要素によって表されるし、の特徴は、これら 3 つの情報。</span><span class="sxs-lookup"><span data-stu-id="0dc14-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="0dc14-107">**ネットワーク**-活動の起点となるソーシャル ネットワークの名前です。</span><span class="sxs-lookup"><span data-stu-id="0dc14-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="0dc14-108">**活動**ソーシャル ネットワークにログオンしたユーザーのアカウントで発生するアクティビティのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="0dc14-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="0dc14-109">**テンプレート**など**の活動**に対応する活動項目を表示するために使用するテンプレートのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="0dc14-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="0dc14-110">アクティビティ フィードのアイテムを作成するには、Outlook ソーシャル コネクタ (OSC) プロバイダーの拡張機能の XML スキーマに準拠する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0dc14-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="0dc14-111">アクティビティ フィードの XML の構造を図 1 に示します。</span><span class="sxs-lookup"><span data-stu-id="0dc14-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="0dc14-112">**図 1 です。アクティビティ フィードの XML データ構造**</span><span class="sxs-lookup"><span data-stu-id="0dc14-112">**Figure 1. Activity feed XML structure**</span></span>

![アクティビティ XML の構造](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="0dc14-114">各アクティビティでは、フィードのアイテム、このスキーマの 2 つの最も重要な部分は、 **activityDetails**と**activityTemplateContainer**の要素。</span><span class="sxs-lookup"><span data-stu-id="0dc14-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="0dc14-115">**ActivityDetails**要素は、各アクティビティは、アクティビティの所有者の名前またはアップロードする画像の URL などのアイテムのフィードに固有の情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="0dc14-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="0dc14-116">**ActivityTemplateContainer**要素の形式を格納する、またはフィード項目の各アクティビティのレイアウトです。</span><span class="sxs-lookup"><span data-stu-id="0dc14-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="0dc14-117">テンプレート、複数のフィード項目を再利用できる個々 の**activityTemplate**の要素で表されるので構成されます。</span><span class="sxs-lookup"><span data-stu-id="0dc14-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="0dc14-118">個々 のアクティビティ フィードのアイテムには、 **activityTemplate**要素は、次の 4 つの情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="0dc14-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="0dc14-119">**アイコン**-フィード項目のアクティビティを表示するアイコンの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="0dc14-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="0dc14-120">**タイトル**: アクティビティ フィードの項目を説明します。</span><span class="sxs-lookup"><span data-stu-id="0dc14-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="0dc14-121">**タイプ**ステータス、写真、またはドキュメントの更新など、活動の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="0dc14-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="0dc14-122">**データ**: アクティビティ フィードのアイテムに表示されるすべての追加情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="0dc14-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="0dc14-123">アクティビティ フィードに表示されるアイコンは、常に、 **ISocialProvider::SocialNetworkIcon**プロパティによって返されるプロバイダーのアイコンと同じです。</span><span class="sxs-lookup"><span data-stu-id="0dc14-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="0dc14-124">**ActivityDetails**要素、要素の**activityTemplateContainer** 、テンプレート トークン、およびテンプレート変数の詳細については次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0dc14-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="0dc14-125">activityDetails 要素</span><span class="sxs-lookup"><span data-stu-id="0dc14-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="0dc14-126">activityTemplateContainer 要素</span><span class="sxs-lookup"><span data-stu-id="0dc14-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="0dc14-127">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="0dc14-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="0dc14-128">アクティビティを正しく表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="0dc14-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="0dc14-129">アクティビティの例については、フィードの XML、[アクティビティ フィードの XML の例](activity-feed-xml-example.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0dc14-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0dc14-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="0dc14-130">See also</span></span>

- [<span data-ttu-id="0dc14-131">活動の XML</span><span class="sxs-lookup"><span data-stu-id="0dc14-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="0dc14-132">Outlook ソーシャル コネクタ プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="0dc14-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="0dc14-133">OSC の XML スキーマを使用してプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="0dc14-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

