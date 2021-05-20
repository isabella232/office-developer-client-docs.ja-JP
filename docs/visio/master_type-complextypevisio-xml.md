---
title: Master_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 22b619149fc5393f085ca6e245c65ed6058538ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538068"
---
# <a name="master_type-complextype-visio-xml"></a><span data-ttu-id="49967-102">Master_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="49967-102">Master_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="49967-103">型情報</span><span class="sxs-lookup"><span data-stu-id="49967-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49967-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="49967-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="49967-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="49967-105">**Schema file**</span></span> <br/> |<span data-ttu-id="49967-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="49967-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="49967-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="49967-107">**Extension base**</span></span> <br/> |<span data-ttu-id="49967-108">なし</span><span class="sxs-lookup"><span data-stu-id="49967-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="49967-109">定義</span><span class="sxs-lookup"><span data-stu-id="49967-109">Definition</span></span>

```XML
          <xs:complexType name="Master_Type">
          
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
    
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="BaseID"
  type="xsd:string"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="MatchByName"
  type="xsd:boolean"
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
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="Hidden"
  type="xsd:boolean"
    />
    <xs:attribute name="IconUpdate"
  type="xsd:boolean"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="49967-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="49967-110">Elements and attributes</span></span>

<span data-ttu-id="49967-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="49967-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="49967-112">子要素</span><span class="sxs-lookup"><span data-stu-id="49967-112">Child elements</span></span>

|<span data-ttu-id="49967-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="49967-113">**Element**</span></span>|<span data-ttu-id="49967-114">**型**</span><span class="sxs-lookup"><span data-stu-id="49967-114">**Type**</span></span>|<span data-ttu-id="49967-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="49967-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="49967-116">Icon</span><span class="sxs-lookup"><span data-stu-id="49967-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="49967-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="49967-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="49967-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="49967-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="49967-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="49967-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="49967-120">Rel</span><span class="sxs-lookup"><span data-stu-id="49967-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="49967-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="49967-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="49967-122">属性</span><span class="sxs-lookup"><span data-stu-id="49967-122">Attributes</span></span>

|<span data-ttu-id="49967-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="49967-123">**Attribute**</span></span>|<span data-ttu-id="49967-124">**型**</span><span class="sxs-lookup"><span data-stu-id="49967-124">**Type**</span></span>|<span data-ttu-id="49967-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="49967-125">**Required**</span></span>|<span data-ttu-id="49967-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="49967-126">**Description**</span></span>|<span data-ttu-id="49967-127">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="49967-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="49967-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="49967-128">AlignName</span></span>  <br/> |<span data-ttu-id="49967-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="49967-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="49967-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-130">optional</span></span>  <br/> ||<span data-ttu-id="49967-131">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="49967-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="49967-132">BaseID</span></span>  <br/> |<span data-ttu-id="49967-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="49967-133">xsd:string</span></span>  <br/> |<span data-ttu-id="49967-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-134">optional</span></span>  <br/> ||<span data-ttu-id="49967-135">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="49967-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="49967-136">Hidden</span></span>  <br/> |<span data-ttu-id="49967-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="49967-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="49967-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-138">optional</span></span>  <br/> ||<span data-ttu-id="49967-139">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="49967-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="49967-140">IconSize</span></span>  <br/> |<span data-ttu-id="49967-141">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="49967-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="49967-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-142">optional</span></span>  <br/> ||<span data-ttu-id="49967-143">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="49967-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="49967-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="49967-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="49967-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="49967-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-146">optional</span></span>  <br/> ||<span data-ttu-id="49967-147">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="49967-148">ID</span><span class="sxs-lookup"><span data-stu-id="49967-148">ID</span></span>  <br/> |<span data-ttu-id="49967-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="49967-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="49967-150">必須</span><span class="sxs-lookup"><span data-stu-id="49967-150">required</span></span>  <br/> ||<span data-ttu-id="49967-151">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="49967-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="49967-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="49967-153">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="49967-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="49967-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-154">optional</span></span>  <br/> ||<span data-ttu-id="49967-155">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="49967-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="49967-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="49967-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="49967-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="49967-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-158">optional</span></span>  <br/> ||<span data-ttu-id="49967-159">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="49967-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="49967-160">MasterType</span></span>  <br/> |<span data-ttu-id="49967-161">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="49967-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="49967-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-162">optional</span></span>  <br/> ||<span data-ttu-id="49967-163">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="49967-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="49967-164">MatchByName</span></span>  <br/> |<span data-ttu-id="49967-165">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="49967-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="49967-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-166">optional</span></span>  <br/> ||<span data-ttu-id="49967-167">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="49967-168">名前</span><span class="sxs-lookup"><span data-stu-id="49967-168">Name</span></span>  <br/> |<span data-ttu-id="49967-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="49967-169">xsd:string</span></span>  <br/> |<span data-ttu-id="49967-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-170">optional</span></span>  <br/> ||<span data-ttu-id="49967-171">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="49967-172">NameU</span><span class="sxs-lookup"><span data-stu-id="49967-172">NameU</span></span>  <br/> |<span data-ttu-id="49967-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="49967-173">xsd:string</span></span>  <br/> |<span data-ttu-id="49967-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-174">optional</span></span>  <br/> ||<span data-ttu-id="49967-175">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="49967-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="49967-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="49967-177">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="49967-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="49967-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-178">optional</span></span>  <br/> ||<span data-ttu-id="49967-179">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="49967-180">プロンプト</span><span class="sxs-lookup"><span data-stu-id="49967-180">Prompt</span></span>  <br/> |<span data-ttu-id="49967-181">xsd:string</span><span class="sxs-lookup"><span data-stu-id="49967-181">xsd:string</span></span>  <br/> |<span data-ttu-id="49967-182">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-182">optional</span></span>  <br/> ||<span data-ttu-id="49967-183">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="49967-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="49967-184">UniqueID</span></span>  <br/> |<span data-ttu-id="49967-185">xsd:string</span><span class="sxs-lookup"><span data-stu-id="49967-185">xsd:string</span></span>  <br/> |<span data-ttu-id="49967-186">省略可能</span><span class="sxs-lookup"><span data-stu-id="49967-186">optional</span></span>  <br/> ||<span data-ttu-id="49967-187">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="49967-187">Values of the xsd:string type.</span></span>  <br/> |
   

