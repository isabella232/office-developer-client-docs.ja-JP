---
title: DataRecordSet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 36d6cf3b34ad0aa81f7b097d6452c46679342a02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360362"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="af7d6-102">DataRecordSet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="af7d6-102">DataRecordSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="af7d6-103">型情報</span><span class="sxs-lookup"><span data-stu-id="af7d6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af7d6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="af7d6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="af7d6-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="af7d6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="af7d6-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="af7d6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="af7d6-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="af7d6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="af7d6-108">なし</span><span class="sxs-lookup"><span data-stu-id="af7d6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="af7d6-109">定義</span><span class="sxs-lookup"><span data-stu-id="af7d6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="af7d6-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="af7d6-110">Elements and attributes</span></span>

<span data-ttu-id="af7d6-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="af7d6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="af7d6-112">子要素</span><span class="sxs-lookup"><span data-stu-id="af7d6-112">Child elements</span></span>

|<span data-ttu-id="af7d6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="af7d6-113">**Element**</span></span>|<span data-ttu-id="af7d6-114">**型**</span><span class="sxs-lookup"><span data-stu-id="af7d6-114">**Type**</span></span>|<span data-ttu-id="af7d6-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="af7d6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="af7d6-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="af7d6-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="af7d6-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="af7d6-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="af7d6-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="af7d6-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="af7d6-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="af7d6-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="af7d6-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="af7d6-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="af7d6-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="af7d6-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="af7d6-122">refreshconflict</span><span class="sxs-lookup"><span data-stu-id="af7d6-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="af7d6-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="af7d6-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="af7d6-124">Rel</span><span class="sxs-lookup"><span data-stu-id="af7d6-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="af7d6-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="af7d6-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="af7d6-126">rowmap</span><span class="sxs-lookup"><span data-stu-id="af7d6-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="af7d6-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="af7d6-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="af7d6-128">属性</span><span class="sxs-lookup"><span data-stu-id="af7d6-128">Attributes</span></span>

|<span data-ttu-id="af7d6-129">**属性**</span><span class="sxs-lookup"><span data-stu-id="af7d6-129">**Attribute**</span></span>|<span data-ttu-id="af7d6-130">**型**</span><span class="sxs-lookup"><span data-stu-id="af7d6-130">**Type**</span></span>|<span data-ttu-id="af7d6-131">**必須**</span><span class="sxs-lookup"><span data-stu-id="af7d6-131">**Required**</span></span>|<span data-ttu-id="af7d6-132">**説明**</span><span class="sxs-lookup"><span data-stu-id="af7d6-132">**Description**</span></span>|<span data-ttu-id="af7d6-133">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="af7d6-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="af7d6-134">チェックサム</span><span class="sxs-lookup"><span data-stu-id="af7d6-134">Checksum</span></span>  <br/> |<span data-ttu-id="af7d6-135">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="af7d6-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="af7d6-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="af7d6-136">optional</span></span>  <br/> ||<span data-ttu-id="af7d6-137">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="af7d6-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="af7d6-138">Command</span><span class="sxs-lookup"><span data-stu-id="af7d6-138">Command</span></span>  <br/> |<span data-ttu-id="af7d6-139">xsd: string</span><span class="sxs-lookup"><span data-stu-id="af7d6-139">xsd:string</span></span>  <br/> |<span data-ttu-id="af7d6-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="af7d6-140">optional</span></span>  <br/> ||<span data-ttu-id="af7d6-141">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="af7d6-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="af7d6-142">ConnectionID</span><span class="sxs-lookup"><span data-stu-id="af7d6-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="af7d6-143">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="af7d6-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="af7d6-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="af7d6-144">optional</span></span>  <br/> ||<span data-ttu-id="af7d6-145">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="af7d6-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="af7d6-146">ID</span><span class="sxs-lookup"><span data-stu-id="af7d6-146">ID</span></span>  <br/> |<span data-ttu-id="af7d6-147">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="af7d6-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="af7d6-148">必須</span><span class="sxs-lookup"><span data-stu-id="af7d6-148">required</span></span>  <br/> ||<span data-ttu-id="af7d6-149">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="af7d6-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="af7d6-150">名前</span><span class="sxs-lookup"><span data-stu-id="af7d6-150">Name</span></span>  <br/> |<span data-ttu-id="af7d6-151">xsd: string</span><span class="sxs-lookup"><span data-stu-id="af7d6-151">xsd:string</span></span>  <br/> |<span data-ttu-id="af7d6-152">省略可能</span><span class="sxs-lookup"><span data-stu-id="af7d6-152">optional</span></span>  <br/> ||<span data-ttu-id="af7d6-153">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="af7d6-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="af7d6-154">nextrowid</span><span class="sxs-lookup"><span data-stu-id="af7d6-154">NextRowID</span></span>  <br/> |<span data-ttu-id="af7d6-155">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="af7d6-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="af7d6-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="af7d6-156">optional</span></span>  <br/> ||<span data-ttu-id="af7d6-157">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="af7d6-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="af7d6-158">Options</span><span class="sxs-lookup"><span data-stu-id="af7d6-158">Options</span></span>  <br/> |<span data-ttu-id="af7d6-159">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="af7d6-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="af7d6-160">省略可能</span><span class="sxs-lookup"><span data-stu-id="af7d6-160">optional</span></span>  <br/> ||<span data-ttu-id="af7d6-161">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="af7d6-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="af7d6-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="af7d6-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="af7d6-163">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="af7d6-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="af7d6-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="af7d6-164">optional</span></span>  <br/> ||<span data-ttu-id="af7d6-165">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="af7d6-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="af7d6-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="af7d6-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="af7d6-167">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="af7d6-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="af7d6-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="af7d6-168">optional</span></span>  <br/> ||<span data-ttu-id="af7d6-169">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="af7d6-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="af7d6-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="af7d6-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="af7d6-171">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="af7d6-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="af7d6-172">省略可能</span><span class="sxs-lookup"><span data-stu-id="af7d6-172">optional</span></span>  <br/> ||<span data-ttu-id="af7d6-173">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="af7d6-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="af7d6-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="af7d6-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="af7d6-175">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="af7d6-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="af7d6-176">省略可能</span><span class="sxs-lookup"><span data-stu-id="af7d6-176">optional</span></span>  <br/> ||<span data-ttu-id="af7d6-177">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="af7d6-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="af7d6-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="af7d6-178">RowOrder</span></span>  <br/> |<span data-ttu-id="af7d6-179">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="af7d6-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="af7d6-180">省略可能</span><span class="sxs-lookup"><span data-stu-id="af7d6-180">optional</span></span>  <br/> ||<span data-ttu-id="af7d6-181">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="af7d6-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="af7d6-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="af7d6-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="af7d6-183">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="af7d6-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="af7d6-184">省略可能</span><span class="sxs-lookup"><span data-stu-id="af7d6-184">optional</span></span>  <br/> ||<span data-ttu-id="af7d6-185">xsd: dateTime 型の値。</span><span class="sxs-lookup"><span data-stu-id="af7d6-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

