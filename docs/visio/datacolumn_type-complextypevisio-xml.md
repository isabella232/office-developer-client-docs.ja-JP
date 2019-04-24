---
title: DataColumn_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344703"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="c2171-102">DataColumn_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c2171-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c2171-103">型情報</span><span class="sxs-lookup"><span data-stu-id="c2171-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2171-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c2171-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c2171-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c2171-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c2171-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="c2171-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c2171-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="c2171-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c2171-108">なし</span><span class="sxs-lookup"><span data-stu-id="c2171-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c2171-109">定義</span><span class="sxs-lookup"><span data-stu-id="c2171-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c2171-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c2171-110">Elements and attributes</span></span>

<span data-ttu-id="c2171-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c2171-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c2171-112">子要素</span><span class="sxs-lookup"><span data-stu-id="c2171-112">Child elements</span></span>

<span data-ttu-id="c2171-113">なし。</span><span class="sxs-lookup"><span data-stu-id="c2171-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2171-114">属性</span><span class="sxs-lookup"><span data-stu-id="c2171-114">Attributes</span></span>

|<span data-ttu-id="c2171-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="c2171-115">**Attribute**</span></span>|<span data-ttu-id="c2171-116">**型**</span><span class="sxs-lookup"><span data-stu-id="c2171-116">**Type**</span></span>|<span data-ttu-id="c2171-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="c2171-117">**Required**</span></span>|<span data-ttu-id="c2171-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="c2171-118">**Description**</span></span>|<span data-ttu-id="c2171-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="c2171-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c2171-120">カレンダー</span><span class="sxs-lookup"><span data-stu-id="c2171-120">Calendar</span></span>  <br/> |<span data-ttu-id="c2171-121">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="c2171-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c2171-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="c2171-122">optional</span></span>  <br/> ||<span data-ttu-id="c2171-123">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c2171-124">columnnameid</span><span class="sxs-lookup"><span data-stu-id="c2171-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="c2171-125">xsd: string</span><span class="sxs-lookup"><span data-stu-id="c2171-125">xsd:string</span></span>  <br/> |<span data-ttu-id="c2171-126">必須</span><span class="sxs-lookup"><span data-stu-id="c2171-126">required</span></span>  <br/> ||<span data-ttu-id="c2171-127">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c2171-128">通貨</span><span class="sxs-lookup"><span data-stu-id="c2171-128">Currency</span></span>  <br/> |<span data-ttu-id="c2171-129">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="c2171-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c2171-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="c2171-130">optional</span></span>  <br/> ||<span data-ttu-id="c2171-131">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c2171-132">DataType</span><span class="sxs-lookup"><span data-stu-id="c2171-132">DataType</span></span>  <br/> |<span data-ttu-id="c2171-133">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="c2171-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c2171-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="c2171-134">optional</span></span>  <br/> ||<span data-ttu-id="c2171-135">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c2171-136">Degree</span><span class="sxs-lookup"><span data-stu-id="c2171-136">Degree</span></span>  <br/> |<span data-ttu-id="c2171-137">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="c2171-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c2171-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="c2171-138">optional</span></span>  <br/> ||<span data-ttu-id="c2171-139">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c2171-140">displayorder</span><span class="sxs-lookup"><span data-stu-id="c2171-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="c2171-141">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="c2171-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c2171-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="c2171-142">optional</span></span>  <br/> ||<span data-ttu-id="c2171-143">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c2171-144">displaywidth</span><span class="sxs-lookup"><span data-stu-id="c2171-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="c2171-145">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="c2171-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c2171-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="c2171-146">optional</span></span>  <br/> ||<span data-ttu-id="c2171-147">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c2171-148">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="c2171-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="c2171-149">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="c2171-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c2171-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="c2171-150">optional</span></span>  <br/> ||<span data-ttu-id="c2171-151">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c2171-152">Label</span><span class="sxs-lookup"><span data-stu-id="c2171-152">Label</span></span>  <br/> |<span data-ttu-id="c2171-153">xsd: string</span><span class="sxs-lookup"><span data-stu-id="c2171-153">xsd:string</span></span>  <br/> |<span data-ttu-id="c2171-154">必須</span><span class="sxs-lookup"><span data-stu-id="c2171-154">required</span></span>  <br/> ||<span data-ttu-id="c2171-155">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c2171-156">LangID</span><span class="sxs-lookup"><span data-stu-id="c2171-156">LangID</span></span>  <br/> |<span data-ttu-id="c2171-157">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="c2171-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c2171-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="c2171-158">optional</span></span>  <br/> ||<span data-ttu-id="c2171-159">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c2171-160">変換</span><span class="sxs-lookup"><span data-stu-id="c2171-160">Mapped</span></span>  <br/> |<span data-ttu-id="c2171-161">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="c2171-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c2171-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="c2171-162">optional</span></span>  <br/> ||<span data-ttu-id="c2171-163">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c2171-164">名前</span><span class="sxs-lookup"><span data-stu-id="c2171-164">Name</span></span>  <br/> |<span data-ttu-id="c2171-165">xsd: string</span><span class="sxs-lookup"><span data-stu-id="c2171-165">xsd:string</span></span>  <br/> |<span data-ttu-id="c2171-166">必須</span><span class="sxs-lookup"><span data-stu-id="c2171-166">required</span></span>  <br/> ||<span data-ttu-id="c2171-167">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c2171-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="c2171-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="c2171-169">xsd: string</span><span class="sxs-lookup"><span data-stu-id="c2171-169">xsd:string</span></span>  <br/> |<span data-ttu-id="c2171-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="c2171-170">optional</span></span>  <br/> ||<span data-ttu-id="c2171-171">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c2171-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="c2171-172">UnitType</span></span>  <br/> |<span data-ttu-id="c2171-173">xsd: string</span><span class="sxs-lookup"><span data-stu-id="c2171-173">xsd:string</span></span>  <br/> |<span data-ttu-id="c2171-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="c2171-174">optional</span></span>  <br/> ||<span data-ttu-id="c2171-175">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c2171-175">Values of the xsd:string type.</span></span>  <br/> |
   

