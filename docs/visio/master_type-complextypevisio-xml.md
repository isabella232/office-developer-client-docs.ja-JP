---
title: Master_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 186099d495849706f68113abb269de4a1f5a2ce7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341805"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="c30d5-102">Master_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c30d5-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c30d5-103">型情報</span><span class="sxs-lookup"><span data-stu-id="c30d5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c30d5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c30d5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c30d5-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c30d5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c30d5-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="c30d5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c30d5-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="c30d5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c30d5-108">なし</span><span class="sxs-lookup"><span data-stu-id="c30d5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c30d5-109">定義</span><span class="sxs-lookup"><span data-stu-id="c30d5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c30d5-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c30d5-110">Elements and attributes</span></span>

<span data-ttu-id="c30d5-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c30d5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c30d5-112">子要素</span><span class="sxs-lookup"><span data-stu-id="c30d5-112">Child elements</span></span>

|<span data-ttu-id="c30d5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c30d5-113">**Element**</span></span>|<span data-ttu-id="c30d5-114">**型**</span><span class="sxs-lookup"><span data-stu-id="c30d5-114">**Type**</span></span>|<span data-ttu-id="c30d5-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="c30d5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c30d5-116">Icon</span><span class="sxs-lookup"><span data-stu-id="c30d5-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c30d5-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="c30d5-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c30d5-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="c30d5-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c30d5-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="c30d5-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c30d5-120">Rel</span><span class="sxs-lookup"><span data-stu-id="c30d5-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c30d5-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="c30d5-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c30d5-122">属性</span><span class="sxs-lookup"><span data-stu-id="c30d5-122">Attributes</span></span>

|<span data-ttu-id="c30d5-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="c30d5-123">**Attribute**</span></span>|<span data-ttu-id="c30d5-124">**型**</span><span class="sxs-lookup"><span data-stu-id="c30d5-124">**Type**</span></span>|<span data-ttu-id="c30d5-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="c30d5-125">**Required**</span></span>|<span data-ttu-id="c30d5-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="c30d5-126">**Description**</span></span>|<span data-ttu-id="c30d5-127">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="c30d5-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c30d5-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="c30d5-128">AlignName</span></span>  <br/> |<span data-ttu-id="c30d5-129">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="c30d5-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c30d5-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-130">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-131">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="c30d5-132">BaseID</span></span>  <br/> |<span data-ttu-id="c30d5-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="c30d5-133">xsd:string</span></span>  <br/> |<span data-ttu-id="c30d5-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-134">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-135">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="c30d5-136">Hidden</span></span>  <br/> |<span data-ttu-id="c30d5-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="c30d5-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c30d5-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-138">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-139">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="c30d5-140">IconSize</span></span>  <br/> |<span data-ttu-id="c30d5-141">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="c30d5-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c30d5-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-142">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-143">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="c30d5-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="c30d5-145">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="c30d5-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c30d5-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-146">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-147">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-148">ID</span><span class="sxs-lookup"><span data-stu-id="c30d5-148">ID</span></span>  <br/> |<span data-ttu-id="c30d5-149">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="c30d5-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c30d5-150">必須</span><span class="sxs-lookup"><span data-stu-id="c30d5-150">required</span></span>  <br/> ||<span data-ttu-id="c30d5-151">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-152">iscustomname</span><span class="sxs-lookup"><span data-stu-id="c30d5-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="c30d5-153">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="c30d5-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c30d5-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-154">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-155">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="c30d5-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="c30d5-157">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="c30d5-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c30d5-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-158">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-159">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="c30d5-160">MasterType</span></span>  <br/> |<span data-ttu-id="c30d5-161">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="c30d5-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c30d5-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-162">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-163">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="c30d5-164">MatchByName</span></span>  <br/> |<span data-ttu-id="c30d5-165">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="c30d5-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c30d5-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-166">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-167">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-168">名前</span><span class="sxs-lookup"><span data-stu-id="c30d5-168">Name</span></span>  <br/> |<span data-ttu-id="c30d5-169">xsd: string</span><span class="sxs-lookup"><span data-stu-id="c30d5-169">xsd:string</span></span>  <br/> |<span data-ttu-id="c30d5-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-170">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-171">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-172">NameU</span><span class="sxs-lookup"><span data-stu-id="c30d5-172">NameU</span></span>  <br/> |<span data-ttu-id="c30d5-173">xsd: string</span><span class="sxs-lookup"><span data-stu-id="c30d5-173">xsd:string</span></span>  <br/> |<span data-ttu-id="c30d5-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-174">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-175">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="c30d5-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="c30d5-177">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="c30d5-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c30d5-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-178">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-179">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-180">プロンプト</span><span class="sxs-lookup"><span data-stu-id="c30d5-180">Prompt</span></span>  <br/> |<span data-ttu-id="c30d5-181">xsd: string</span><span class="sxs-lookup"><span data-stu-id="c30d5-181">xsd:string</span></span>  <br/> |<span data-ttu-id="c30d5-182">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-182">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-183">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c30d5-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="c30d5-184">UniqueID</span></span>  <br/> |<span data-ttu-id="c30d5-185">xsd: string</span><span class="sxs-lookup"><span data-stu-id="c30d5-185">xsd:string</span></span>  <br/> |<span data-ttu-id="c30d5-186">省略可能</span><span class="sxs-lookup"><span data-stu-id="c30d5-186">optional</span></span>  <br/> ||<span data-ttu-id="c30d5-187">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c30d5-187">Values of the xsd:string type.</span></span>  <br/> |
   

