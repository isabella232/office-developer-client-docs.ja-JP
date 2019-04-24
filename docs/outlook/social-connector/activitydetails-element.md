---
title: activitydetails 要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: activitydetails 要素は、1つのアクティビティフィードアイテムの生データを格納します。 各アクティビティフィードアイテムは、独自の activitydetails 要素を持つ必要があります。 activitydetails 要素のデータは、アクティビティテンプレートで name 要素を使用して参照されます。
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281350"
---
# <a name="activitydetails-element"></a><span data-ttu-id="94e62-105">activitydetails 要素</span><span class="sxs-lookup"><span data-stu-id="94e62-105">activityDetails Element</span></span>

<span data-ttu-id="94e62-106">**activitydetails**要素は、1つのアクティビティフィードアイテムの生データを格納します。</span><span class="sxs-lookup"><span data-stu-id="94e62-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="94e62-107">各アクティビティフィードアイテムは、独自の**activitydetails**要素を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="94e62-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="94e62-108">**activitydetails**要素のデータは、アクティビティテンプレートで**name**要素を使用して参照されます。</span><span class="sxs-lookup"><span data-stu-id="94e62-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="94e62-109">**activitydetails**要素のすべてのデータに**name**要素が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="94e62-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="94e62-110">次の表では、 **activitydetails**要素に必要な6つの要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="94e62-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="94e62-111">**要素**</span><span class="sxs-lookup"><span data-stu-id="94e62-111">**Element**</span></span>|<span data-ttu-id="94e62-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="94e62-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="94e62-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="94e62-113">**ownerID**</span></span> <br/> |<span data-ttu-id="94e62-114">このアクティビティフィードアイテムを生成したソーシャルネットワーク上のユーザーの ID。</span><span class="sxs-lookup"><span data-stu-id="94e62-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="94e62-115">**id**</span><span class="sxs-lookup"><span data-stu-id="94e62-115">**objectID**</span></span> <br/> |<span data-ttu-id="94e62-116">重複したフィードアイテムを検出するためのアクティビティフィードアイテムの一意の文字列。</span><span class="sxs-lookup"><span data-stu-id="94e62-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="94e62-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="94e62-117">**applicationId**</span></span> <br/> |<span data-ttu-id="94e62-118">アクティビティフィードアイテムをテンプレートと照合するために使用される2つの一意の id のいずれか。</span><span class="sxs-lookup"><span data-stu-id="94e62-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="94e62-119">複数のアプリケーションまたは他のグループがある場合は、これを第1層のテンプレートオーガナイザーとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="94e62-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="94e62-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="94e62-120">**templateId**</span></span> <br/> |<span data-ttu-id="94e62-121">アクティビティフィードアイテムをテンプレートと照合するために使用される2番目の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="94e62-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="94e62-122">これは、第2層のテンプレート開催者として使用できます。</span><span class="sxs-lookup"><span data-stu-id="94e62-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="94e62-123">**publishdate**</span><span class="sxs-lookup"><span data-stu-id="94e62-123">**publishDate**</span></span> <br/> |<span data-ttu-id="94e62-124">アクティビティフィードアイテムが発行された日時。</span><span class="sxs-lookup"><span data-stu-id="94e62-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="94e62-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="94e62-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="94e62-126">アクティビティフィードアイテムテンプレートのトークンで使用されるデータ。</span><span class="sxs-lookup"><span data-stu-id="94e62-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="94e62-127">アクティビティフィード xml の例については、「[アクティビティフィード xml の例](activity-feed-xml-example.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="94e62-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="94e62-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="94e62-128">See also</span></span>

- [<span data-ttu-id="94e62-129">アクティビティフィードアイテムの XML の概要</span><span class="sxs-lookup"><span data-stu-id="94e62-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="94e62-130">activitytemplatecontainer 要素</span><span class="sxs-lookup"><span data-stu-id="94e62-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="94e62-131">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="94e62-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="94e62-132">アクティビティを適切に表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="94e62-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="94e62-133">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="94e62-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="94e62-134">Outlook Social Connector プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="94e62-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="94e62-135">.osc XML スキーマを使用してプロバイダーを開発する</span><span class="sxs-lookup"><span data-stu-id="94e62-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

