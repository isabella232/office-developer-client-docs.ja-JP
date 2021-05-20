---
title: アクティビティ フィード アイテムのための XML の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: アクティビティ フィードは、ソーシャル ネットワーク上で発生する 1 つ以上のアクティビティで構成されます。 各アクティビティ フィードは activityFeed 要素で表され、次の 3 つの情報が特徴です。
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439948"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="51c4a-104">アクティビティ フィード アイテムのための XML の概要</span><span class="sxs-lookup"><span data-stu-id="51c4a-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="51c4a-105">アクティビティ フィードは、ソーシャル ネットワーク上で発生する 1 つ以上のアクティビティで構成されます。</span><span class="sxs-lookup"><span data-stu-id="51c4a-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="51c4a-106">各アクティビティ フィードは **activityFeed** 要素で表され、次の 3 つの情報が特徴です。</span><span class="sxs-lookup"><span data-stu-id="51c4a-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="51c4a-107">**network**—アクティビティの発信元のソーシャル ネットワークの名前。</span><span class="sxs-lookup"><span data-stu-id="51c4a-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="51c4a-108">**activities**—そのソーシャル ネットワーク上のログオンしているユーザーのアカウントで発生するアクティビティのコンテナー。</span><span class="sxs-lookup"><span data-stu-id="51c4a-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="51c4a-109">**templates**—アクティビティに対応するアクティビティ アイテムを表示するために使用されるテンプレートの **コンテナー** です。</span><span class="sxs-lookup"><span data-stu-id="51c4a-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="51c4a-110">アクティビティ フィード アイテムを作成するには、ソーシャル コネクタ (OSC) プロバイダー Outlook XML スキーマに準拠する必要があります。</span><span class="sxs-lookup"><span data-stu-id="51c4a-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="51c4a-111">図 1 は、アクティビティ フィードの XML 構造を示しています。</span><span class="sxs-lookup"><span data-stu-id="51c4a-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="51c4a-112">**図 1.アクティビティ フィードの XML 構造**</span><span class="sxs-lookup"><span data-stu-id="51c4a-112">**Figure 1. Activity feed XML structure**</span></span>

![アクティビティ XML の構造](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="51c4a-114">各アクティビティ フィード アイテムについて、このスキーマの最も重要な 2 つの部分は **、activityDetails** 要素と **activityTemplateContainer** 要素です。</span><span class="sxs-lookup"><span data-stu-id="51c4a-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="51c4a-115">**activityDetails** 要素には、アクティビティの所有者の名前やアップロードされた画像の URL など、各アクティビティ フィード アイテムの特定の情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="51c4a-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="51c4a-116">**activityTemplateContainer 要素** は、各アクティビティ フィード アイテムの形式またはレイアウトを格納します。</span><span class="sxs-lookup"><span data-stu-id="51c4a-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="51c4a-117">個々の **activityTemplate** 要素で表されるテンプレートで構成され、複数のフィード アイテムに再利用できます。</span><span class="sxs-lookup"><span data-stu-id="51c4a-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="51c4a-118">個々のアクティビティ フィード アイテムの **activityTemplate** 要素は、次の 4 つの情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="51c4a-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="51c4a-119">**icon**—アクティビティ フィード アイテムを表示するアイコンの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="51c4a-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="51c4a-120">**title**—アクティビティ フィード アイテムについて説明します。</span><span class="sxs-lookup"><span data-stu-id="51c4a-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="51c4a-121">**type**—状態、写真、ドキュメントの更新など、アクティビティの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="51c4a-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="51c4a-122">**data**—アクティビティ フィード アイテムと一緒に表示される追加の情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="51c4a-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="51c4a-123">アクティビティ フィードに表示されるアイコンは **、ISocialProvider::SocialNetworkIcon** プロパティによって返されるプロバイダー アイコンと常に同じです。</span><span class="sxs-lookup"><span data-stu-id="51c4a-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="51c4a-124">**activityDetails** 要素 **、activityTemplateContainer** 要素、テンプレート トークン、テンプレート変数の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="51c4a-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="51c4a-125">activityDetails 要素</span><span class="sxs-lookup"><span data-stu-id="51c4a-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="51c4a-126">activityTemplateContainer 要素</span><span class="sxs-lookup"><span data-stu-id="51c4a-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="51c4a-127">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="51c4a-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="51c4a-128">アクティビティを適切に表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="51c4a-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="51c4a-129">アクティビティ フィード XML の例については、「アクティビティ フィード [XML の例」を参照してください](activity-feed-xml-example.md)。</span><span class="sxs-lookup"><span data-stu-id="51c4a-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="51c4a-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="51c4a-130">See also</span></span>

- [<span data-ttu-id="51c4a-131">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="51c4a-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="51c4a-132">Outlookソーシャル コネクタ プロバイダー XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="51c4a-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="51c4a-133">OSC XML スキーマを使用したプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="51c4a-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

