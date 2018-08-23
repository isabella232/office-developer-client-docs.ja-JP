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
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="932f8-103">RefBy 要素 (Trigger_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="932f8-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="932f8-104">図面のページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="932f8-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="932f8-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="932f8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="932f8-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="932f8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="932f8-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="932f8-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="932f8-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="932f8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="932f8-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="932f8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="932f8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="932f8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="932f8-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="932f8-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="932f8-112">定義</span><span class="sxs-lookup"><span data-stu-id="932f8-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="932f8-113">要素と属性</span><span class="sxs-lookup"><span data-stu-id="932f8-113">Elements and attributes</span></span>

<span data-ttu-id="932f8-114">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="932f8-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="932f8-115">親要素</span><span class="sxs-lookup"><span data-stu-id="932f8-115">Parent elements</span></span>

|<span data-ttu-id="932f8-116">**要素**</span><span class="sxs-lookup"><span data-stu-id="932f8-116">**Element**</span></span>|<span data-ttu-id="932f8-117">**型**</span><span class="sxs-lookup"><span data-stu-id="932f8-117">**Type**</span></span>|<span data-ttu-id="932f8-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="932f8-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="932f8-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="932f8-119">Trigger</span></span>](http://msdn.microsoft.com/library/6dbd2c66-3b29-03f6-648f-723d359ded0d%28Office.15%29.aspx) <br/> |[<span data-ttu-id="932f8-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="932f8-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="932f8-121">Visio ファイル内のドキュメント パーツ間の関係を再計算するための Microsoft Visio に指示を提供します。</span><span class="sxs-lookup"><span data-stu-id="932f8-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
|[<span data-ttu-id="932f8-122">Trigger</span><span class="sxs-lookup"><span data-stu-id="932f8-122">Trigger</span></span>](http://msdn.microsoft.com/library/e4eeb238-f6d0-fb23-db1c-01d55b0a8d88%28Office.15%29.aspx) <br/> |[<span data-ttu-id="932f8-123">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="932f8-123">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="932f8-124">Visio ファイル内のドキュメント パーツ間の関係を再計算するための Microsoft Visio に指示を提供します。</span><span class="sxs-lookup"><span data-stu-id="932f8-124">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
|[<span data-ttu-id="932f8-125">Trigger</span><span class="sxs-lookup"><span data-stu-id="932f8-125">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="932f8-126">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="932f8-126">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="932f8-127">Visio ファイル内のドキュメント パーツ間の関係を再計算するための Microsoft Visio に指示を提供します。</span><span class="sxs-lookup"><span data-stu-id="932f8-127">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="932f8-128">子要素</span><span class="sxs-lookup"><span data-stu-id="932f8-128">Child elements</span></span>

<span data-ttu-id="932f8-129">なし。</span><span class="sxs-lookup"><span data-stu-id="932f8-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="932f8-130">属性</span><span class="sxs-lookup"><span data-stu-id="932f8-130">Attributes</span></span>

|<span data-ttu-id="932f8-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="932f8-131">**Attribute**</span></span>|<span data-ttu-id="932f8-132">**型**</span><span class="sxs-lookup"><span data-stu-id="932f8-132">**Type**</span></span>|<span data-ttu-id="932f8-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="932f8-133">**Required**</span></span>|<span data-ttu-id="932f8-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="932f8-134">**Description**</span></span>|<span data-ttu-id="932f8-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="932f8-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="932f8-136">ID</span><span class="sxs-lookup"><span data-stu-id="932f8-136">ID</span></span>  <br/> |<span data-ttu-id="932f8-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="932f8-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="932f8-138">必須</span><span class="sxs-lookup"><span data-stu-id="932f8-138">required</span></span>  <br/> |<span data-ttu-id="932f8-139">図面のページの [ID] 属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="932f8-139">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="932f8-140">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="932f8-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="932f8-141">SV 要素</span><span class="sxs-lookup"><span data-stu-id="932f8-141">T</span></span>  <br/> |<span data-ttu-id="932f8-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="932f8-142">xsd:string</span></span>  <br/> |<span data-ttu-id="932f8-143">必須</span><span class="sxs-lookup"><span data-stu-id="932f8-143">required</span></span>  <br/> |<span data-ttu-id="932f8-144">参照型を指定します。</span><span class="sxs-lookup"><span data-stu-id="932f8-144">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="932f8-145">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="932f8-145">Values of the xsd:string type.</span></span>  <br/> |
   

