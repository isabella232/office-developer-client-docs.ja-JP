---
title: RefBy 要素 (Trigger_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: 図面のページへの参照を指定します。
ms.openlocfilehash: 57ac63c4488b68d3af3c6e4a75417e2c7937723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806160"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="c42e0-103">RefBy 要素 (Trigger_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="c42e0-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c42e0-104">図面のページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="c42e0-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c42e0-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="c42e0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c42e0-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="c42e0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c42e0-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="c42e0-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c42e0-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="c42e0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c42e0-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c42e0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c42e0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c42e0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c42e0-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="c42e0-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="c42e0-112">定義</span><span class="sxs-lookup"><span data-stu-id="c42e0-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c42e0-113">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c42e0-113">Elements and attributes</span></span>

<span data-ttu-id="c42e0-114">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c42e0-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c42e0-115">親要素</span><span class="sxs-lookup"><span data-stu-id="c42e0-115">Parent elements</span></span>

|<span data-ttu-id="c42e0-116">**要素**</span><span class="sxs-lookup"><span data-stu-id="c42e0-116">**Element**</span></span>|<span data-ttu-id="c42e0-117">**型**</span><span class="sxs-lookup"><span data-stu-id="c42e0-117">**Type**</span></span>|<span data-ttu-id="c42e0-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="c42e0-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c42e0-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="c42e0-119">Trigger</span></span>](http://msdn.microsoft.com/library/6dbd2c66-3b29-03f6-648f-723d359ded0d%28Office.15%29.aspx) <br/> |[<span data-ttu-id="c42e0-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="c42e0-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c42e0-121">Visio ファイル内のドキュメント パーツ間の関係を再計算するための Microsoft Visio に指示を提供します。</span><span class="sxs-lookup"><span data-stu-id="c42e0-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
|[<span data-ttu-id="c42e0-122">Trigger</span><span class="sxs-lookup"><span data-stu-id="c42e0-122">Trigger</span></span>](http://msdn.microsoft.com/library/e4eeb238-f6d0-fb23-db1c-01d55b0a8d88%28Office.15%29.aspx) <br/> |[<span data-ttu-id="c42e0-123">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="c42e0-123">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c42e0-124">Visio ファイル内のドキュメント パーツ間の関係を再計算するための Microsoft Visio に指示を提供します。</span><span class="sxs-lookup"><span data-stu-id="c42e0-124">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
|[<span data-ttu-id="c42e0-125">Trigger</span><span class="sxs-lookup"><span data-stu-id="c42e0-125">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="c42e0-126">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="c42e0-126">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c42e0-127">Visio ファイル内のドキュメント パーツ間の関係を再計算するための Microsoft Visio に指示を提供します。</span><span class="sxs-lookup"><span data-stu-id="c42e0-127">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c42e0-128">子要素</span><span class="sxs-lookup"><span data-stu-id="c42e0-128">Child elements</span></span>

<span data-ttu-id="c42e0-129">なし。</span><span class="sxs-lookup"><span data-stu-id="c42e0-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c42e0-130">属性</span><span class="sxs-lookup"><span data-stu-id="c42e0-130">Attributes</span></span>

|<span data-ttu-id="c42e0-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="c42e0-131">**Attribute**</span></span>|<span data-ttu-id="c42e0-132">**型**</span><span class="sxs-lookup"><span data-stu-id="c42e0-132">**Type**</span></span>|<span data-ttu-id="c42e0-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="c42e0-133">**Required**</span></span>|<span data-ttu-id="c42e0-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="c42e0-134">**Description**</span></span>|<span data-ttu-id="c42e0-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="c42e0-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c42e0-136">ID</span><span class="sxs-lookup"><span data-stu-id="c42e0-136">ID</span></span>  <br/> |<span data-ttu-id="c42e0-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c42e0-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c42e0-138">必須</span><span class="sxs-lookup"><span data-stu-id="c42e0-138">required</span></span>  <br/> |<span data-ttu-id="c42e0-139">図面のページの [ID] 属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="c42e0-139">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="c42e0-140">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c42e0-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c42e0-141">SV 要素</span><span class="sxs-lookup"><span data-stu-id="c42e0-141">T</span></span>  <br/> |<span data-ttu-id="c42e0-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c42e0-142">xsd:string</span></span>  <br/> |<span data-ttu-id="c42e0-143">必須</span><span class="sxs-lookup"><span data-stu-id="c42e0-143">required</span></span>  <br/> |<span data-ttu-id="c42e0-144">参照型を指定します。</span><span class="sxs-lookup"><span data-stu-id="c42e0-144">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="c42e0-145">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c42e0-145">Values of the xsd:string type.</span></span>  <br/> |
   

