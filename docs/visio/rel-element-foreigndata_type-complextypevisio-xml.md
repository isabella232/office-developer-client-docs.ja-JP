---
title: Rel 要素 (ForeignData_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: 図形と、図形に関連付けられた画像データを含むドキュメント パーツとの関係を指定します。
ms.openlocfilehash: 5836fd306670600f65eda1f3a998ef4c5479114b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542808"
---
# <a name="rel-element-foreigndata_type-complextype-visio-xml"></a><span data-ttu-id="70ef8-103">Rel 要素 (ForeignData_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="70ef8-103">Rel element (ForeignData_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="70ef8-104">図形と、図形に関連付けられた画像データを含むドキュメント パーツとの関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="70ef8-104">Specifies a relationship between a shape and a document part that contains the image data associated with the shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70ef8-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="70ef8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70ef8-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="70ef8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="70ef8-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="70ef8-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="70ef8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="70ef8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="70ef8-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="70ef8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="70ef8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="70ef8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="70ef8-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="70ef8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="70ef8-112">pages.xml、masters.xml、recordsets.xml、page#.xml、master#.xml</span><span class="sxs-lookup"><span data-stu-id="70ef8-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="70ef8-113">定義</span><span class="sxs-lookup"><span data-stu-id="70ef8-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="70ef8-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="70ef8-114">Elements and attributes</span></span>

<span data-ttu-id="70ef8-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="70ef8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="70ef8-116">親要素</span><span class="sxs-lookup"><span data-stu-id="70ef8-116">Parent elements</span></span>

|<span data-ttu-id="70ef8-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="70ef8-117">**Element**</span></span>|<span data-ttu-id="70ef8-118">**型**</span><span class="sxs-lookup"><span data-stu-id="70ef8-118">**Type**</span></span>|<span data-ttu-id="70ef8-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="70ef8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="70ef8-120">ForeignData</span><span class="sxs-lookup"><span data-stu-id="70ef8-120">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70ef8-121">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="70ef8-121">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="70ef8-122">図面に格納されているイメージ データのインスタンスを 1 つ指定します。</span><span class="sxs-lookup"><span data-stu-id="70ef8-122">Specifies one instance of image data stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="70ef8-123">子要素</span><span class="sxs-lookup"><span data-stu-id="70ef8-123">Child elements</span></span>

<span data-ttu-id="70ef8-124">なし。</span><span class="sxs-lookup"><span data-stu-id="70ef8-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70ef8-125">属性</span><span class="sxs-lookup"><span data-stu-id="70ef8-125">Attributes</span></span>

|<span data-ttu-id="70ef8-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="70ef8-126">**Attribute**</span></span>|<span data-ttu-id="70ef8-127">**型**</span><span class="sxs-lookup"><span data-stu-id="70ef8-127">**Type**</span></span>|<span data-ttu-id="70ef8-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="70ef8-128">**Required**</span></span>|<span data-ttu-id="70ef8-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="70ef8-129">**Description**</span></span>|<span data-ttu-id="70ef8-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="70ef8-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="70ef8-131">r:id</span><span class="sxs-lookup"><span data-stu-id="70ef8-131">r:id</span></span>  <br/> |<span data-ttu-id="70ef8-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="70ef8-132">xsd:string</span></span>  <br/> <span data-ttu-id="70ef8-133">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70ef8-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="70ef8-134">必須</span><span class="sxs-lookup"><span data-stu-id="70ef8-134">required</span></span>  <br/> |<span data-ttu-id="70ef8-135">パーツとの関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="70ef8-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="70ef8-136">"rId#"</span><span class="sxs-lookup"><span data-stu-id="70ef8-136">"rId#"</span></span>  <br/> <span data-ttu-id="70ef8-137">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70ef8-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70ef8-138">注釈</span><span class="sxs-lookup"><span data-stu-id="70ef8-138">Remarks</span></span>

<span data-ttu-id="70ef8-139">**r:id 属性の値** は、次の型 **ST_RelationshipID** があります。</span><span class="sxs-lookup"><span data-stu-id="70ef8-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="70ef8-140">この **ST_RelationshipID** は、'rId#' 形式である必要がある文字列で、最後の文字は数値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="70ef8-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="70ef8-141">この数値は **、Rel** 要素のすべての兄弟要素間で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="70ef8-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="70ef8-142">この種類の詳細ST_RelationshipID [ISO/IEC 29500 パート 1 の仕様を参照してください](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)。</span><span class="sxs-lookup"><span data-stu-id="70ef8-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

