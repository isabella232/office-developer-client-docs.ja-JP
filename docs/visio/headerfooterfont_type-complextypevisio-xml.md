---
title: HeaderFooterFont_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: dd99d87e0d80aad3bcde31e4834337ee59088da2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541072"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="325c5-102">HeaderFooterFont_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="325c5-102">HeaderFooterFont_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="325c5-103">型情報</span><span class="sxs-lookup"><span data-stu-id="325c5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="325c5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="325c5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="325c5-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="325c5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="325c5-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="325c5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="325c5-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="325c5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="325c5-108">None</span><span class="sxs-lookup"><span data-stu-id="325c5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="325c5-109">定義</span><span class="sxs-lookup"><span data-stu-id="325c5-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderFooterFont_Type">
    <xs:attribute name="Height"
  type="xsd:int"
    />
    <xs:attribute name="Width"
  type="xsd:int"
    />
    <xs:attribute name="Escapement"
  type="xsd:int"
    />
    <xs:attribute name="Orientation"
  type="xsd:int"
    />
    <xs:attribute name="Weight"
  type="xsd:int"
    />
    <xs:attribute name="Italic"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Underline"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="StrikeOut"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="CharSet"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="OutPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="ClipPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Quality"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="PitchAndFamily"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="FaceName"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="325c5-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="325c5-110">Elements and attributes</span></span>

<span data-ttu-id="325c5-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="325c5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="325c5-112">子要素</span><span class="sxs-lookup"><span data-stu-id="325c5-112">Child elements</span></span>

<span data-ttu-id="325c5-113">なし。</span><span class="sxs-lookup"><span data-stu-id="325c5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="325c5-114">属性</span><span class="sxs-lookup"><span data-stu-id="325c5-114">Attributes</span></span>

|<span data-ttu-id="325c5-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="325c5-115">**Attribute**</span></span>|<span data-ttu-id="325c5-116">**型**</span><span class="sxs-lookup"><span data-stu-id="325c5-116">**Type**</span></span>|<span data-ttu-id="325c5-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="325c5-117">**Required**</span></span>|<span data-ttu-id="325c5-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="325c5-118">**Description**</span></span>|<span data-ttu-id="325c5-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="325c5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="325c5-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="325c5-120">CharSet</span></span>  <br/> |<span data-ttu-id="325c5-121">xsd: アン Signedbyte</span><span class="sxs-lookup"><span data-stu-id="325c5-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="325c5-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-122">optional</span></span>  <br/> ||<span data-ttu-id="325c5-123">Xsd:/Signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="325c5-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="325c5-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="325c5-125">xsd: アン Signedbyte</span><span class="sxs-lookup"><span data-stu-id="325c5-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="325c5-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-126">optional</span></span>  <br/> ||<span data-ttu-id="325c5-127">Xsd:/Signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="325c5-128">実際</span><span class="sxs-lookup"><span data-stu-id="325c5-128">Escapement</span></span>  <br/> |<span data-ttu-id="325c5-129">xsd: int</span><span class="sxs-lookup"><span data-stu-id="325c5-129">xsd:int</span></span>  <br/> |<span data-ttu-id="325c5-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-130">optional</span></span>  <br/> ||<span data-ttu-id="325c5-131">Xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="325c5-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="325c5-132">FaceName</span></span>  <br/> |<span data-ttu-id="325c5-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="325c5-133">xsd:string</span></span>  <br/> |<span data-ttu-id="325c5-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-134">optional</span></span>  <br/> ||<span data-ttu-id="325c5-135">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="325c5-136">Height</span><span class="sxs-lookup"><span data-stu-id="325c5-136">Height</span></span>  <br/> |<span data-ttu-id="325c5-137">xsd: int</span><span class="sxs-lookup"><span data-stu-id="325c5-137">xsd:int</span></span>  <br/> |<span data-ttu-id="325c5-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-138">optional</span></span>  <br/> ||<span data-ttu-id="325c5-139">Xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="325c5-140">斜体</span><span class="sxs-lookup"><span data-stu-id="325c5-140">Italic</span></span>  <br/> |<span data-ttu-id="325c5-141">xsd: アン Signedbyte</span><span class="sxs-lookup"><span data-stu-id="325c5-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="325c5-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-142">optional</span></span>  <br/> ||<span data-ttu-id="325c5-143">Xsd:/Signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="325c5-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="325c5-144">Orientation</span></span>  <br/> |<span data-ttu-id="325c5-145">xsd: int</span><span class="sxs-lookup"><span data-stu-id="325c5-145">xsd:int</span></span>  <br/> |<span data-ttu-id="325c5-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-146">optional</span></span>  <br/> ||<span data-ttu-id="325c5-147">Xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="325c5-148">アウト精度</span><span class="sxs-lookup"><span data-stu-id="325c5-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="325c5-149">xsd: アン Signedbyte</span><span class="sxs-lookup"><span data-stu-id="325c5-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="325c5-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-150">optional</span></span>  <br/> ||<span data-ttu-id="325c5-151">Xsd:/Signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="325c5-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="325c5-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="325c5-153">xsd: アン Signedbyte</span><span class="sxs-lookup"><span data-stu-id="325c5-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="325c5-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-154">optional</span></span>  <br/> ||<span data-ttu-id="325c5-155">Xsd:/Signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="325c5-156">Quality</span><span class="sxs-lookup"><span data-stu-id="325c5-156">Quality</span></span>  <br/> |<span data-ttu-id="325c5-157">xsd: アン Signedbyte</span><span class="sxs-lookup"><span data-stu-id="325c5-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="325c5-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-158">optional</span></span>  <br/> ||<span data-ttu-id="325c5-159">Xsd:/Signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="325c5-160">線</span><span class="sxs-lookup"><span data-stu-id="325c5-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="325c5-161">xsd: アン Signedbyte</span><span class="sxs-lookup"><span data-stu-id="325c5-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="325c5-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-162">optional</span></span>  <br/> ||<span data-ttu-id="325c5-163">Xsd:/Signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="325c5-164">下線</span><span class="sxs-lookup"><span data-stu-id="325c5-164">Underline</span></span>  <br/> |<span data-ttu-id="325c5-165">xsd: アン Signedbyte</span><span class="sxs-lookup"><span data-stu-id="325c5-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="325c5-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-166">optional</span></span>  <br/> ||<span data-ttu-id="325c5-167">Xsd:/Signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="325c5-168">太さ</span><span class="sxs-lookup"><span data-stu-id="325c5-168">Weight</span></span>  <br/> |<span data-ttu-id="325c5-169">xsd: int</span><span class="sxs-lookup"><span data-stu-id="325c5-169">xsd:int</span></span>  <br/> |<span data-ttu-id="325c5-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-170">optional</span></span>  <br/> ||<span data-ttu-id="325c5-171">Xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="325c5-172">Width</span><span class="sxs-lookup"><span data-stu-id="325c5-172">Width</span></span>  <br/> |<span data-ttu-id="325c5-173">xsd: int</span><span class="sxs-lookup"><span data-stu-id="325c5-173">xsd:int</span></span>  <br/> |<span data-ttu-id="325c5-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="325c5-174">optional</span></span>  <br/> ||<span data-ttu-id="325c5-175">Xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="325c5-175">Values of the xsd:int type.</span></span>  <br/> |
   

