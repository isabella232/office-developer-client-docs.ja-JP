---
title: HeaderFooterFont_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: 1d7c4d6850e4a8ea1933ae751c580d09e0dd67bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805508"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="95b31-102">HeaderFooterFont_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="95b31-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="95b31-103">型情報</span><span class="sxs-lookup"><span data-stu-id="95b31-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95b31-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="95b31-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="95b31-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="95b31-105">**Schema file**</span></span> <br/> |<span data-ttu-id="95b31-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="95b31-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="95b31-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="95b31-107">**Extension base**</span></span> <br/> |<span data-ttu-id="95b31-108">なし</span><span class="sxs-lookup"><span data-stu-id="95b31-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95b31-109">定義</span><span class="sxs-lookup"><span data-stu-id="95b31-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="95b31-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="95b31-110">Elements and attributes</span></span>

<span data-ttu-id="95b31-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="95b31-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="95b31-112">子要素</span><span class="sxs-lookup"><span data-stu-id="95b31-112">Child elements</span></span>

<span data-ttu-id="95b31-113">なし。</span><span class="sxs-lookup"><span data-stu-id="95b31-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95b31-114">属性</span><span class="sxs-lookup"><span data-stu-id="95b31-114">Attributes</span></span>

|<span data-ttu-id="95b31-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="95b31-115">**Attribute**</span></span>|<span data-ttu-id="95b31-116">**型**</span><span class="sxs-lookup"><span data-stu-id="95b31-116">**Type**</span></span>|<span data-ttu-id="95b31-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="95b31-117">**Required**</span></span>|<span data-ttu-id="95b31-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="95b31-118">**Description**</span></span>|<span data-ttu-id="95b31-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="95b31-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="95b31-120">文字セット</span><span class="sxs-lookup"><span data-stu-id="95b31-120">CharSet</span></span>  <br/> |<span data-ttu-id="95b31-121">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="95b31-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="95b31-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-122">optional</span></span>  <br/> ||<span data-ttu-id="95b31-123">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95b31-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="95b31-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="95b31-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="95b31-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="95b31-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="95b31-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-126">optional</span></span>  <br/> ||<span data-ttu-id="95b31-127">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95b31-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="95b31-128">文字送り</span><span class="sxs-lookup"><span data-stu-id="95b31-128">Escapement</span></span>  <br/> |<span data-ttu-id="95b31-129">xsd:int</span><span class="sxs-lookup"><span data-stu-id="95b31-129">xsd:int</span></span>  <br/> |<span data-ttu-id="95b31-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-130">optional</span></span>  <br/> ||<span data-ttu-id="95b31-131">Xsd:int 型の値です。</span><span class="sxs-lookup"><span data-stu-id="95b31-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="95b31-132">フォント名</span><span class="sxs-lookup"><span data-stu-id="95b31-132">FaceName</span></span>  <br/> |<span data-ttu-id="95b31-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="95b31-133">xsd:string</span></span>  <br/> |<span data-ttu-id="95b31-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-134">optional</span></span>  <br/> ||<span data-ttu-id="95b31-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95b31-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="95b31-136">Height</span><span class="sxs-lookup"><span data-stu-id="95b31-136">Height</span></span>  <br/> |<span data-ttu-id="95b31-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="95b31-137">xsd:int</span></span>  <br/> |<span data-ttu-id="95b31-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-138">optional</span></span>  <br/> ||<span data-ttu-id="95b31-139">Xsd:int 型の値です。</span><span class="sxs-lookup"><span data-stu-id="95b31-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="95b31-140">イタリック</span><span class="sxs-lookup"><span data-stu-id="95b31-140">Italic</span></span>  <br/> |<span data-ttu-id="95b31-141">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="95b31-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="95b31-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-142">optional</span></span>  <br/> ||<span data-ttu-id="95b31-143">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95b31-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="95b31-144">オリエンテーション</span><span class="sxs-lookup"><span data-stu-id="95b31-144">Orientation</span></span>  <br/> |<span data-ttu-id="95b31-145">xsd:int</span><span class="sxs-lookup"><span data-stu-id="95b31-145">xsd:int</span></span>  <br/> |<span data-ttu-id="95b31-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-146">optional</span></span>  <br/> ||<span data-ttu-id="95b31-147">Xsd:int 型の値です。</span><span class="sxs-lookup"><span data-stu-id="95b31-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="95b31-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="95b31-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="95b31-149">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="95b31-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="95b31-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-150">optional</span></span>  <br/> ||<span data-ttu-id="95b31-151">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95b31-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="95b31-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="95b31-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="95b31-153">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="95b31-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="95b31-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-154">optional</span></span>  <br/> ||<span data-ttu-id="95b31-155">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95b31-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="95b31-156">品質</span><span class="sxs-lookup"><span data-stu-id="95b31-156">Quality</span></span>  <br/> |<span data-ttu-id="95b31-157">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="95b31-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="95b31-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-158">optional</span></span>  <br/> ||<span data-ttu-id="95b31-159">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95b31-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="95b31-160">取り消し線</span><span class="sxs-lookup"><span data-stu-id="95b31-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="95b31-161">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="95b31-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="95b31-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-162">optional</span></span>  <br/> ||<span data-ttu-id="95b31-163">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95b31-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="95b31-164">下線</span><span class="sxs-lookup"><span data-stu-id="95b31-164">Underline</span></span>  <br/> |<span data-ttu-id="95b31-165">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="95b31-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="95b31-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-166">optional</span></span>  <br/> ||<span data-ttu-id="95b31-167">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95b31-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="95b31-168">太さ</span><span class="sxs-lookup"><span data-stu-id="95b31-168">Weight</span></span>  <br/> |<span data-ttu-id="95b31-169">xsd:int</span><span class="sxs-lookup"><span data-stu-id="95b31-169">xsd:int</span></span>  <br/> |<span data-ttu-id="95b31-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-170">optional</span></span>  <br/> ||<span data-ttu-id="95b31-171">Xsd:int 型の値です。</span><span class="sxs-lookup"><span data-stu-id="95b31-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="95b31-172">Width</span><span class="sxs-lookup"><span data-stu-id="95b31-172">Width</span></span>  <br/> |<span data-ttu-id="95b31-173">xsd:int</span><span class="sxs-lookup"><span data-stu-id="95b31-173">xsd:int</span></span>  <br/> |<span data-ttu-id="95b31-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="95b31-174">optional</span></span>  <br/> ||<span data-ttu-id="95b31-175">Xsd:int 型の値です。</span><span class="sxs-lookup"><span data-stu-id="95b31-175">Values of the xsd:int type.</span></span>  <br/> |
   

