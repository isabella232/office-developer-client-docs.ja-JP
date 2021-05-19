---
title: activityDetails 要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: activityDetails 要素は、1 つのアクティビティ フィード アイテムの生データを格納します。 各アクティビティ フィード アイテムには、独自の activityDetails 要素が必要です。 activityDetails 要素のデータは、name 要素を使用してアクティビティ テンプレートで参照されます。
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434873"
---
# <a name="activitydetails-element"></a><span data-ttu-id="d1ab3-105">activityDetails 要素</span><span class="sxs-lookup"><span data-stu-id="d1ab3-105">activityDetails Element</span></span>

<span data-ttu-id="d1ab3-106">**activityDetails 要素** は、1 つのアクティビティ フィード アイテムの生データを格納します。</span><span class="sxs-lookup"><span data-stu-id="d1ab3-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="d1ab3-107">各アクティビティ フィード アイテムには、独自の **activityDetails 要素が必要** です。</span><span class="sxs-lookup"><span data-stu-id="d1ab3-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="d1ab3-108">**activityDetails 要素のデータ** は、name 要素を使用してアクティビティ テンプレート **で参照** されます。</span><span class="sxs-lookup"><span data-stu-id="d1ab3-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="d1ab3-109">**activityDetails** 要素のすべてのデータには、name 要素が **必要** です。</span><span class="sxs-lookup"><span data-stu-id="d1ab3-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="d1ab3-110">次の表に **、activityDetails** 要素で必要な 6 つの要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="d1ab3-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="d1ab3-111">**要素**</span><span class="sxs-lookup"><span data-stu-id="d1ab3-111">**Element**</span></span>|<span data-ttu-id="d1ab3-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="d1ab3-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d1ab3-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="d1ab3-113">**ownerID**</span></span> <br/> |<span data-ttu-id="d1ab3-114">このアクティビティ フィード アイテムを生成したソーシャル ネットワーク上のユーザーの ID。</span><span class="sxs-lookup"><span data-stu-id="d1ab3-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="d1ab3-115">**objectID**</span><span class="sxs-lookup"><span data-stu-id="d1ab3-115">**objectID**</span></span> <br/> |<span data-ttu-id="d1ab3-116">重複するフィード アイテムを検出するアクティビティ フィード アイテムの一意の文字列。</span><span class="sxs-lookup"><span data-stu-id="d1ab3-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="d1ab3-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="d1ab3-117">**applicationId**</span></span> <br/> |<span data-ttu-id="d1ab3-118">アクティビティ フィード アイテムとテンプレートを一致するために使用される 2 つの一意の ID の 1 つ。</span><span class="sxs-lookup"><span data-stu-id="d1ab3-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="d1ab3-119">複数のアプリケーションまたは他のグループ化がある場合、これは第 1 層テンプレートオーガナイザーとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1ab3-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="d1ab3-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="d1ab3-120">**templateId**</span></span> <br/> |<span data-ttu-id="d1ab3-121">アクティビティ フィード アイテムとテンプレートを一致するために使用される 2 番目の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="d1ab3-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="d1ab3-122">これは、第 2 層テンプレートオーガナイザーとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1ab3-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="d1ab3-123">**publishDate**</span><span class="sxs-lookup"><span data-stu-id="d1ab3-123">**publishDate**</span></span> <br/> |<span data-ttu-id="d1ab3-124">アクティビティ フィード アイテムが発行された日付と時刻。</span><span class="sxs-lookup"><span data-stu-id="d1ab3-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="d1ab3-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="d1ab3-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="d1ab3-126">アクティビティ フィード アイテム テンプレートのトークンで使用するデータ。</span><span class="sxs-lookup"><span data-stu-id="d1ab3-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="d1ab3-127">アクティビティ フィード XML の例については、「アクティビティ フィード [XML の例」を参照してください。](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="d1ab3-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1ab3-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1ab3-128">See also</span></span>

- [<span data-ttu-id="d1ab3-129">アクティビティ フィード アイテムの XML の概要</span><span class="sxs-lookup"><span data-stu-id="d1ab3-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="d1ab3-130">activityTemplateContainer 要素</span><span class="sxs-lookup"><span data-stu-id="d1ab3-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="d1ab3-131">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="d1ab3-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="d1ab3-132">アクティビティを適切に表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="d1ab3-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="d1ab3-133">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="d1ab3-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="d1ab3-134">Outlookソーシャル コネクタ プロバイダー XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="d1ab3-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="d1ab3-135">OSC XML スキーマを使用したプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="d1ab3-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

