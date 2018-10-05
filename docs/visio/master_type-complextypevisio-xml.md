---
title: Master_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 186099d495849706f68113abb269de4a1f5a2ce7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397712"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="61e2b-102">Master_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="61e2b-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="61e2b-103">型情報</span><span class="sxs-lookup"><span data-stu-id="61e2b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61e2b-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="61e2b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="61e2b-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="61e2b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="61e2b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="61e2b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="61e2b-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="61e2b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="61e2b-108">なし</span><span class="sxs-lookup"><span data-stu-id="61e2b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="61e2b-109">定義</span><span class="sxs-lookup"><span data-stu-id="61e2b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="61e2b-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="61e2b-110">Elements and attributes</span></span>

<span data-ttu-id="61e2b-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="61e2b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="61e2b-112">子要素</span><span class="sxs-lookup"><span data-stu-id="61e2b-112">Child elements</span></span>

|<span data-ttu-id="61e2b-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="61e2b-113">**Element**</span></span>|<span data-ttu-id="61e2b-114">**型**</span><span class="sxs-lookup"><span data-stu-id="61e2b-114">**Type**</span></span>|<span data-ttu-id="61e2b-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="61e2b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61e2b-116">Icon</span><span class="sxs-lookup"><span data-stu-id="61e2b-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61e2b-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="61e2b-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="61e2b-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="61e2b-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61e2b-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="61e2b-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="61e2b-120">Rel</span><span class="sxs-lookup"><span data-stu-id="61e2b-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61e2b-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="61e2b-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="61e2b-122">属性</span><span class="sxs-lookup"><span data-stu-id="61e2b-122">Attributes</span></span>

|<span data-ttu-id="61e2b-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="61e2b-123">**Attribute**</span></span>|<span data-ttu-id="61e2b-124">**型**</span><span class="sxs-lookup"><span data-stu-id="61e2b-124">**Type**</span></span>|<span data-ttu-id="61e2b-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="61e2b-125">**Required**</span></span>|<span data-ttu-id="61e2b-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="61e2b-126">**Description**</span></span>|<span data-ttu-id="61e2b-127">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="61e2b-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="61e2b-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="61e2b-128">AlignName</span></span>  <br/> |<span data-ttu-id="61e2b-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="61e2b-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="61e2b-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-130">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-131">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="61e2b-132">BaseID</span></span>  <br/> |<span data-ttu-id="61e2b-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61e2b-133">xsd:string</span></span>  <br/> |<span data-ttu-id="61e2b-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-134">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-136">非表示</span><span class="sxs-lookup"><span data-stu-id="61e2b-136">Hidden</span></span>  <br/> |<span data-ttu-id="61e2b-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="61e2b-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="61e2b-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-138">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-139">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="61e2b-140">IconSize</span></span>  <br/> |<span data-ttu-id="61e2b-141">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="61e2b-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="61e2b-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-142">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-143">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="61e2b-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="61e2b-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="61e2b-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="61e2b-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-146">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-147">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-148">ID</span><span class="sxs-lookup"><span data-stu-id="61e2b-148">ID</span></span>  <br/> |<span data-ttu-id="61e2b-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61e2b-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61e2b-150">必須</span><span class="sxs-lookup"><span data-stu-id="61e2b-150">required</span></span>  <br/> ||<span data-ttu-id="61e2b-151">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="61e2b-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="61e2b-153">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="61e2b-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="61e2b-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-154">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-155">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="61e2b-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="61e2b-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="61e2b-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="61e2b-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-158">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-159">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="61e2b-160">MasterType</span></span>  <br/> |<span data-ttu-id="61e2b-161">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="61e2b-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="61e2b-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-162">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-163">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="61e2b-164">MatchByName</span></span>  <br/> |<span data-ttu-id="61e2b-165">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="61e2b-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="61e2b-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-166">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-167">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-168">名前</span><span class="sxs-lookup"><span data-stu-id="61e2b-168">Name</span></span>  <br/> |<span data-ttu-id="61e2b-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61e2b-169">xsd:string</span></span>  <br/> |<span data-ttu-id="61e2b-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-170">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-171">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-172">NameU</span><span class="sxs-lookup"><span data-stu-id="61e2b-172">NameU</span></span>  <br/> |<span data-ttu-id="61e2b-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61e2b-173">xsd:string</span></span>  <br/> |<span data-ttu-id="61e2b-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-174">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-175">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="61e2b-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="61e2b-177">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="61e2b-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="61e2b-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-178">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-179">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-180">プロンプト</span><span class="sxs-lookup"><span data-stu-id="61e2b-180">Prompt</span></span>  <br/> |<span data-ttu-id="61e2b-181">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61e2b-181">xsd:string</span></span>  <br/> |<span data-ttu-id="61e2b-182">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-182">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-183">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="61e2b-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="61e2b-184">UniqueID</span></span>  <br/> |<span data-ttu-id="61e2b-185">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61e2b-185">xsd:string</span></span>  <br/> |<span data-ttu-id="61e2b-186">省略可能</span><span class="sxs-lookup"><span data-stu-id="61e2b-186">optional</span></span>  <br/> ||<span data-ttu-id="61e2b-187">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61e2b-187">Values of the xsd:string type.</span></span>  <br/> |
   

