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
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="13977-102">Master_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="13977-102">Master_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="13977-103">型情報</span><span class="sxs-lookup"><span data-stu-id="13977-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13977-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="13977-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="13977-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="13977-105">**Schema file**</span></span> <br/> |<span data-ttu-id="13977-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="13977-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="13977-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="13977-107">**Extension base**</span></span> <br/> |<span data-ttu-id="13977-108">None</span><span class="sxs-lookup"><span data-stu-id="13977-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="13977-109">定義</span><span class="sxs-lookup"><span data-stu-id="13977-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="13977-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="13977-110">Elements and attributes</span></span>

<span data-ttu-id="13977-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="13977-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="13977-112">子要素</span><span class="sxs-lookup"><span data-stu-id="13977-112">Child elements</span></span>

|<span data-ttu-id="13977-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="13977-113">**Element**</span></span>|<span data-ttu-id="13977-114">**型**</span><span class="sxs-lookup"><span data-stu-id="13977-114">**Type**</span></span>|<span data-ttu-id="13977-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="13977-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="13977-116">Icon</span><span class="sxs-lookup"><span data-stu-id="13977-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13977-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="13977-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="13977-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="13977-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13977-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="13977-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="13977-120">Rel</span><span class="sxs-lookup"><span data-stu-id="13977-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13977-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="13977-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="13977-122">属性</span><span class="sxs-lookup"><span data-stu-id="13977-122">Attributes</span></span>

|<span data-ttu-id="13977-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="13977-123">**Attribute**</span></span>|<span data-ttu-id="13977-124">**型**</span><span class="sxs-lookup"><span data-stu-id="13977-124">**Type**</span></span>|<span data-ttu-id="13977-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="13977-125">**Required**</span></span>|<span data-ttu-id="13977-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="13977-126">**Description**</span></span>|<span data-ttu-id="13977-127">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="13977-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="13977-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="13977-128">AlignName</span></span>  <br/> |<span data-ttu-id="13977-129">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="13977-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="13977-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-130">optional</span></span>  <br/> ||<span data-ttu-id="13977-131">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="13977-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="13977-132">BaseID</span></span>  <br/> |<span data-ttu-id="13977-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="13977-133">xsd:string</span></span>  <br/> |<span data-ttu-id="13977-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-134">optional</span></span>  <br/> ||<span data-ttu-id="13977-135">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13977-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="13977-136">Hidden</span></span>  <br/> |<span data-ttu-id="13977-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="13977-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="13977-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-138">optional</span></span>  <br/> ||<span data-ttu-id="13977-139">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="13977-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="13977-140">IconSize</span></span>  <br/> |<span data-ttu-id="13977-141">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="13977-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="13977-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-142">optional</span></span>  <br/> ||<span data-ttu-id="13977-143">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="13977-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="13977-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="13977-145">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="13977-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="13977-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-146">optional</span></span>  <br/> ||<span data-ttu-id="13977-147">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="13977-148">ID</span><span class="sxs-lookup"><span data-stu-id="13977-148">ID</span></span>  <br/> |<span data-ttu-id="13977-149">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="13977-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="13977-150">必須</span><span class="sxs-lookup"><span data-stu-id="13977-150">required</span></span>  <br/> ||<span data-ttu-id="13977-151">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="13977-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="13977-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="13977-153">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="13977-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="13977-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-154">optional</span></span>  <br/> ||<span data-ttu-id="13977-155">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="13977-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="13977-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="13977-157">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="13977-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="13977-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-158">optional</span></span>  <br/> ||<span data-ttu-id="13977-159">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="13977-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="13977-160">MasterType</span></span>  <br/> |<span data-ttu-id="13977-161">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="13977-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="13977-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-162">optional</span></span>  <br/> ||<span data-ttu-id="13977-163">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="13977-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="13977-164">MatchByName</span></span>  <br/> |<span data-ttu-id="13977-165">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="13977-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="13977-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-166">optional</span></span>  <br/> ||<span data-ttu-id="13977-167">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="13977-168">名前</span><span class="sxs-lookup"><span data-stu-id="13977-168">Name</span></span>  <br/> |<span data-ttu-id="13977-169">xsd: string</span><span class="sxs-lookup"><span data-stu-id="13977-169">xsd:string</span></span>  <br/> |<span data-ttu-id="13977-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-170">optional</span></span>  <br/> ||<span data-ttu-id="13977-171">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13977-172">NameU</span><span class="sxs-lookup"><span data-stu-id="13977-172">NameU</span></span>  <br/> |<span data-ttu-id="13977-173">xsd: string</span><span class="sxs-lookup"><span data-stu-id="13977-173">xsd:string</span></span>  <br/> |<span data-ttu-id="13977-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-174">optional</span></span>  <br/> ||<span data-ttu-id="13977-175">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13977-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="13977-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="13977-177">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="13977-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="13977-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-178">optional</span></span>  <br/> ||<span data-ttu-id="13977-179">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="13977-180">プロンプト</span><span class="sxs-lookup"><span data-stu-id="13977-180">Prompt</span></span>  <br/> |<span data-ttu-id="13977-181">xsd: string</span><span class="sxs-lookup"><span data-stu-id="13977-181">xsd:string</span></span>  <br/> |<span data-ttu-id="13977-182">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-182">optional</span></span>  <br/> ||<span data-ttu-id="13977-183">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13977-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="13977-184">UniqueID</span></span>  <br/> |<span data-ttu-id="13977-185">xsd: string</span><span class="sxs-lookup"><span data-stu-id="13977-185">xsd:string</span></span>  <br/> |<span data-ttu-id="13977-186">省略可能</span><span class="sxs-lookup"><span data-stu-id="13977-186">optional</span></span>  <br/> ||<span data-ttu-id="13977-187">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="13977-187">Values of the xsd:string type.</span></span>  <br/> |
   

