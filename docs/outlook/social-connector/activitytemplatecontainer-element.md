---
title: activityTemplateContainer 要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: ActivityTemplateContainer 要素は、テンプレート、アクティビティ フィードのアイテムの書式設定し、レイアウトを指定する XML を再利用するためです。
ms.openlocfilehash: e744bb1bdb828003cdda7086468533b32b4bf20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804336"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="93064-103">activityTemplateContainer 要素</span><span class="sxs-lookup"><span data-stu-id="93064-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="93064-104">**ActivityTemplateContainer**要素は、テンプレート、アクティビティ フィードのアイテムの書式設定し、レイアウトを指定する XML を再利用するためです。</span><span class="sxs-lookup"><span data-stu-id="93064-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="93064-105">Id (**付きアプリケーション Id** **テンプレート Id**) テンプレート (**activityTemplateContainer**) へのフィードのアイテム (**activityDetails**) と一致するを使用します。</span><span class="sxs-lookup"><span data-stu-id="93064-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="93064-106">**ActivityTemplate**要素の一部としてレイアウトのデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="93064-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="93064-107">個々 のアクティビティのフィードのアイテムから抽出されたデータを参照するには、人、リンク、およびテキストなどの情報のプレース ホルダーとしてテンプレート変数を使用します。</span><span class="sxs-lookup"><span data-stu-id="93064-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="93064-108">次の表では、 **activityTemplateContainer**要素を必要とする 3 つの要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="93064-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="93064-109">**要素**</span><span class="sxs-lookup"><span data-stu-id="93064-109">**Element**</span></span>|<span data-ttu-id="93064-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="93064-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="93064-111">**付きアプリケーション Id**</span><span class="sxs-lookup"><span data-stu-id="93064-111">**applicationID**</span></span> <br/> |<span data-ttu-id="93064-112">そのテンプレートを使用してフィードの項目に一致するように使用される 2 つの一意の Id の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="93064-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="93064-113">複数のアプリケーションまたはその他のグループがあれば、1 層構成のテンプレートの開催者は、これを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93064-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="93064-114">**テンプレート Id**</span><span class="sxs-lookup"><span data-stu-id="93064-114">**templateID**</span></span> <br/> |<span data-ttu-id="93064-115">そのテンプレートを使用してフィードの項目を一致させるために使用される 2 番目の固有 ID。</span><span class="sxs-lookup"><span data-stu-id="93064-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="93064-116">開催者は、第 2 層のテンプレートは、これを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93064-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="93064-117">**activityTemplate**</span><span class="sxs-lookup"><span data-stu-id="93064-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="93064-118">テンプレート (**アイコン**、**タイトル**、および**データ**要素) と活動 (**型**の要素) の種類のレイアウト。</span><span class="sxs-lookup"><span data-stu-id="93064-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="93064-119">次の表では、レイアウトとテンプレートの種類を説明する**activityTemplate**の子要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="93064-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="93064-120">**要素**</span><span class="sxs-lookup"><span data-stu-id="93064-120">**Element**</span></span>|<span data-ttu-id="93064-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="93064-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="93064-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="93064-122">**icon**</span></span> <br/> |<span data-ttu-id="93064-123">そのフィードのアイテムのアイコンの URL を参照するリンク トークンです。</span><span class="sxs-lookup"><span data-stu-id="93064-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="93064-124">**title**</span><span class="sxs-lookup"><span data-stu-id="93064-124">**title**</span></span> <br/> |<span data-ttu-id="93064-125">フィードの項目に必要な情報です。</span><span class="sxs-lookup"><span data-stu-id="93064-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="93064-126">**type**</span><span class="sxs-lookup"><span data-stu-id="93064-126">**type**</span></span> <br/> |<span data-ttu-id="93064-127">状態、写真、またはドキュメントの更新など、活動の種類。</span><span class="sxs-lookup"><span data-stu-id="93064-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="93064-128">**data**</span><span class="sxs-lookup"><span data-stu-id="93064-128">**data**</span></span> <br/> |<span data-ttu-id="93064-129">フィード項目、画像、テキスト、リンクなどの追加情報です。</span><span class="sxs-lookup"><span data-stu-id="93064-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="93064-130">アクティビティの例については、フィードの XML、[アクティビティ フィードの XML の例](activity-feed-xml-example.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93064-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="93064-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="93064-131">See also</span></span>

- [<span data-ttu-id="93064-132">フィード アイテムの活動項目の XML の概要</span><span class="sxs-lookup"><span data-stu-id="93064-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="93064-133">activityDetails 要素</span><span class="sxs-lookup"><span data-stu-id="93064-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="93064-134">テンプレート変数</span><span class="sxs-lookup"><span data-stu-id="93064-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="93064-135">アクティビティを正しく表示するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="93064-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="93064-136">活動の XML</span><span class="sxs-lookup"><span data-stu-id="93064-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="93064-137">Outlook ソーシャル コネクタ プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="93064-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="93064-138">OSC の XML スキーマを使用してプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="93064-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

