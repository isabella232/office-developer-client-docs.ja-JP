---
title: activitytemplatecontainer 要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: activitytemplatecontainer 要素は、アクティビティフィードアイテムを書式設定し、レイアウトを指定する XML を再利用できるテンプレートです。
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413718"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="47812-103">activitytemplatecontainer 要素</span><span class="sxs-lookup"><span data-stu-id="47812-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="47812-104">**activitytemplatecontainer**要素は、アクティビティフィードアイテムを書式設定し、レイアウトを指定する XML を再利用できるテンプレートです。</span><span class="sxs-lookup"><span data-stu-id="47812-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="47812-105">id (**applicationID**および**templateID**) を使用して、フィードアイテム (**activitydetails**) をテンプレート (**activitytemplatecontainer**) と照合します。</span><span class="sxs-lookup"><span data-stu-id="47812-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="47812-106">レイアウトデータを**activitytemplate**要素の一部として格納します。</span><span class="sxs-lookup"><span data-stu-id="47812-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="47812-107">個別のアクティビティフィードアイテムから取り出されたデータを参照するには、人物、リンク、テキストなどの情報のためにテンプレート変数をプレースホルダーとして使用します。</span><span class="sxs-lookup"><span data-stu-id="47812-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="47812-108">次の表では、 **activitytemplatecontainer**要素に必要な3つの要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="47812-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="47812-109">**要素**</span><span class="sxs-lookup"><span data-stu-id="47812-109">**Element**</span></span>|<span data-ttu-id="47812-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="47812-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="47812-111">**applicationID**</span><span class="sxs-lookup"><span data-stu-id="47812-111">**applicationID**</span></span> <br/> |<span data-ttu-id="47812-112">フィードアイテムとそのテンプレートを一致させるために使用される2つの一意の id のいずれか。</span><span class="sxs-lookup"><span data-stu-id="47812-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="47812-113">複数のアプリケーションまたは他のグループがある場合は、これを第1層のテンプレートオーガナイザーとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="47812-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="47812-114">**templateID**</span><span class="sxs-lookup"><span data-stu-id="47812-114">**templateID**</span></span> <br/> |<span data-ttu-id="47812-115">フィードアイテムとそのテンプレートを照合するために使用される2番目の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="47812-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="47812-116">これは、第2層のテンプレート開催者として使用できます。</span><span class="sxs-lookup"><span data-stu-id="47812-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="47812-117">**activitytemplate**</span><span class="sxs-lookup"><span data-stu-id="47812-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="47812-118">テンプレートのレイアウト (**アイコン**、**タイトル**、**データ**要素)、およびアクティビティの種類 (**type**要素)。</span><span class="sxs-lookup"><span data-stu-id="47812-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="47812-119">次の表では、テンプレートのレイアウトと種類を説明する**activitytemplate**の子要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="47812-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="47812-120">**要素**</span><span class="sxs-lookup"><span data-stu-id="47812-120">**Element**</span></span>|<span data-ttu-id="47812-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="47812-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="47812-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="47812-122">**icon**</span></span> <br/> |<span data-ttu-id="47812-123">リンクトークン。そのフィードアイテムのアイコンの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="47812-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="47812-124">**title**</span><span class="sxs-lookup"><span data-stu-id="47812-124">**title**</span></span> <br/> |<span data-ttu-id="47812-125">フィードアイテムに必要な情報。</span><span class="sxs-lookup"><span data-stu-id="47812-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="47812-126">**type**</span><span class="sxs-lookup"><span data-stu-id="47812-126">**type**</span></span> <br/> |<span data-ttu-id="47812-127">状態、写真、ドキュメントの更新など、アクティビティの種類。</span><span class="sxs-lookup"><span data-stu-id="47812-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="47812-128">**data**</span><span class="sxs-lookup"><span data-stu-id="47812-128">**data**</span></span> <br/> |<span data-ttu-id="47812-129">フィードアイテムの追加情報 (画像、テキスト、リンクなど)。</span><span class="sxs-lookup"><span data-stu-id="47812-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="47812-130">アクティビティフィード xml の例については、「[アクティビティフィード xml の例](activity-feed-xml-example.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47812-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="47812-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="47812-131">See also</span></span>

- [<span data-ttu-id="47812-132">アクティビティフィードアイテムの XML の概要</span><span class="sxs-lookup"><span data-stu-id="47812-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="47812-133">activitydetails 要素</span><span class="sxs-lookup"><span data-stu-id="47812-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="47812-134">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="47812-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="47812-135">アクティビティを適切に表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="47812-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="47812-136">アクティビティの XML</span><span class="sxs-lookup"><span data-stu-id="47812-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="47812-137">Outlook Social Connector プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="47812-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="47812-138">.osc XML スキーマを使用してプロバイダーを開発する</span><span class="sxs-lookup"><span data-stu-id="47812-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

