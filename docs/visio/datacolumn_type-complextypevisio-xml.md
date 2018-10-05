---
title: DataColumn_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388659"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="228ad-102">DataColumn_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="228ad-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="228ad-103">型情報</span><span class="sxs-lookup"><span data-stu-id="228ad-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="228ad-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="228ad-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="228ad-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="228ad-105">**Schema file**</span></span> <br/> |<span data-ttu-id="228ad-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="228ad-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="228ad-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="228ad-107">**Extension base**</span></span> <br/> |<span data-ttu-id="228ad-108">なし</span><span class="sxs-lookup"><span data-stu-id="228ad-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="228ad-109">定義</span><span class="sxs-lookup"><span data-stu-id="228ad-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="228ad-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="228ad-110">Elements and attributes</span></span>

<span data-ttu-id="228ad-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="228ad-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="228ad-112">子要素</span><span class="sxs-lookup"><span data-stu-id="228ad-112">Child elements</span></span>

<span data-ttu-id="228ad-113">なし。</span><span class="sxs-lookup"><span data-stu-id="228ad-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="228ad-114">属性</span><span class="sxs-lookup"><span data-stu-id="228ad-114">Attributes</span></span>

|<span data-ttu-id="228ad-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="228ad-115">**Attribute**</span></span>|<span data-ttu-id="228ad-116">**型**</span><span class="sxs-lookup"><span data-stu-id="228ad-116">**Type**</span></span>|<span data-ttu-id="228ad-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="228ad-117">**Required**</span></span>|<span data-ttu-id="228ad-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="228ad-118">**Description**</span></span>|<span data-ttu-id="228ad-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="228ad-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="228ad-120">予定表</span><span class="sxs-lookup"><span data-stu-id="228ad-120">Calendar</span></span>  <br/> |<span data-ttu-id="228ad-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="228ad-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="228ad-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="228ad-122">optional</span></span>  <br/> ||<span data-ttu-id="228ad-123">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="228ad-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="228ad-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="228ad-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="228ad-125">xsd:string</span></span>  <br/> |<span data-ttu-id="228ad-126">必須</span><span class="sxs-lookup"><span data-stu-id="228ad-126">required</span></span>  <br/> ||<span data-ttu-id="228ad-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="228ad-128">通貨型 (Currency)</span><span class="sxs-lookup"><span data-stu-id="228ad-128">Currency</span></span>  <br/> |<span data-ttu-id="228ad-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="228ad-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="228ad-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="228ad-130">optional</span></span>  <br/> ||<span data-ttu-id="228ad-131">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="228ad-132">DataType</span><span class="sxs-lookup"><span data-stu-id="228ad-132">DataType</span></span>  <br/> |<span data-ttu-id="228ad-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="228ad-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="228ad-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="228ad-134">optional</span></span>  <br/> ||<span data-ttu-id="228ad-135">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="228ad-136">Degree</span><span class="sxs-lookup"><span data-stu-id="228ad-136">Degree</span></span>  <br/> |<span data-ttu-id="228ad-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="228ad-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="228ad-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="228ad-138">optional</span></span>  <br/> ||<span data-ttu-id="228ad-139">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="228ad-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="228ad-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="228ad-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="228ad-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="228ad-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="228ad-142">optional</span></span>  <br/> ||<span data-ttu-id="228ad-143">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="228ad-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="228ad-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="228ad-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="228ad-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="228ad-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="228ad-146">optional</span></span>  <br/> ||<span data-ttu-id="228ad-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="228ad-148">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="228ad-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="228ad-149">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="228ad-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="228ad-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="228ad-150">optional</span></span>  <br/> ||<span data-ttu-id="228ad-151">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="228ad-152">ラベル</span><span class="sxs-lookup"><span data-stu-id="228ad-152">Label</span></span>  <br/> |<span data-ttu-id="228ad-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="228ad-153">xsd:string</span></span>  <br/> |<span data-ttu-id="228ad-154">必須</span><span class="sxs-lookup"><span data-stu-id="228ad-154">required</span></span>  <br/> ||<span data-ttu-id="228ad-155">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="228ad-156">LangID</span><span class="sxs-lookup"><span data-stu-id="228ad-156">LangID</span></span>  <br/> |<span data-ttu-id="228ad-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="228ad-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="228ad-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="228ad-158">optional</span></span>  <br/> ||<span data-ttu-id="228ad-159">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="228ad-160">マップ</span><span class="sxs-lookup"><span data-stu-id="228ad-160">Mapped</span></span>  <br/> |<span data-ttu-id="228ad-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="228ad-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="228ad-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="228ad-162">optional</span></span>  <br/> ||<span data-ttu-id="228ad-163">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="228ad-164">名前</span><span class="sxs-lookup"><span data-stu-id="228ad-164">Name</span></span>  <br/> |<span data-ttu-id="228ad-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="228ad-165">xsd:string</span></span>  <br/> |<span data-ttu-id="228ad-166">必須</span><span class="sxs-lookup"><span data-stu-id="228ad-166">required</span></span>  <br/> ||<span data-ttu-id="228ad-167">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="228ad-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="228ad-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="228ad-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="228ad-169">xsd:string</span></span>  <br/> |<span data-ttu-id="228ad-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="228ad-170">optional</span></span>  <br/> ||<span data-ttu-id="228ad-171">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="228ad-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="228ad-172">UnitType</span></span>  <br/> |<span data-ttu-id="228ad-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="228ad-173">xsd:string</span></span>  <br/> |<span data-ttu-id="228ad-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="228ad-174">optional</span></span>  <br/> ||<span data-ttu-id="228ad-175">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="228ad-175">Values of the xsd:string type.</span></span>  <br/> |
   

