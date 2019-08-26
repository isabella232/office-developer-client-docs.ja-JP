---
title: DataColumn_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 7f35cd2ef1f6d710644033599fe4a90a0f2978ef
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541212"
---
# <a name="datacolumn_type-complextype-visio-xml"></a><span data-ttu-id="6fed5-102">DataColumn_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6fed5-102">DataColumn_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6fed5-103">型情報</span><span class="sxs-lookup"><span data-stu-id="6fed5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fed5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6fed5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6fed5-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6fed5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6fed5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6fed5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6fed5-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="6fed5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6fed5-108">なし</span><span class="sxs-lookup"><span data-stu-id="6fed5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6fed5-109">定義</span><span class="sxs-lookup"><span data-stu-id="6fed5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6fed5-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6fed5-110">Elements and attributes</span></span>

<span data-ttu-id="6fed5-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6fed5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6fed5-112">子要素</span><span class="sxs-lookup"><span data-stu-id="6fed5-112">Child elements</span></span>

<span data-ttu-id="6fed5-113">なし。</span><span class="sxs-lookup"><span data-stu-id="6fed5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6fed5-114">属性</span><span class="sxs-lookup"><span data-stu-id="6fed5-114">Attributes</span></span>

|<span data-ttu-id="6fed5-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="6fed5-115">**Attribute**</span></span>|<span data-ttu-id="6fed5-116">**型**</span><span class="sxs-lookup"><span data-stu-id="6fed5-116">**Type**</span></span>|<span data-ttu-id="6fed5-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="6fed5-117">**Required**</span></span>|<span data-ttu-id="6fed5-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="6fed5-118">**Description**</span></span>|<span data-ttu-id="6fed5-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="6fed5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6fed5-120">予定表</span><span class="sxs-lookup"><span data-stu-id="6fed5-120">Calendar</span></span>  <br/> |<span data-ttu-id="6fed5-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6fed5-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6fed5-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="6fed5-122">optional</span></span>  <br/> ||<span data-ttu-id="6fed5-123">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6fed5-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="6fed5-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="6fed5-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6fed5-125">xsd:string</span></span>  <br/> |<span data-ttu-id="6fed5-126">必須</span><span class="sxs-lookup"><span data-stu-id="6fed5-126">required</span></span>  <br/> ||<span data-ttu-id="6fed5-127">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6fed5-128">通貨</span><span class="sxs-lookup"><span data-stu-id="6fed5-128">Currency</span></span>  <br/> |<span data-ttu-id="6fed5-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6fed5-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6fed5-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="6fed5-130">optional</span></span>  <br/> ||<span data-ttu-id="6fed5-131">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6fed5-132">DataType</span><span class="sxs-lookup"><span data-stu-id="6fed5-132">DataType</span></span>  <br/> |<span data-ttu-id="6fed5-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6fed5-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6fed5-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="6fed5-134">optional</span></span>  <br/> ||<span data-ttu-id="6fed5-135">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6fed5-136">Degree</span><span class="sxs-lookup"><span data-stu-id="6fed5-136">Degree</span></span>  <br/> |<span data-ttu-id="6fed5-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6fed5-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6fed5-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="6fed5-138">optional</span></span>  <br/> ||<span data-ttu-id="6fed5-139">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6fed5-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="6fed5-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="6fed5-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6fed5-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6fed5-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="6fed5-142">optional</span></span>  <br/> ||<span data-ttu-id="6fed5-143">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6fed5-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="6fed5-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="6fed5-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6fed5-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6fed5-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="6fed5-146">optional</span></span>  <br/> ||<span data-ttu-id="6fed5-147">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6fed5-148">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="6fed5-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="6fed5-149">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6fed5-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6fed5-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="6fed5-150">optional</span></span>  <br/> ||<span data-ttu-id="6fed5-151">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6fed5-152">ラベル</span><span class="sxs-lookup"><span data-stu-id="6fed5-152">Label</span></span>  <br/> |<span data-ttu-id="6fed5-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6fed5-153">xsd:string</span></span>  <br/> |<span data-ttu-id="6fed5-154">必須</span><span class="sxs-lookup"><span data-stu-id="6fed5-154">required</span></span>  <br/> ||<span data-ttu-id="6fed5-155">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6fed5-156">LangID</span><span class="sxs-lookup"><span data-stu-id="6fed5-156">LangID</span></span>  <br/> |<span data-ttu-id="6fed5-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6fed5-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6fed5-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="6fed5-158">optional</span></span>  <br/> ||<span data-ttu-id="6fed5-159">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6fed5-160">マッピングされた</span><span class="sxs-lookup"><span data-stu-id="6fed5-160">Mapped CP</span></span>  <br/> |<span data-ttu-id="6fed5-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6fed5-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6fed5-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="6fed5-162">optional</span></span>  <br/> ||<span data-ttu-id="6fed5-163">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6fed5-164">名前</span><span class="sxs-lookup"><span data-stu-id="6fed5-164">Name</span></span>  <br/> |<span data-ttu-id="6fed5-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6fed5-165">xsd:string</span></span>  <br/> |<span data-ttu-id="6fed5-166">必須</span><span class="sxs-lookup"><span data-stu-id="6fed5-166">required</span></span>  <br/> ||<span data-ttu-id="6fed5-167">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6fed5-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="6fed5-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="6fed5-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6fed5-169">xsd:string</span></span>  <br/> |<span data-ttu-id="6fed5-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="6fed5-170">optional</span></span>  <br/> ||<span data-ttu-id="6fed5-171">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6fed5-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="6fed5-172">UnitType</span></span>  <br/> |<span data-ttu-id="6fed5-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6fed5-173">xsd:string</span></span>  <br/> |<span data-ttu-id="6fed5-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="6fed5-174">optional</span></span>  <br/> ||<span data-ttu-id="6fed5-175">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="6fed5-175">Values of the xsd:string type.</span></span>  <br/> |
   

