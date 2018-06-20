---
title: DataRecordSet_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 79fe048c578e8b9d8095d3fe7cd456af8ce08549
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805173"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="64cae-102">DataRecordSet_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="64cae-102">DataRecordSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="64cae-103">型情報</span><span class="sxs-lookup"><span data-stu-id="64cae-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64cae-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="64cae-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="64cae-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="64cae-105">**Schema file**</span></span> <br/> |<span data-ttu-id="64cae-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="64cae-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="64cae-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="64cae-107">**Extension base**</span></span> <br/> |<span data-ttu-id="64cae-108">なし</span><span class="sxs-lookup"><span data-stu-id="64cae-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="64cae-109">定義</span><span class="sxs-lookup"><span data-stu-id="64cae-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="64cae-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="64cae-110">Elements and attributes</span></span>

<span data-ttu-id="64cae-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="64cae-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="64cae-112">子要素</span><span class="sxs-lookup"><span data-stu-id="64cae-112">Child elements</span></span>

|<span data-ttu-id="64cae-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="64cae-113">**Element**</span></span>|<span data-ttu-id="64cae-114">**型**</span><span class="sxs-lookup"><span data-stu-id="64cae-114">**Type**</span></span>|<span data-ttu-id="64cae-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="64cae-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="64cae-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="64cae-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64cae-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="64cae-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="64cae-118">Datacolumn</span><span class="sxs-lookup"><span data-stu-id="64cae-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64cae-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="64cae-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="64cae-120">主キー</span><span class="sxs-lookup"><span data-stu-id="64cae-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64cae-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="64cae-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="64cae-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="64cae-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64cae-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="64cae-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="64cae-124">Rel</span><span class="sxs-lookup"><span data-stu-id="64cae-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64cae-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="64cae-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="64cae-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="64cae-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64cae-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="64cae-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="64cae-128">属性</span><span class="sxs-lookup"><span data-stu-id="64cae-128">Attributes</span></span>

|<span data-ttu-id="64cae-129">**属性**</span><span class="sxs-lookup"><span data-stu-id="64cae-129">**Attribute**</span></span>|<span data-ttu-id="64cae-130">**型**</span><span class="sxs-lookup"><span data-stu-id="64cae-130">**Type**</span></span>|<span data-ttu-id="64cae-131">**必須**</span><span class="sxs-lookup"><span data-stu-id="64cae-131">**Required**</span></span>|<span data-ttu-id="64cae-132">**説明**</span><span class="sxs-lookup"><span data-stu-id="64cae-132">**Description**</span></span>|<span data-ttu-id="64cae-133">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="64cae-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="64cae-134">チェックサム</span><span class="sxs-lookup"><span data-stu-id="64cae-134">Checksum</span></span>  <br/> |<span data-ttu-id="64cae-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64cae-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64cae-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="64cae-136">optional</span></span>  <br/> ||<span data-ttu-id="64cae-137">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64cae-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="64cae-138">コマンド</span><span class="sxs-lookup"><span data-stu-id="64cae-138">Command</span></span>  <br/> |<span data-ttu-id="64cae-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="64cae-139">xsd:string</span></span>  <br/> |<span data-ttu-id="64cae-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="64cae-140">optional</span></span>  <br/> ||<span data-ttu-id="64cae-141">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64cae-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="64cae-142">接続 Id</span><span class="sxs-lookup"><span data-stu-id="64cae-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="64cae-143">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64cae-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64cae-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="64cae-144">optional</span></span>  <br/> ||<span data-ttu-id="64cae-145">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64cae-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="64cae-146">ID</span><span class="sxs-lookup"><span data-stu-id="64cae-146">ID</span></span>  <br/> |<span data-ttu-id="64cae-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64cae-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64cae-148">必須</span><span class="sxs-lookup"><span data-stu-id="64cae-148">required</span></span>  <br/> ||<span data-ttu-id="64cae-149">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64cae-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="64cae-150">名前</span><span class="sxs-lookup"><span data-stu-id="64cae-150">Name</span></span>  <br/> |<span data-ttu-id="64cae-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="64cae-151">xsd:string</span></span>  <br/> |<span data-ttu-id="64cae-152">省略可能</span><span class="sxs-lookup"><span data-stu-id="64cae-152">optional</span></span>  <br/> ||<span data-ttu-id="64cae-153">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64cae-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="64cae-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="64cae-154">NextRowID</span></span>  <br/> |<span data-ttu-id="64cae-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64cae-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64cae-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="64cae-156">optional</span></span>  <br/> ||<span data-ttu-id="64cae-157">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64cae-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="64cae-158">選択肢</span><span class="sxs-lookup"><span data-stu-id="64cae-158">Options</span></span>  <br/> |<span data-ttu-id="64cae-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64cae-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64cae-160">省略可能</span><span class="sxs-lookup"><span data-stu-id="64cae-160">optional</span></span>  <br/> ||<span data-ttu-id="64cae-161">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64cae-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="64cae-162">間隔</span><span class="sxs-lookup"><span data-stu-id="64cae-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="64cae-163">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64cae-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64cae-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="64cae-164">optional</span></span>  <br/> ||<span data-ttu-id="64cae-165">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64cae-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="64cae-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="64cae-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="64cae-167">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="64cae-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="64cae-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="64cae-168">optional</span></span>  <br/> ||<span data-ttu-id="64cae-169">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64cae-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="64cae-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="64cae-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="64cae-171">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="64cae-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="64cae-172">省略可能</span><span class="sxs-lookup"><span data-stu-id="64cae-172">optional</span></span>  <br/> ||<span data-ttu-id="64cae-173">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64cae-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="64cae-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="64cae-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="64cae-175">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64cae-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64cae-176">省略可能</span><span class="sxs-lookup"><span data-stu-id="64cae-176">optional</span></span>  <br/> ||<span data-ttu-id="64cae-177">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64cae-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="64cae-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="64cae-178">RowOrder</span></span>  <br/> |<span data-ttu-id="64cae-179">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="64cae-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="64cae-180">省略可能</span><span class="sxs-lookup"><span data-stu-id="64cae-180">optional</span></span>  <br/> ||<span data-ttu-id="64cae-181">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64cae-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="64cae-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="64cae-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="64cae-183">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="64cae-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="64cae-184">省略可能</span><span class="sxs-lookup"><span data-stu-id="64cae-184">optional</span></span>  <br/> ||<span data-ttu-id="64cae-185">Xsd:dateTime の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64cae-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

