---
title: Rel 要素 (Page_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: 対応するページ XML を持つパーツとの関係を指定します。
ms.openlocfilehash: 19224a7057786677cdb371df887e69e8457649c6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542780"
---
# <a name="rel-element-page_type-complextype-visio-xml"></a><span data-ttu-id="ba010-103">Rel 要素 (Page_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ba010-103">Rel element (Page_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ba010-104">対応するページ XML を持つパーツとの関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="ba010-104">Specifies a relationship to a part with the corresponding page XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba010-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="ba010-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba010-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="ba010-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ba010-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="ba010-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ba010-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ba010-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ba010-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ba010-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ba010-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ba010-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ba010-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="ba010-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ba010-112">pages.xml、masters.xml、recordsets.xml、page#.xml、master#.xml</span><span class="sxs-lookup"><span data-stu-id="ba010-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ba010-113">定義</span><span class="sxs-lookup"><span data-stu-id="ba010-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ba010-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ba010-114">Elements and attributes</span></span>

<span data-ttu-id="ba010-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba010-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ba010-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ba010-116">Parent elements</span></span>

|<span data-ttu-id="ba010-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="ba010-117">**Element**</span></span>|<span data-ttu-id="ba010-118">**型**</span><span class="sxs-lookup"><span data-stu-id="ba010-118">**Type**</span></span>|<span data-ttu-id="ba010-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="ba010-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ba010-120">Page</span><span class="sxs-lookup"><span data-stu-id="ba010-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ba010-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="ba010-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ba010-122">図面に格納されているページ XML のインスタンスを 1 つ指定します。</span><span class="sxs-lookup"><span data-stu-id="ba010-122">Specifies one instance of page XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ba010-123">子要素</span><span class="sxs-lookup"><span data-stu-id="ba010-123">Child elements</span></span>

<span data-ttu-id="ba010-124">なし。</span><span class="sxs-lookup"><span data-stu-id="ba010-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba010-125">属性</span><span class="sxs-lookup"><span data-stu-id="ba010-125">Attributes</span></span>

|<span data-ttu-id="ba010-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="ba010-126">**Attribute**</span></span>|<span data-ttu-id="ba010-127">**型**</span><span class="sxs-lookup"><span data-stu-id="ba010-127">**Type**</span></span>|<span data-ttu-id="ba010-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="ba010-128">**Required**</span></span>|<span data-ttu-id="ba010-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="ba010-129">**Description**</span></span>|<span data-ttu-id="ba010-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="ba010-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ba010-131">r:id</span><span class="sxs-lookup"><span data-stu-id="ba010-131">r:id</span></span>  <br/> |<span data-ttu-id="ba010-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ba010-132">xsd:string</span></span>  <br/> <span data-ttu-id="ba010-133">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba010-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="ba010-134">必須</span><span class="sxs-lookup"><span data-stu-id="ba010-134">required</span></span>  <br/> |<span data-ttu-id="ba010-135">パーツとの関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="ba010-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="ba010-136">"rId#"</span><span class="sxs-lookup"><span data-stu-id="ba010-136">"rId#"</span></span>  <br/> <span data-ttu-id="ba010-137">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba010-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba010-138">注釈</span><span class="sxs-lookup"><span data-stu-id="ba010-138">Remarks</span></span>

<span data-ttu-id="ba010-139">**r:id 属性の値** は、次の型 **ST_RelationshipID** があります。</span><span class="sxs-lookup"><span data-stu-id="ba010-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="ba010-140">この **ST_RelationshipID** は、'rId#' 形式である必要がある文字列で、最後の文字は数値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba010-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="ba010-141">この数値は **、Rel** 要素のすべての兄弟要素間で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba010-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="ba010-142">この種類の詳細ST_RelationshipID [ISO/IEC 29500 パート 1 の仕様を参照してください](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)。</span><span class="sxs-lookup"><span data-stu-id="ba010-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

