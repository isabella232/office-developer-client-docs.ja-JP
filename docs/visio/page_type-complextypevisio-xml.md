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
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="3f4ef-102">Page_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="3f4ef-102">Page_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="3f4ef-103">型情報</span><span class="sxs-lookup"><span data-stu-id="3f4ef-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f4ef-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3f4ef-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3f4ef-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="3f4ef-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3f4ef-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="3f4ef-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3f4ef-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="3f4ef-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3f4ef-108">None</span><span class="sxs-lookup"><span data-stu-id="3f4ef-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3f4ef-109">定義</span><span class="sxs-lookup"><span data-stu-id="3f4ef-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3f4ef-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="3f4ef-110">Elements and attributes</span></span>

<span data-ttu-id="3f4ef-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f4ef-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3f4ef-112">子要素</span><span class="sxs-lookup"><span data-stu-id="3f4ef-112">Child elements</span></span>

|<span data-ttu-id="3f4ef-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f4ef-113">**Element**</span></span>|<span data-ttu-id="3f4ef-114">**型**</span><span class="sxs-lookup"><span data-stu-id="3f4ef-114">**Type**</span></span>|<span data-ttu-id="3f4ef-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="3f4ef-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3f4ef-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="3f4ef-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3f4ef-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="3f4ef-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3f4ef-118">Rel</span><span class="sxs-lookup"><span data-stu-id="3f4ef-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3f4ef-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="3f4ef-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3f4ef-120">属性</span><span class="sxs-lookup"><span data-stu-id="3f4ef-120">Attributes</span></span>

|<span data-ttu-id="3f4ef-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="3f4ef-121">**Attribute**</span></span>|<span data-ttu-id="3f4ef-122">**型**</span><span class="sxs-lookup"><span data-stu-id="3f4ef-122">**Type**</span></span>|<span data-ttu-id="3f4ef-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="3f4ef-123">**Required**</span></span>|<span data-ttu-id="3f4ef-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="3f4ef-124">**Description**</span></span>|<span data-ttu-id="3f4ef-125">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="3f4ef-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3f4ef-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="3f4ef-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="3f4ef-127">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="3f4ef-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3f4ef-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="3f4ef-128">optional</span></span>  <br/> ||<span data-ttu-id="3f4ef-129">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="3f4ef-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3f4ef-130">背景</span><span class="sxs-lookup"><span data-stu-id="3f4ef-130">Background</span></span>  <br/> |<span data-ttu-id="3f4ef-131">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="3f4ef-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3f4ef-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="3f4ef-132">optional</span></span>  <br/> ||<span data-ttu-id="3f4ef-133">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="3f4ef-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3f4ef-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="3f4ef-134">BackPage</span></span>  <br/> |<span data-ttu-id="3f4ef-135">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="3f4ef-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3f4ef-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="3f4ef-136">optional</span></span>  <br/> ||<span data-ttu-id="3f4ef-137">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="3f4ef-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3f4ef-138">ID</span><span class="sxs-lookup"><span data-stu-id="3f4ef-138">ID</span></span>  <br/> |<span data-ttu-id="3f4ef-139">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="3f4ef-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3f4ef-140">必須</span><span class="sxs-lookup"><span data-stu-id="3f4ef-140">required</span></span>  <br/> ||<span data-ttu-id="3f4ef-141">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="3f4ef-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3f4ef-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="3f4ef-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="3f4ef-143">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="3f4ef-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3f4ef-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="3f4ef-144">optional</span></span>  <br/> ||<span data-ttu-id="3f4ef-145">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="3f4ef-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3f4ef-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="3f4ef-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="3f4ef-147">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="3f4ef-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3f4ef-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="3f4ef-148">optional</span></span>  <br/> ||<span data-ttu-id="3f4ef-149">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="3f4ef-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3f4ef-150">名前</span><span class="sxs-lookup"><span data-stu-id="3f4ef-150">Name</span></span>  <br/> |<span data-ttu-id="3f4ef-151">xsd: string</span><span class="sxs-lookup"><span data-stu-id="3f4ef-151">xsd:string</span></span>  <br/> |<span data-ttu-id="3f4ef-152">省略可能</span><span class="sxs-lookup"><span data-stu-id="3f4ef-152">optional</span></span>  <br/> ||<span data-ttu-id="3f4ef-153">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="3f4ef-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3f4ef-154">NameU</span><span class="sxs-lookup"><span data-stu-id="3f4ef-154">NameU</span></span>  <br/> |<span data-ttu-id="3f4ef-155">xsd: string</span><span class="sxs-lookup"><span data-stu-id="3f4ef-155">xsd:string</span></span>  <br/> |<span data-ttu-id="3f4ef-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="3f4ef-156">optional</span></span>  <br/> ||<span data-ttu-id="3f4ef-157">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="3f4ef-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3f4ef-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="3f4ef-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="3f4ef-159">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="3f4ef-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3f4ef-160">省略可能</span><span class="sxs-lookup"><span data-stu-id="3f4ef-160">optional</span></span>  <br/> ||<span data-ttu-id="3f4ef-161">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="3f4ef-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3f4ef-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="3f4ef-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="3f4ef-163">xsd: double</span><span class="sxs-lookup"><span data-stu-id="3f4ef-163">xsd:double</span></span>  <br/> |<span data-ttu-id="3f4ef-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="3f4ef-164">optional</span></span>  <br/> ||<span data-ttu-id="3f4ef-165">Xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="3f4ef-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="3f4ef-166">View中央 y</span><span class="sxs-lookup"><span data-stu-id="3f4ef-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="3f4ef-167">xsd: double</span><span class="sxs-lookup"><span data-stu-id="3f4ef-167">xsd:double</span></span>  <br/> |<span data-ttu-id="3f4ef-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="3f4ef-168">optional</span></span>  <br/> ||<span data-ttu-id="3f4ef-169">Xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="3f4ef-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="3f4ef-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="3f4ef-170">ViewScale</span></span>  <br/> |<span data-ttu-id="3f4ef-171">xsd: double</span><span class="sxs-lookup"><span data-stu-id="3f4ef-171">xsd:double</span></span>  <br/> |<span data-ttu-id="3f4ef-172">省略可能</span><span class="sxs-lookup"><span data-stu-id="3f4ef-172">optional</span></span>  <br/> ||<span data-ttu-id="3f4ef-173">Xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="3f4ef-173">Values of the xsd:double type.</span></span>  <br/> |
   

