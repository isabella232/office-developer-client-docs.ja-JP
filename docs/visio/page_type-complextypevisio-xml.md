---
title: Page_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: b3a4916f3de20d9350b6673a6000d56f3030b66e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805950"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="28cc3-102">Page_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="28cc3-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="28cc3-103">型情報</span><span class="sxs-lookup"><span data-stu-id="28cc3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28cc3-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="28cc3-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="28cc3-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="28cc3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="28cc3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="28cc3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="28cc3-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="28cc3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="28cc3-108">なし</span><span class="sxs-lookup"><span data-stu-id="28cc3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="28cc3-109">定義</span><span class="sxs-lookup"><span data-stu-id="28cc3-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="28cc3-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="28cc3-110">Elements and attributes</span></span>

<span data-ttu-id="28cc3-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="28cc3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="28cc3-112">子要素</span><span class="sxs-lookup"><span data-stu-id="28cc3-112">Child elements</span></span>

|<span data-ttu-id="28cc3-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="28cc3-113">**Element**</span></span>|<span data-ttu-id="28cc3-114">**型**</span><span class="sxs-lookup"><span data-stu-id="28cc3-114">**Type**</span></span>|<span data-ttu-id="28cc3-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="28cc3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="28cc3-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="28cc3-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="28cc3-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="28cc3-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="28cc3-118">Rel</span><span class="sxs-lookup"><span data-stu-id="28cc3-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="28cc3-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="28cc3-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="28cc3-120">属性</span><span class="sxs-lookup"><span data-stu-id="28cc3-120">Attributes</span></span>

|<span data-ttu-id="28cc3-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="28cc3-121">**Attribute**</span></span>|<span data-ttu-id="28cc3-122">**型**</span><span class="sxs-lookup"><span data-stu-id="28cc3-122">**Type**</span></span>|<span data-ttu-id="28cc3-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="28cc3-123">**Required**</span></span>|<span data-ttu-id="28cc3-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="28cc3-124">**Description**</span></span>|<span data-ttu-id="28cc3-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="28cc3-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="28cc3-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="28cc3-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="28cc3-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="28cc3-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28cc3-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="28cc3-128">optional</span></span>  <br/> ||<span data-ttu-id="28cc3-129">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cc3-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28cc3-130">背景</span><span class="sxs-lookup"><span data-stu-id="28cc3-130">Background</span></span>  <br/> |<span data-ttu-id="28cc3-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="28cc3-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="28cc3-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="28cc3-132">optional</span></span>  <br/> ||<span data-ttu-id="28cc3-133">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cc3-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="28cc3-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="28cc3-134">BackPage</span></span>  <br/> |<span data-ttu-id="28cc3-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="28cc3-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28cc3-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="28cc3-136">optional</span></span>  <br/> ||<span data-ttu-id="28cc3-137">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cc3-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28cc3-138">ID</span><span class="sxs-lookup"><span data-stu-id="28cc3-138">ID</span></span>  <br/> |<span data-ttu-id="28cc3-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="28cc3-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28cc3-140">必須</span><span class="sxs-lookup"><span data-stu-id="28cc3-140">required</span></span>  <br/> ||<span data-ttu-id="28cc3-141">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cc3-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28cc3-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="28cc3-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="28cc3-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="28cc3-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="28cc3-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="28cc3-144">optional</span></span>  <br/> ||<span data-ttu-id="28cc3-145">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cc3-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="28cc3-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="28cc3-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="28cc3-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="28cc3-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="28cc3-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="28cc3-148">optional</span></span>  <br/> ||<span data-ttu-id="28cc3-149">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cc3-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="28cc3-150">名前</span><span class="sxs-lookup"><span data-stu-id="28cc3-150">Name</span></span>  <br/> |<span data-ttu-id="28cc3-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="28cc3-151">xsd:string</span></span>  <br/> |<span data-ttu-id="28cc3-152">省略可能</span><span class="sxs-lookup"><span data-stu-id="28cc3-152">optional</span></span>  <br/> ||<span data-ttu-id="28cc3-153">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cc3-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="28cc3-154">NameU</span><span class="sxs-lookup"><span data-stu-id="28cc3-154">NameU</span></span>  <br/> |<span data-ttu-id="28cc3-155">xsd:string</span><span class="sxs-lookup"><span data-stu-id="28cc3-155">xsd:string</span></span>  <br/> |<span data-ttu-id="28cc3-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="28cc3-156">optional</span></span>  <br/> ||<span data-ttu-id="28cc3-157">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cc3-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="28cc3-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="28cc3-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="28cc3-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="28cc3-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28cc3-160">省略可能</span><span class="sxs-lookup"><span data-stu-id="28cc3-160">optional</span></span>  <br/> ||<span data-ttu-id="28cc3-161">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cc3-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28cc3-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="28cc3-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="28cc3-163">xsd:double</span><span class="sxs-lookup"><span data-stu-id="28cc3-163">xsd:double</span></span>  <br/> |<span data-ttu-id="28cc3-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="28cc3-164">optional</span></span>  <br/> ||<span data-ttu-id="28cc3-165">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="28cc3-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="28cc3-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="28cc3-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="28cc3-167">xsd:double</span><span class="sxs-lookup"><span data-stu-id="28cc3-167">xsd:double</span></span>  <br/> |<span data-ttu-id="28cc3-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="28cc3-168">optional</span></span>  <br/> ||<span data-ttu-id="28cc3-169">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="28cc3-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="28cc3-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="28cc3-170">ViewScale</span></span>  <br/> |<span data-ttu-id="28cc3-171">xsd:double</span><span class="sxs-lookup"><span data-stu-id="28cc3-171">xsd:double</span></span>  <br/> |<span data-ttu-id="28cc3-172">省略可能</span><span class="sxs-lookup"><span data-stu-id="28cc3-172">optional</span></span>  <br/> ||<span data-ttu-id="28cc3-173">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="28cc3-173">Values of the xsd:double type.</span></span>  <br/> |
   

