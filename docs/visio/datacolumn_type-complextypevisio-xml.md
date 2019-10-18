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
# <a name="datacolumn_type-complextype-visio-xml"></a><span data-ttu-id="cfbd2-102">DataColumn_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="cfbd2-102">DataColumn_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="cfbd2-103">型情報</span><span class="sxs-lookup"><span data-stu-id="cfbd2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cfbd2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cfbd2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cfbd2-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="cfbd2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cfbd2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cfbd2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cfbd2-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="cfbd2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cfbd2-108">なし</span><span class="sxs-lookup"><span data-stu-id="cfbd2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cfbd2-109">定義</span><span class="sxs-lookup"><span data-stu-id="cfbd2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cfbd2-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="cfbd2-110">Elements and attributes</span></span>

<span data-ttu-id="cfbd2-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cfbd2-112">子要素</span><span class="sxs-lookup"><span data-stu-id="cfbd2-112">Child elements</span></span>

<span data-ttu-id="cfbd2-113">なし。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cfbd2-114">属性</span><span class="sxs-lookup"><span data-stu-id="cfbd2-114">Attributes</span></span>

|<span data-ttu-id="cfbd2-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="cfbd2-115">**Attribute**</span></span>|<span data-ttu-id="cfbd2-116">**型**</span><span class="sxs-lookup"><span data-stu-id="cfbd2-116">**Type**</span></span>|<span data-ttu-id="cfbd2-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="cfbd2-117">**Required**</span></span>|<span data-ttu-id="cfbd2-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="cfbd2-118">**Description**</span></span>|<span data-ttu-id="cfbd2-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="cfbd2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cfbd2-120">予定表</span><span class="sxs-lookup"><span data-stu-id="cfbd2-120">Calendar</span></span>  <br/> |<span data-ttu-id="cfbd2-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="cfbd2-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cfbd2-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="cfbd2-122">optional</span></span>  <br/> ||<span data-ttu-id="cfbd2-123">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cfbd2-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="cfbd2-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="cfbd2-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cfbd2-125">xsd:string</span></span>  <br/> |<span data-ttu-id="cfbd2-126">必須</span><span class="sxs-lookup"><span data-stu-id="cfbd2-126">required</span></span>  <br/> ||<span data-ttu-id="cfbd2-127">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cfbd2-128">通貨</span><span class="sxs-lookup"><span data-stu-id="cfbd2-128">Currency</span></span>  <br/> |<span data-ttu-id="cfbd2-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="cfbd2-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cfbd2-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="cfbd2-130">optional</span></span>  <br/> ||<span data-ttu-id="cfbd2-131">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cfbd2-132">DataType</span><span class="sxs-lookup"><span data-stu-id="cfbd2-132">DataType</span></span>  <br/> |<span data-ttu-id="cfbd2-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="cfbd2-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cfbd2-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="cfbd2-134">optional</span></span>  <br/> ||<span data-ttu-id="cfbd2-135">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cfbd2-136">Degree</span><span class="sxs-lookup"><span data-stu-id="cfbd2-136">Degree</span></span>  <br/> |<span data-ttu-id="cfbd2-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cfbd2-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cfbd2-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="cfbd2-138">optional</span></span>  <br/> ||<span data-ttu-id="cfbd2-139">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cfbd2-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="cfbd2-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="cfbd2-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cfbd2-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cfbd2-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="cfbd2-142">optional</span></span>  <br/> ||<span data-ttu-id="cfbd2-143">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cfbd2-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="cfbd2-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="cfbd2-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cfbd2-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cfbd2-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="cfbd2-146">optional</span></span>  <br/> ||<span data-ttu-id="cfbd2-147">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cfbd2-148">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="cfbd2-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="cfbd2-149">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="cfbd2-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cfbd2-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="cfbd2-150">optional</span></span>  <br/> ||<span data-ttu-id="cfbd2-151">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cfbd2-152">ラベル</span><span class="sxs-lookup"><span data-stu-id="cfbd2-152">Label</span></span>  <br/> |<span data-ttu-id="cfbd2-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cfbd2-153">xsd:string</span></span>  <br/> |<span data-ttu-id="cfbd2-154">必須</span><span class="sxs-lookup"><span data-stu-id="cfbd2-154">required</span></span>  <br/> ||<span data-ttu-id="cfbd2-155">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cfbd2-156">LangID</span><span class="sxs-lookup"><span data-stu-id="cfbd2-156">LangID</span></span>  <br/> |<span data-ttu-id="cfbd2-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cfbd2-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cfbd2-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="cfbd2-158">optional</span></span>  <br/> ||<span data-ttu-id="cfbd2-159">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cfbd2-160">マッピングされた</span><span class="sxs-lookup"><span data-stu-id="cfbd2-160">Mapped CP</span></span>  <br/> |<span data-ttu-id="cfbd2-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="cfbd2-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cfbd2-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="cfbd2-162">optional</span></span>  <br/> ||<span data-ttu-id="cfbd2-163">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cfbd2-164">名前</span><span class="sxs-lookup"><span data-stu-id="cfbd2-164">Name</span></span>  <br/> |<span data-ttu-id="cfbd2-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cfbd2-165">xsd:string</span></span>  <br/> |<span data-ttu-id="cfbd2-166">必須</span><span class="sxs-lookup"><span data-stu-id="cfbd2-166">required</span></span>  <br/> ||<span data-ttu-id="cfbd2-167">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cfbd2-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="cfbd2-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="cfbd2-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cfbd2-169">xsd:string</span></span>  <br/> |<span data-ttu-id="cfbd2-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="cfbd2-170">optional</span></span>  <br/> ||<span data-ttu-id="cfbd2-171">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cfbd2-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="cfbd2-172">UnitType</span></span>  <br/> |<span data-ttu-id="cfbd2-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cfbd2-173">xsd:string</span></span>  <br/> |<span data-ttu-id="cfbd2-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="cfbd2-174">optional</span></span>  <br/> ||<span data-ttu-id="cfbd2-175">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="cfbd2-175">Values of the xsd:string type.</span></span>  <br/> |
   

