---
title: Page_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: 3a0153b724539136fe142c2489badcf9895af765
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537984"
---
# <a name="page_type-complextype-visio-xml"></a><span data-ttu-id="280f0-102">Page_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="280f0-102">Page_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="280f0-103">型情報</span><span class="sxs-lookup"><span data-stu-id="280f0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="280f0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="280f0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="280f0-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="280f0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="280f0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="280f0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="280f0-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="280f0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="280f0-108">なし</span><span class="sxs-lookup"><span data-stu-id="280f0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="280f0-109">定義</span><span class="sxs-lookup"><span data-stu-id="280f0-109">Definition</span></span>

```XML
          <xs:complexType name="Page_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="Background"
  type="xsd:boolean"
    />
    <xs:attribute name="BackPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ViewScale"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterX"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterY"
  type="xsd:double"
    />
    <xs:attribute name="ReviewerID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AssociatedPage"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="280f0-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="280f0-110">Elements and attributes</span></span>

<span data-ttu-id="280f0-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="280f0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="280f0-112">子要素</span><span class="sxs-lookup"><span data-stu-id="280f0-112">Child elements</span></span>

|<span data-ttu-id="280f0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="280f0-113">**Element**</span></span>|<span data-ttu-id="280f0-114">**型**</span><span class="sxs-lookup"><span data-stu-id="280f0-114">**Type**</span></span>|<span data-ttu-id="280f0-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="280f0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="280f0-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="280f0-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="280f0-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="280f0-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="280f0-118">Rel</span><span class="sxs-lookup"><span data-stu-id="280f0-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="280f0-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="280f0-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="280f0-120">属性</span><span class="sxs-lookup"><span data-stu-id="280f0-120">Attributes</span></span>

|<span data-ttu-id="280f0-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="280f0-121">**Attribute**</span></span>|<span data-ttu-id="280f0-122">**型**</span><span class="sxs-lookup"><span data-stu-id="280f0-122">**Type**</span></span>|<span data-ttu-id="280f0-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="280f0-123">**Required**</span></span>|<span data-ttu-id="280f0-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="280f0-124">**Description**</span></span>|<span data-ttu-id="280f0-125">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="280f0-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="280f0-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="280f0-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="280f0-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="280f0-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="280f0-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="280f0-128">optional</span></span>  <br/> ||<span data-ttu-id="280f0-129">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="280f0-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="280f0-130">背景</span><span class="sxs-lookup"><span data-stu-id="280f0-130">Background</span></span>  <br/> |<span data-ttu-id="280f0-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="280f0-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="280f0-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="280f0-132">optional</span></span>  <br/> ||<span data-ttu-id="280f0-133">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="280f0-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="280f0-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="280f0-134">BackPage</span></span>  <br/> |<span data-ttu-id="280f0-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="280f0-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="280f0-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="280f0-136">optional</span></span>  <br/> ||<span data-ttu-id="280f0-137">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="280f0-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="280f0-138">ID</span><span class="sxs-lookup"><span data-stu-id="280f0-138">ID</span></span>  <br/> |<span data-ttu-id="280f0-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="280f0-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="280f0-140">必須</span><span class="sxs-lookup"><span data-stu-id="280f0-140">required</span></span>  <br/> ||<span data-ttu-id="280f0-141">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="280f0-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="280f0-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="280f0-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="280f0-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="280f0-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="280f0-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="280f0-144">optional</span></span>  <br/> ||<span data-ttu-id="280f0-145">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="280f0-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="280f0-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="280f0-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="280f0-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="280f0-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="280f0-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="280f0-148">optional</span></span>  <br/> ||<span data-ttu-id="280f0-149">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="280f0-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="280f0-150">名前</span><span class="sxs-lookup"><span data-stu-id="280f0-150">Name</span></span>  <br/> |<span data-ttu-id="280f0-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="280f0-151">xsd:string</span></span>  <br/> |<span data-ttu-id="280f0-152">省略可能</span><span class="sxs-lookup"><span data-stu-id="280f0-152">optional</span></span>  <br/> ||<span data-ttu-id="280f0-153">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="280f0-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="280f0-154">NameU</span><span class="sxs-lookup"><span data-stu-id="280f0-154">NameU</span></span>  <br/> |<span data-ttu-id="280f0-155">xsd:string</span><span class="sxs-lookup"><span data-stu-id="280f0-155">xsd:string</span></span>  <br/> |<span data-ttu-id="280f0-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="280f0-156">optional</span></span>  <br/> ||<span data-ttu-id="280f0-157">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="280f0-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="280f0-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="280f0-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="280f0-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="280f0-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="280f0-160">省略可能</span><span class="sxs-lookup"><span data-stu-id="280f0-160">optional</span></span>  <br/> ||<span data-ttu-id="280f0-161">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="280f0-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="280f0-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="280f0-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="280f0-163">xsd:double</span><span class="sxs-lookup"><span data-stu-id="280f0-163">xsd:double</span></span>  <br/> |<span data-ttu-id="280f0-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="280f0-164">optional</span></span>  <br/> ||<span data-ttu-id="280f0-165">xsd:double 型の値。</span><span class="sxs-lookup"><span data-stu-id="280f0-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="280f0-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="280f0-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="280f0-167">xsd:double</span><span class="sxs-lookup"><span data-stu-id="280f0-167">xsd:double</span></span>  <br/> |<span data-ttu-id="280f0-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="280f0-168">optional</span></span>  <br/> ||<span data-ttu-id="280f0-169">xsd:double 型の値。</span><span class="sxs-lookup"><span data-stu-id="280f0-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="280f0-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="280f0-170">ViewScale</span></span>  <br/> |<span data-ttu-id="280f0-171">xsd:double</span><span class="sxs-lookup"><span data-stu-id="280f0-171">xsd:double</span></span>  <br/> |<span data-ttu-id="280f0-172">省略可能</span><span class="sxs-lookup"><span data-stu-id="280f0-172">optional</span></span>  <br/> ||<span data-ttu-id="280f0-173">xsd:double 型の値。</span><span class="sxs-lookup"><span data-stu-id="280f0-173">Values of the xsd:double type.</span></span>  <br/> |
   

