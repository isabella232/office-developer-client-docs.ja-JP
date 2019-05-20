---
title: CellDef_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344703"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="e664d-102">CellDef_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="e664d-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e664d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="e664d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e664d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e664d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e664d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e664d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e664d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e664d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e664d-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="e664d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e664d-108">なし</span><span class="sxs-lookup"><span data-stu-id="e664d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e664d-109">定義</span><span class="sxs-lookup"><span data-stu-id="e664d-109">Definition</span></span>

```XML
      <xs:complexType name="DataColumn_Type">
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Label"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="OrigLabel"
  type="xsd:string"
    />
    <xs:attribute name="LangID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Calendar"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="DataType"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="UnitType"
  type="xsd:string"
    />
    <xs:attribute name="Currency"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Degree"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayOrder"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Mapped"
  type="xsd:boolean"
    />
    <xs:attribute name="Hyperlink"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e664d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e664d-110">Elements and attributes</span></span>

<span data-ttu-id="e664d-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e664d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e664d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="e664d-112">Child elements</span></span>

<span data-ttu-id="e664d-113">なし。</span><span class="sxs-lookup"><span data-stu-id="e664d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e664d-114">属性</span><span class="sxs-lookup"><span data-stu-id="e664d-114">Attributes</span></span>

|<span data-ttu-id="e664d-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="e664d-115">**Attribute**</span></span>|<span data-ttu-id="e664d-116">**型**</span><span class="sxs-lookup"><span data-stu-id="e664d-116">**Type**</span></span>|<span data-ttu-id="e664d-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="e664d-117">**Required**</span></span>|<span data-ttu-id="e664d-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="e664d-118">**Description**</span></span>|<span data-ttu-id="e664d-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="e664d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e664d-120">予定表</span><span class="sxs-lookup"><span data-stu-id="e664d-120">Calendar</span></span>  <br/> |<span data-ttu-id="e664d-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="e664d-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="e664d-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="e664d-122">optional</span></span>  <br/> ||<span data-ttu-id="e664d-123">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="e664d-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="e664d-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="e664d-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e664d-125">xsd:string</span></span>  <br/> |<span data-ttu-id="e664d-126">必須</span><span class="sxs-lookup"><span data-stu-id="e664d-126">required</span></span>  <br/> ||<span data-ttu-id="e664d-127">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e664d-128">通貨</span><span class="sxs-lookup"><span data-stu-id="e664d-128">Currency</span></span>  <br/> |<span data-ttu-id="e664d-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="e664d-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="e664d-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="e664d-130">optional</span></span>  <br/> ||<span data-ttu-id="e664d-131">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="e664d-132">DataType</span><span class="sxs-lookup"><span data-stu-id="e664d-132">DataType</span></span>  <br/> |<span data-ttu-id="e664d-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="e664d-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="e664d-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="e664d-134">optional</span></span>  <br/> ||<span data-ttu-id="e664d-135">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="e664d-136">Degree</span><span class="sxs-lookup"><span data-stu-id="e664d-136">Degree</span></span>  <br/> |<span data-ttu-id="e664d-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e664d-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e664d-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="e664d-138">optional</span></span>  <br/> ||<span data-ttu-id="e664d-139">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e664d-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="e664d-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="e664d-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e664d-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e664d-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="e664d-142">optional</span></span>  <br/> ||<span data-ttu-id="e664d-143">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e664d-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="e664d-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="e664d-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e664d-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e664d-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="e664d-146">optional</span></span>  <br/> ||<span data-ttu-id="e664d-147">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e664d-148">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="e664d-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="e664d-149">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e664d-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e664d-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="e664d-150">optional</span></span>  <br/> ||<span data-ttu-id="e664d-151">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e664d-152">ラベル</span><span class="sxs-lookup"><span data-stu-id="e664d-152">Label</span></span>  <br/> |<span data-ttu-id="e664d-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e664d-153">xsd:string</span></span>  <br/> |<span data-ttu-id="e664d-154">必須</span><span class="sxs-lookup"><span data-stu-id="e664d-154">required</span></span>  <br/> ||<span data-ttu-id="e664d-155">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e664d-156">LangID</span><span class="sxs-lookup"><span data-stu-id="e664d-156">LangID</span></span>  <br/> |<span data-ttu-id="e664d-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e664d-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e664d-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="e664d-158">optional</span></span>  <br/> ||<span data-ttu-id="e664d-159">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e664d-160">マッピングされた</span><span class="sxs-lookup"><span data-stu-id="e664d-160">Mapped CP</span></span>  <br/> |<span data-ttu-id="e664d-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e664d-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e664d-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="e664d-162">optional</span></span>  <br/> ||<span data-ttu-id="e664d-163">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e664d-164">名前</span><span class="sxs-lookup"><span data-stu-id="e664d-164">Name</span></span>  <br/> |<span data-ttu-id="e664d-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e664d-165">xsd:string</span></span>  <br/> |<span data-ttu-id="e664d-166">必須</span><span class="sxs-lookup"><span data-stu-id="e664d-166">required</span></span>  <br/> ||<span data-ttu-id="e664d-167">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e664d-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="e664d-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="e664d-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e664d-169">xsd:string</span></span>  <br/> |<span data-ttu-id="e664d-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="e664d-170">optional</span></span>  <br/> ||<span data-ttu-id="e664d-171">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e664d-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="e664d-172">UnitType</span></span>  <br/> |<span data-ttu-id="e664d-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e664d-173">xsd:string</span></span>  <br/> |<span data-ttu-id="e664d-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="e664d-174">optional</span></span>  <br/> ||<span data-ttu-id="e664d-175">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="e664d-175">Values of the xsd:string type.</span></span>  <br/> |
   

