---
title: DataRecordSet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 132261ae823d1749676b7bdc28cdd1cb94f6ef5b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539145"
---
# <a name="datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="d80d4-102">DataRecordSet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d80d4-102">DataRecordSet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d80d4-103">型情報</span><span class="sxs-lookup"><span data-stu-id="d80d4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d80d4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d80d4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d80d4-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d80d4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d80d4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d80d4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d80d4-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="d80d4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d80d4-108">なし</span><span class="sxs-lookup"><span data-stu-id="d80d4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d80d4-109">定義</span><span class="sxs-lookup"><span data-stu-id="d80d4-109">Definition</span></span>

```XML
          <xs:complexType name="DataRecordSet_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DataColumns"  type="DataColumns_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PrimaryKey"  type="PrimaryKey_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowMap"  type="RowMap_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshConflict"  type="RefreshConflict_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="AutoLinkComparison"  type="AutoLinkComparison_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ConnectionID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="Options"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TimeRefreshed"
  type="xsd:dateTime"
    />
    <xs:attribute name="NextRowID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="RowOrder"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshOverwriteAll"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshNoReconciliationUI"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshInterval"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReplaceLinks"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Checksum"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d80d4-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d80d4-110">Elements and attributes</span></span>

<span data-ttu-id="d80d4-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d80d4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d80d4-112">子要素</span><span class="sxs-lookup"><span data-stu-id="d80d4-112">Child elements</span></span>

|<span data-ttu-id="d80d4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d80d4-113">**Element**</span></span>|<span data-ttu-id="d80d4-114">**型**</span><span class="sxs-lookup"><span data-stu-id="d80d4-114">**Type**</span></span>|<span data-ttu-id="d80d4-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="d80d4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d80d4-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="d80d4-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d80d4-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="d80d4-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d80d4-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="d80d4-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d80d4-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="d80d4-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d80d4-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="d80d4-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d80d4-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="d80d4-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d80d4-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="d80d4-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d80d4-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="d80d4-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d80d4-124">Rel</span><span class="sxs-lookup"><span data-stu-id="d80d4-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d80d4-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="d80d4-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d80d4-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="d80d4-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d80d4-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="d80d4-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d80d4-128">属性</span><span class="sxs-lookup"><span data-stu-id="d80d4-128">Attributes</span></span>

|<span data-ttu-id="d80d4-129">**属性**</span><span class="sxs-lookup"><span data-stu-id="d80d4-129">**Attribute**</span></span>|<span data-ttu-id="d80d4-130">**型**</span><span class="sxs-lookup"><span data-stu-id="d80d4-130">**Type**</span></span>|<span data-ttu-id="d80d4-131">**必須**</span><span class="sxs-lookup"><span data-stu-id="d80d4-131">**Required**</span></span>|<span data-ttu-id="d80d4-132">**説明**</span><span class="sxs-lookup"><span data-stu-id="d80d4-132">**Description**</span></span>|<span data-ttu-id="d80d4-133">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="d80d4-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d80d4-134">Checksum</span><span class="sxs-lookup"><span data-stu-id="d80d4-134">Checksum</span></span>  <br/> |<span data-ttu-id="d80d4-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d80d4-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d80d4-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="d80d4-136">optional</span></span>  <br/> ||<span data-ttu-id="d80d4-137">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="d80d4-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d80d4-138">Command</span><span class="sxs-lookup"><span data-stu-id="d80d4-138">Command</span></span>  <br/> |<span data-ttu-id="d80d4-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d80d4-139">xsd:string</span></span>  <br/> |<span data-ttu-id="d80d4-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="d80d4-140">optional</span></span>  <br/> ||<span data-ttu-id="d80d4-141">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d80d4-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d80d4-142">ConnectionID</span><span class="sxs-lookup"><span data-stu-id="d80d4-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="d80d4-143">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d80d4-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d80d4-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="d80d4-144">optional</span></span>  <br/> ||<span data-ttu-id="d80d4-145">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="d80d4-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d80d4-146">ID</span><span class="sxs-lookup"><span data-stu-id="d80d4-146">ID</span></span>  <br/> |<span data-ttu-id="d80d4-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d80d4-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d80d4-148">必須</span><span class="sxs-lookup"><span data-stu-id="d80d4-148">required</span></span>  <br/> ||<span data-ttu-id="d80d4-149">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="d80d4-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d80d4-150">名前</span><span class="sxs-lookup"><span data-stu-id="d80d4-150">Name</span></span>  <br/> |<span data-ttu-id="d80d4-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d80d4-151">xsd:string</span></span>  <br/> |<span data-ttu-id="d80d4-152">省略可能</span><span class="sxs-lookup"><span data-stu-id="d80d4-152">optional</span></span>  <br/> ||<span data-ttu-id="d80d4-153">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d80d4-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d80d4-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="d80d4-154">NextRowID</span></span>  <br/> |<span data-ttu-id="d80d4-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d80d4-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d80d4-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="d80d4-156">optional</span></span>  <br/> ||<span data-ttu-id="d80d4-157">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="d80d4-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d80d4-158">Options</span><span class="sxs-lookup"><span data-stu-id="d80d4-158">Options</span></span>  <br/> |<span data-ttu-id="d80d4-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d80d4-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d80d4-160">省略可能</span><span class="sxs-lookup"><span data-stu-id="d80d4-160">optional</span></span>  <br/> ||<span data-ttu-id="d80d4-161">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="d80d4-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d80d4-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="d80d4-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="d80d4-163">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d80d4-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d80d4-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="d80d4-164">optional</span></span>  <br/> ||<span data-ttu-id="d80d4-165">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="d80d4-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d80d4-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="d80d4-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="d80d4-167">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="d80d4-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d80d4-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="d80d4-168">optional</span></span>  <br/> ||<span data-ttu-id="d80d4-169">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="d80d4-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d80d4-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="d80d4-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="d80d4-171">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="d80d4-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d80d4-172">省略可能</span><span class="sxs-lookup"><span data-stu-id="d80d4-172">optional</span></span>  <br/> ||<span data-ttu-id="d80d4-173">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="d80d4-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d80d4-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="d80d4-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="d80d4-175">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d80d4-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d80d4-176">省略可能</span><span class="sxs-lookup"><span data-stu-id="d80d4-176">optional</span></span>  <br/> ||<span data-ttu-id="d80d4-177">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="d80d4-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d80d4-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="d80d4-178">RowOrder</span></span>  <br/> |<span data-ttu-id="d80d4-179">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="d80d4-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d80d4-180">省略可能</span><span class="sxs-lookup"><span data-stu-id="d80d4-180">optional</span></span>  <br/> ||<span data-ttu-id="d80d4-181">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="d80d4-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d80d4-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="d80d4-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="d80d4-183">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="d80d4-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="d80d4-184">省略可能</span><span class="sxs-lookup"><span data-stu-id="d80d4-184">optional</span></span>  <br/> ||<span data-ttu-id="d80d4-185">xsd:dateTime type 型の値。</span><span class="sxs-lookup"><span data-stu-id="d80d4-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

