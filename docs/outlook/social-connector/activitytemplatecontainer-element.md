---
title: activityTemplateContainer 要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: activityTemplateContainer 要素は、アクティビティ フィード アイテムの書式を設定し、レイアウトを指定する XML を再利用できるテンプレートです。
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413718"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="39565-103">activityTemplateContainer 要素</span><span class="sxs-lookup"><span data-stu-id="39565-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="39565-104">**activityTemplateContainer** 要素は、アクティビティ フィード アイテムの書式を設定し、レイアウトを指定する XML を再利用できるテンプレートです。</span><span class="sxs-lookup"><span data-stu-id="39565-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="39565-105">フィード アイテム (**activityDetails**) をテンプレート (**activityTemplateContainer**) に一致するには、ID (**applicationID** と **templateID**) を使用します。</span><span class="sxs-lookup"><span data-stu-id="39565-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="39565-106">レイアウト データを **activityTemplate 要素の一部として格納** します。</span><span class="sxs-lookup"><span data-stu-id="39565-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="39565-107">個々のアクティビティ フィード アイテムから取得されたデータを参照するには、ユーザー、リンク、テキストなどの情報のプレースホルダーとしてテンプレート変数を使用します。</span><span class="sxs-lookup"><span data-stu-id="39565-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="39565-108">次の表に **、activityTemplateContainer** 要素で必要な 3 つの要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="39565-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="39565-109">**要素**</span><span class="sxs-lookup"><span data-stu-id="39565-109">**Element**</span></span>|<span data-ttu-id="39565-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="39565-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39565-111">**applicationID**</span><span class="sxs-lookup"><span data-stu-id="39565-111">**applicationID**</span></span> <br/> |<span data-ttu-id="39565-112">フィード アイテムとテンプレートを一致するために使用される 2 つの一意の ID の 1 つ。</span><span class="sxs-lookup"><span data-stu-id="39565-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="39565-113">複数のアプリケーションまたは他のグループ化がある場合、これは第 1 層テンプレートオーガナイザーとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="39565-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="39565-114">**templateID**</span><span class="sxs-lookup"><span data-stu-id="39565-114">**templateID**</span></span> <br/> |<span data-ttu-id="39565-115">フィード アイテムとテンプレートを一致するために使用される 2 番目の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="39565-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="39565-116">これは、第 2 層テンプレートオーガナイザーとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="39565-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="39565-117">**activityTemplate**</span><span class="sxs-lookup"><span data-stu-id="39565-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="39565-118">テンプレートのレイアウト (**アイコン**、**タイトル、および\*\*\*\*データ** 要素)、およびアクティビティの種類 (**型** 要素)。</span><span class="sxs-lookup"><span data-stu-id="39565-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="39565-119">次の表では、レイアウトとテンプレートの種類を説明する **activityTemplate** の子要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="39565-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="39565-120">**要素**</span><span class="sxs-lookup"><span data-stu-id="39565-120">**Element**</span></span>|<span data-ttu-id="39565-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="39565-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39565-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="39565-122">**icon**</span></span> <br/> |<span data-ttu-id="39565-123">そのフィード アイテムのアイコンの URL を参照するリンク トークン。</span><span class="sxs-lookup"><span data-stu-id="39565-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="39565-124">**title**</span><span class="sxs-lookup"><span data-stu-id="39565-124">**title**</span></span> <br/> |<span data-ttu-id="39565-125">フィード アイテムに必要な情報。</span><span class="sxs-lookup"><span data-stu-id="39565-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="39565-126">**type**</span><span class="sxs-lookup"><span data-stu-id="39565-126">**type**</span></span> <br/> |<span data-ttu-id="39565-127">アクティビティの種類 (ステータス、写真、ドキュメントの更新など)。</span><span class="sxs-lookup"><span data-stu-id="39565-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="39565-128">**data**</span><span class="sxs-lookup"><span data-stu-id="39565-128">**data**</span></span> <br/> |<span data-ttu-id="39565-129">画像、テキスト、リンクなど、フィード アイテムに関する追加情報。</span><span class="sxs-lookup"><span data-stu-id="39565-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="39565-130">アクティビティ フィード XML の例については、「アクティビティ フィード [XML の例」を参照してください。](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="39565-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="39565-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="39565-131">See also</span></span>

- [<span data-ttu-id="39565-132">アクティビティ フィード アイテムの XML の概要</span><span class="sxs-lookup"><span data-stu-id="39565-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="39565-133">activityDetails 要素</span><span class="sxs-lookup"><span data-stu-id="39565-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="39565-134">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="39565-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="39565-135">アクティビティを適切に表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="39565-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="39565-136">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="39565-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="39565-137">Outlookソーシャル コネクタ プロバイダー XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="39565-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="39565-138">OSC XML スキーマを使用したプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="39565-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

