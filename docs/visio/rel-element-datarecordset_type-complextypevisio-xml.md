---
title: Rel 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: 関連付けられたレコードセットとデータ バインド情報を持つパーツとの関係を指定します。
ms.openlocfilehash: fa93a3cbc32b6929b159b958ef2a96eafacf204f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542864"
---
# <a name="rel-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="74b51-103">Rel 要素 (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="74b51-103">Rel element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="74b51-104">関連付けられたレコードセットとデータ バインド情報を持つパーツとの関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="74b51-104">Specifies a relationship to a part with the associated recordset and data binding information.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="74b51-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="74b51-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="74b51-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="74b51-106">**Element type**</span></span> <br/> |[<span data-ttu-id="74b51-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="74b51-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="74b51-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="74b51-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="74b51-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="74b51-109">**Schema file**</span></span> <br/> |<span data-ttu-id="74b51-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="74b51-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="74b51-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="74b51-111">**Document parts**</span></span> <br/> |<span data-ttu-id="74b51-112">pages.xml、masters.xml、recordsets.xml、page#.xml、master#.xml</span><span class="sxs-lookup"><span data-stu-id="74b51-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="74b51-113">定義</span><span class="sxs-lookup"><span data-stu-id="74b51-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="74b51-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="74b51-114">Elements and attributes</span></span>

<span data-ttu-id="74b51-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="74b51-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="74b51-116">親要素</span><span class="sxs-lookup"><span data-stu-id="74b51-116">Parent elements</span></span>

|<span data-ttu-id="74b51-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="74b51-117">**Element**</span></span>|<span data-ttu-id="74b51-118">**型**</span><span class="sxs-lookup"><span data-stu-id="74b51-118">**Type**</span></span>|<span data-ttu-id="74b51-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="74b51-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="74b51-120">DataRecordset</span><span class="sxs-lookup"><span data-stu-id="74b51-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="74b51-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="74b51-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="74b51-122">図面に格納されているレコードセットとデータ バインド情報の 1 つのインスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="74b51-122">Specifies one instance of a recordset and data binding information stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="74b51-123">子要素</span><span class="sxs-lookup"><span data-stu-id="74b51-123">Child elements</span></span>

<span data-ttu-id="74b51-124">なし。</span><span class="sxs-lookup"><span data-stu-id="74b51-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="74b51-125">属性</span><span class="sxs-lookup"><span data-stu-id="74b51-125">Attributes</span></span>

|<span data-ttu-id="74b51-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="74b51-126">**Attribute**</span></span>|<span data-ttu-id="74b51-127">**型**</span><span class="sxs-lookup"><span data-stu-id="74b51-127">**Type**</span></span>|<span data-ttu-id="74b51-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="74b51-128">**Required**</span></span>|<span data-ttu-id="74b51-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="74b51-129">**Description**</span></span>|<span data-ttu-id="74b51-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="74b51-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="74b51-131">r:id</span><span class="sxs-lookup"><span data-stu-id="74b51-131">r:id</span></span>  <br/> |<span data-ttu-id="74b51-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="74b51-132">xsd:string</span></span>  <br/> <span data-ttu-id="74b51-133">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74b51-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="74b51-134">必須</span><span class="sxs-lookup"><span data-stu-id="74b51-134">required</span></span>  <br/> |<span data-ttu-id="74b51-135">パーツとの関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="74b51-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="74b51-136">"rId#"</span><span class="sxs-lookup"><span data-stu-id="74b51-136">"rId#"</span></span>  <br/> <span data-ttu-id="74b51-137">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74b51-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74b51-138">注釈</span><span class="sxs-lookup"><span data-stu-id="74b51-138">Remarks</span></span>

<span data-ttu-id="74b51-139">**r:id 属性の値** は、次の型 **ST_RelationshipID** があります。</span><span class="sxs-lookup"><span data-stu-id="74b51-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="74b51-140">この **ST_RelationshipID** は、'rId#' 形式である必要がある文字列で、最後の文字は数値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="74b51-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="74b51-141">この数値は **、Rel** 要素のすべての兄弟要素間で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="74b51-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="74b51-142">この種類の詳細ST_RelationshipID [ISO/IEC 29500 パート 1 の仕様を参照してください](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)。</span><span class="sxs-lookup"><span data-stu-id="74b51-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

