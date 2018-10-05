---
title: Page_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: d0c364164d2453c9dc64290db24890224a3c70e1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401553"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="6709b-102">Page_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="6709b-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6709b-103">型情報</span><span class="sxs-lookup"><span data-stu-id="6709b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6709b-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="6709b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6709b-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6709b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6709b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6709b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6709b-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="6709b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6709b-108">なし</span><span class="sxs-lookup"><span data-stu-id="6709b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6709b-109">定義</span><span class="sxs-lookup"><span data-stu-id="6709b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6709b-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6709b-110">Elements and attributes</span></span>

<span data-ttu-id="6709b-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6709b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6709b-112">子要素</span><span class="sxs-lookup"><span data-stu-id="6709b-112">Child elements</span></span>

|<span data-ttu-id="6709b-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="6709b-113">**Element**</span></span>|<span data-ttu-id="6709b-114">**型**</span><span class="sxs-lookup"><span data-stu-id="6709b-114">**Type**</span></span>|<span data-ttu-id="6709b-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="6709b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6709b-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="6709b-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6709b-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="6709b-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6709b-118">Rel</span><span class="sxs-lookup"><span data-stu-id="6709b-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6709b-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="6709b-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6709b-120">属性</span><span class="sxs-lookup"><span data-stu-id="6709b-120">Attributes</span></span>

|<span data-ttu-id="6709b-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="6709b-121">**Attribute**</span></span>|<span data-ttu-id="6709b-122">**型**</span><span class="sxs-lookup"><span data-stu-id="6709b-122">**Type**</span></span>|<span data-ttu-id="6709b-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="6709b-123">**Required**</span></span>|<span data-ttu-id="6709b-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="6709b-124">**Description**</span></span>|<span data-ttu-id="6709b-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="6709b-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6709b-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="6709b-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="6709b-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6709b-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6709b-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="6709b-128">optional</span></span>  <br/> ||<span data-ttu-id="6709b-129">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6709b-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6709b-130">背景</span><span class="sxs-lookup"><span data-stu-id="6709b-130">Background</span></span>  <br/> |<span data-ttu-id="6709b-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6709b-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6709b-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="6709b-132">optional</span></span>  <br/> ||<span data-ttu-id="6709b-133">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6709b-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6709b-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="6709b-134">BackPage</span></span>  <br/> |<span data-ttu-id="6709b-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6709b-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6709b-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="6709b-136">optional</span></span>  <br/> ||<span data-ttu-id="6709b-137">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6709b-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6709b-138">ID</span><span class="sxs-lookup"><span data-stu-id="6709b-138">ID</span></span>  <br/> |<span data-ttu-id="6709b-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6709b-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6709b-140">必須</span><span class="sxs-lookup"><span data-stu-id="6709b-140">required</span></span>  <br/> ||<span data-ttu-id="6709b-141">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6709b-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6709b-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="6709b-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="6709b-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6709b-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6709b-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="6709b-144">optional</span></span>  <br/> ||<span data-ttu-id="6709b-145">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6709b-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6709b-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="6709b-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="6709b-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6709b-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6709b-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="6709b-148">optional</span></span>  <br/> ||<span data-ttu-id="6709b-149">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6709b-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6709b-150">名前</span><span class="sxs-lookup"><span data-stu-id="6709b-150">Name</span></span>  <br/> |<span data-ttu-id="6709b-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6709b-151">xsd:string</span></span>  <br/> |<span data-ttu-id="6709b-152">省略可能</span><span class="sxs-lookup"><span data-stu-id="6709b-152">optional</span></span>  <br/> ||<span data-ttu-id="6709b-153">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6709b-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6709b-154">NameU</span><span class="sxs-lookup"><span data-stu-id="6709b-154">NameU</span></span>  <br/> |<span data-ttu-id="6709b-155">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6709b-155">xsd:string</span></span>  <br/> |<span data-ttu-id="6709b-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="6709b-156">optional</span></span>  <br/> ||<span data-ttu-id="6709b-157">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6709b-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6709b-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="6709b-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="6709b-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6709b-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6709b-160">省略可能</span><span class="sxs-lookup"><span data-stu-id="6709b-160">optional</span></span>  <br/> ||<span data-ttu-id="6709b-161">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6709b-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6709b-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="6709b-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="6709b-163">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6709b-163">xsd:double</span></span>  <br/> |<span data-ttu-id="6709b-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="6709b-164">optional</span></span>  <br/> ||<span data-ttu-id="6709b-165">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="6709b-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6709b-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="6709b-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="6709b-167">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6709b-167">xsd:double</span></span>  <br/> |<span data-ttu-id="6709b-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="6709b-168">optional</span></span>  <br/> ||<span data-ttu-id="6709b-169">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="6709b-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6709b-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="6709b-170">ViewScale</span></span>  <br/> |<span data-ttu-id="6709b-171">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6709b-171">xsd:double</span></span>  <br/> |<span data-ttu-id="6709b-172">省略可能</span><span class="sxs-lookup"><span data-stu-id="6709b-172">optional</span></span>  <br/> ||<span data-ttu-id="6709b-173">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="6709b-173">Values of the xsd:double type.</span></span>  <br/> |
   

