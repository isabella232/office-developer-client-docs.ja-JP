---
title: Page_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: d0c364164d2453c9dc64290db24890224a3c70e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334399"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="52d56-102">Page_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="52d56-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="52d56-103">型情報</span><span class="sxs-lookup"><span data-stu-id="52d56-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52d56-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="52d56-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="52d56-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="52d56-105">**Schema file**</span></span> <br/> |<span data-ttu-id="52d56-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="52d56-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="52d56-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="52d56-107">**Extension base**</span></span> <br/> |<span data-ttu-id="52d56-108">なし</span><span class="sxs-lookup"><span data-stu-id="52d56-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="52d56-109">定義</span><span class="sxs-lookup"><span data-stu-id="52d56-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="52d56-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="52d56-110">Elements and attributes</span></span>

<span data-ttu-id="52d56-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="52d56-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="52d56-112">子要素</span><span class="sxs-lookup"><span data-stu-id="52d56-112">Child elements</span></span>

|<span data-ttu-id="52d56-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="52d56-113">**Element**</span></span>|<span data-ttu-id="52d56-114">**型**</span><span class="sxs-lookup"><span data-stu-id="52d56-114">**Type**</span></span>|<span data-ttu-id="52d56-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="52d56-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="52d56-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="52d56-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="52d56-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="52d56-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="52d56-118">Rel</span><span class="sxs-lookup"><span data-stu-id="52d56-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="52d56-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="52d56-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="52d56-120">属性</span><span class="sxs-lookup"><span data-stu-id="52d56-120">Attributes</span></span>

|<span data-ttu-id="52d56-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="52d56-121">**Attribute**</span></span>|<span data-ttu-id="52d56-122">**型**</span><span class="sxs-lookup"><span data-stu-id="52d56-122">**Type**</span></span>|<span data-ttu-id="52d56-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="52d56-123">**Required**</span></span>|<span data-ttu-id="52d56-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="52d56-124">**Description**</span></span>|<span data-ttu-id="52d56-125">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="52d56-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="52d56-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="52d56-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="52d56-127">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="52d56-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="52d56-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="52d56-128">optional</span></span>  <br/> ||<span data-ttu-id="52d56-129">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="52d56-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="52d56-130">背景</span><span class="sxs-lookup"><span data-stu-id="52d56-130">Background</span></span>  <br/> |<span data-ttu-id="52d56-131">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="52d56-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="52d56-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="52d56-132">optional</span></span>  <br/> ||<span data-ttu-id="52d56-133">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="52d56-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="52d56-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="52d56-134">BackPage</span></span>  <br/> |<span data-ttu-id="52d56-135">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="52d56-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="52d56-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="52d56-136">optional</span></span>  <br/> ||<span data-ttu-id="52d56-137">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="52d56-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="52d56-138">ID</span><span class="sxs-lookup"><span data-stu-id="52d56-138">ID</span></span>  <br/> |<span data-ttu-id="52d56-139">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="52d56-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="52d56-140">必須</span><span class="sxs-lookup"><span data-stu-id="52d56-140">required</span></span>  <br/> ||<span data-ttu-id="52d56-141">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="52d56-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="52d56-142">iscustomname</span><span class="sxs-lookup"><span data-stu-id="52d56-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="52d56-143">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="52d56-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="52d56-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="52d56-144">optional</span></span>  <br/> ||<span data-ttu-id="52d56-145">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="52d56-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="52d56-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="52d56-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="52d56-147">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="52d56-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="52d56-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="52d56-148">optional</span></span>  <br/> ||<span data-ttu-id="52d56-149">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="52d56-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="52d56-150">名前</span><span class="sxs-lookup"><span data-stu-id="52d56-150">Name</span></span>  <br/> |<span data-ttu-id="52d56-151">xsd: string</span><span class="sxs-lookup"><span data-stu-id="52d56-151">xsd:string</span></span>  <br/> |<span data-ttu-id="52d56-152">省略可能</span><span class="sxs-lookup"><span data-stu-id="52d56-152">optional</span></span>  <br/> ||<span data-ttu-id="52d56-153">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="52d56-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="52d56-154">NameU</span><span class="sxs-lookup"><span data-stu-id="52d56-154">NameU</span></span>  <br/> |<span data-ttu-id="52d56-155">xsd: string</span><span class="sxs-lookup"><span data-stu-id="52d56-155">xsd:string</span></span>  <br/> |<span data-ttu-id="52d56-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="52d56-156">optional</span></span>  <br/> ||<span data-ttu-id="52d56-157">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="52d56-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="52d56-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="52d56-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="52d56-159">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="52d56-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="52d56-160">省略可能</span><span class="sxs-lookup"><span data-stu-id="52d56-160">optional</span></span>  <br/> ||<span data-ttu-id="52d56-161">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="52d56-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="52d56-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="52d56-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="52d56-163">xsd: double</span><span class="sxs-lookup"><span data-stu-id="52d56-163">xsd:double</span></span>  <br/> |<span data-ttu-id="52d56-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="52d56-164">optional</span></span>  <br/> ||<span data-ttu-id="52d56-165">xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="52d56-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="52d56-166">view中央 y</span><span class="sxs-lookup"><span data-stu-id="52d56-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="52d56-167">xsd: double</span><span class="sxs-lookup"><span data-stu-id="52d56-167">xsd:double</span></span>  <br/> |<span data-ttu-id="52d56-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="52d56-168">optional</span></span>  <br/> ||<span data-ttu-id="52d56-169">xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="52d56-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="52d56-170">viewscale</span><span class="sxs-lookup"><span data-stu-id="52d56-170">ViewScale</span></span>  <br/> |<span data-ttu-id="52d56-171">xsd: double</span><span class="sxs-lookup"><span data-stu-id="52d56-171">xsd:double</span></span>  <br/> |<span data-ttu-id="52d56-172">省略可能</span><span class="sxs-lookup"><span data-stu-id="52d56-172">optional</span></span>  <br/> ||<span data-ttu-id="52d56-173">xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="52d56-173">Values of the xsd:double type.</span></span>  <br/> |
   

