---
title: activityDetails 要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: ActivityDetails 要素は、1 つのアクティビティ フィードのアイテム用の生データを格納します。 各アクティビティのフィードのアイテムには、独自の activityDetails 要素が必要です。 ActivityDetails 要素内のデータは、名前の要素を使用して、アクティビティ テンプレートで参照されます。
ms.openlocfilehash: c326017a038dff138d690b020a98972a08212690
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804333"
---
# <a name="activitydetails-element"></a><span data-ttu-id="16159-105">activityDetails 要素</span><span class="sxs-lookup"><span data-stu-id="16159-105">activityDetails Element</span></span>

<span data-ttu-id="16159-106">**ActivityDetails**要素は、1 つのアクティビティ フィードのアイテム用の生データを格納します。</span><span class="sxs-lookup"><span data-stu-id="16159-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="16159-107">各アクティビティのフィードのアイテムには、独自の**activityDetails**要素が必要です。</span><span class="sxs-lookup"><span data-stu-id="16159-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="16159-108">**ActivityDetails**要素内のデータは、**名前**の要素を使用して、アクティビティ テンプレートで参照されます。</span><span class="sxs-lookup"><span data-stu-id="16159-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="16159-109">**ActivityDetails**要素内のデータの各要素には、 **name**要素が必要です。</span><span class="sxs-lookup"><span data-stu-id="16159-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="16159-110">次の表では、 **activityDetails**要素を必要とする 6 つの要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="16159-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="16159-111">**要素**</span><span class="sxs-lookup"><span data-stu-id="16159-111">**Element**</span></span>|<span data-ttu-id="16159-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="16159-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="16159-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="16159-113">**ownerID**</span></span> <br/> |<span data-ttu-id="16159-114">この活動を生成したソーシャル ネットワーク上のユーザーの ID は、アイテムをフィードします。</span><span class="sxs-lookup"><span data-stu-id="16159-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="16159-115">**オブジェクト Id**</span><span class="sxs-lookup"><span data-stu-id="16159-115">**objectID**</span></span> <br/> |<span data-ttu-id="16159-116">アクティビティの一意の文字列では、フィード アイテムの重複を検出するために項目をフィードします。</span><span class="sxs-lookup"><span data-stu-id="16159-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="16159-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="16159-117">**applicationId**</span></span> <br/> |<span data-ttu-id="16159-118">アクティビティを一致するように使用される 2 つの一意の Id のいずれかのフィードの項目テンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="16159-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="16159-119">複数のアプリケーションまたはその他のグループがあれば、1 層構成のテンプレートの開催者は、これを使用できます。</span><span class="sxs-lookup"><span data-stu-id="16159-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="16159-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="16159-120">**templateId**</span></span> <br/> |<span data-ttu-id="16159-121">アクティビティを一致させるために使用される 2 つ目の一意の ID は、そのテンプレートを使用してアイテムをフィードします。</span><span class="sxs-lookup"><span data-stu-id="16159-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="16159-122">開催者は、第 2 層のテンプレートは、これを使用できます。</span><span class="sxs-lookup"><span data-stu-id="16159-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="16159-123">**publishDate**</span><span class="sxs-lookup"><span data-stu-id="16159-123">**publishDate**</span></span> <br/> |<span data-ttu-id="16159-124">日付と時間、アクティビティ フィードのアイテムを発行します。</span><span class="sxs-lookup"><span data-stu-id="16159-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="16159-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="16159-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="16159-126">アクティビティ フィード項目テンプレートのトークンに使用するデータ。</span><span class="sxs-lookup"><span data-stu-id="16159-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="16159-127">アクティビティの例については、フィードの XML、[アクティビティ フィードの XML の例](activity-feed-xml-example.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16159-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="16159-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="16159-128">See also</span></span>

- [<span data-ttu-id="16159-129">フィード アイテムの活動項目の XML の概要</span><span class="sxs-lookup"><span data-stu-id="16159-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="16159-130">activityTemplateContainer 要素</span><span class="sxs-lookup"><span data-stu-id="16159-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="16159-131">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="16159-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="16159-132">アクティビティを正しく表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="16159-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="16159-133">活動の XML</span><span class="sxs-lookup"><span data-stu-id="16159-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="16159-134">Outlook ソーシャル コネクタ プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="16159-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="16159-135">OSC の XML スキーマを使用してプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="16159-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

