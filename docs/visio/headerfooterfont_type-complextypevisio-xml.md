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
# <a name="headerfooterfont_type-complextype-visio-xml"></a><span data-ttu-id="fca32-102">HeaderFooterFont_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fca32-102">HeaderFooterFont_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="fca32-103">型情報</span><span class="sxs-lookup"><span data-stu-id="fca32-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fca32-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fca32-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fca32-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="fca32-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fca32-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fca32-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fca32-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="fca32-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fca32-108">なし</span><span class="sxs-lookup"><span data-stu-id="fca32-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fca32-109">定義</span><span class="sxs-lookup"><span data-stu-id="fca32-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fca32-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="fca32-110">Elements and attributes</span></span>

<span data-ttu-id="fca32-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fca32-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fca32-112">子要素</span><span class="sxs-lookup"><span data-stu-id="fca32-112">Child elements</span></span>

<span data-ttu-id="fca32-113">なし。</span><span class="sxs-lookup"><span data-stu-id="fca32-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fca32-114">属性</span><span class="sxs-lookup"><span data-stu-id="fca32-114">Attributes</span></span>

|<span data-ttu-id="fca32-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="fca32-115">**Attribute**</span></span>|<span data-ttu-id="fca32-116">**型**</span><span class="sxs-lookup"><span data-stu-id="fca32-116">**Type**</span></span>|<span data-ttu-id="fca32-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="fca32-117">**Required**</span></span>|<span data-ttu-id="fca32-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="fca32-118">**Description**</span></span>|<span data-ttu-id="fca32-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="fca32-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fca32-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="fca32-120">CharSet</span></span>  <br/> |<span data-ttu-id="fca32-121">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fca32-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fca32-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-122">optional</span></span>  <br/> ||<span data-ttu-id="fca32-123">xsd:unsignedByte 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fca32-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="fca32-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="fca32-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fca32-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fca32-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-126">optional</span></span>  <br/> ||<span data-ttu-id="fca32-127">xsd:unsignedByte 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fca32-128">Escapement</span><span class="sxs-lookup"><span data-stu-id="fca32-128">Escapement</span></span>  <br/> |<span data-ttu-id="fca32-129">xsd:int</span><span class="sxs-lookup"><span data-stu-id="fca32-129">xsd:int</span></span>  <br/> |<span data-ttu-id="fca32-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-130">optional</span></span>  <br/> ||<span data-ttu-id="fca32-131">xsd:int 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="fca32-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="fca32-132">FaceName</span></span>  <br/> |<span data-ttu-id="fca32-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fca32-133">xsd:string</span></span>  <br/> |<span data-ttu-id="fca32-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-134">optional</span></span>  <br/> ||<span data-ttu-id="fca32-135">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fca32-136">Height</span><span class="sxs-lookup"><span data-stu-id="fca32-136">Height</span></span>  <br/> |<span data-ttu-id="fca32-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="fca32-137">xsd:int</span></span>  <br/> |<span data-ttu-id="fca32-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-138">optional</span></span>  <br/> ||<span data-ttu-id="fca32-139">xsd:int 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="fca32-140">斜体</span><span class="sxs-lookup"><span data-stu-id="fca32-140">Italic</span></span>  <br/> |<span data-ttu-id="fca32-141">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fca32-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fca32-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-142">optional</span></span>  <br/> ||<span data-ttu-id="fca32-143">xsd:unsignedByte 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fca32-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="fca32-144">Orientation</span></span>  <br/> |<span data-ttu-id="fca32-145">xsd:int</span><span class="sxs-lookup"><span data-stu-id="fca32-145">xsd:int</span></span>  <br/> |<span data-ttu-id="fca32-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-146">optional</span></span>  <br/> ||<span data-ttu-id="fca32-147">xsd:int 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="fca32-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="fca32-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="fca32-149">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fca32-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fca32-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-150">optional</span></span>  <br/> ||<span data-ttu-id="fca32-151">xsd:unsignedByte 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fca32-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="fca32-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="fca32-153">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fca32-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fca32-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-154">optional</span></span>  <br/> ||<span data-ttu-id="fca32-155">xsd:unsignedByte 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fca32-156">品質</span><span class="sxs-lookup"><span data-stu-id="fca32-156">Quality</span></span>  <br/> |<span data-ttu-id="fca32-157">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fca32-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fca32-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-158">optional</span></span>  <br/> ||<span data-ttu-id="fca32-159">xsd:unsignedByte 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fca32-160">StrikeOut</span><span class="sxs-lookup"><span data-stu-id="fca32-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="fca32-161">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fca32-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fca32-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-162">optional</span></span>  <br/> ||<span data-ttu-id="fca32-163">xsd:unsignedByte 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fca32-164">下線</span><span class="sxs-lookup"><span data-stu-id="fca32-164">Underline</span></span>  <br/> |<span data-ttu-id="fca32-165">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fca32-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="fca32-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-166">optional</span></span>  <br/> ||<span data-ttu-id="fca32-167">xsd:unsignedByte 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="fca32-168">太さ</span><span class="sxs-lookup"><span data-stu-id="fca32-168">Weight</span></span>  <br/> |<span data-ttu-id="fca32-169">xsd:int</span><span class="sxs-lookup"><span data-stu-id="fca32-169">xsd:int</span></span>  <br/> |<span data-ttu-id="fca32-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-170">optional</span></span>  <br/> ||<span data-ttu-id="fca32-171">xsd:int 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="fca32-172">Width</span><span class="sxs-lookup"><span data-stu-id="fca32-172">Width</span></span>  <br/> |<span data-ttu-id="fca32-173">xsd:int</span><span class="sxs-lookup"><span data-stu-id="fca32-173">xsd:int</span></span>  <br/> |<span data-ttu-id="fca32-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="fca32-174">optional</span></span>  <br/> ||<span data-ttu-id="fca32-175">xsd:int 型の値。</span><span class="sxs-lookup"><span data-stu-id="fca32-175">Values of the xsd:int type.</span></span>  <br/> |
   

