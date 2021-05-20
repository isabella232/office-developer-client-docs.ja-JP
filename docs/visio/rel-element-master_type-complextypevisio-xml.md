---
title: Rel 要素 (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: 対応するマスター XML を持つパーツとの関係を指定します。
ms.openlocfilehash: 032c1ef4a94bb6acf18587a1257fe82285124e87
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542801"
---
# <a name="rel-element-master_type-complextype-visio-xml"></a><span data-ttu-id="5c1b4-103">Rel 要素 (Master_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5c1b4-103">Rel element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="5c1b4-104">対応するマスター XML を持つパーツとの関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="5c1b4-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c1b4-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="5c1b4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c1b4-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="5c1b4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5c1b4-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="5c1b4-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5c1b4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5c1b4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5c1b4-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5c1b4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5c1b4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5c1b4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5c1b4-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="5c1b4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5c1b4-112">pages.xml、masters.xml、recordsets.xml、page#.xml、master#.xml</span><span class="sxs-lookup"><span data-stu-id="5c1b4-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5c1b4-113">定義</span><span class="sxs-lookup"><span data-stu-id="5c1b4-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5c1b4-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5c1b4-114">Elements and attributes</span></span>

<span data-ttu-id="5c1b4-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c1b4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5c1b4-116">親要素</span><span class="sxs-lookup"><span data-stu-id="5c1b4-116">Parent elements</span></span>

|<span data-ttu-id="5c1b4-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="5c1b4-117">**Element**</span></span>|<span data-ttu-id="5c1b4-118">**型**</span><span class="sxs-lookup"><span data-stu-id="5c1b4-118">**Type**</span></span>|<span data-ttu-id="5c1b4-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="5c1b4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5c1b4-120">Master</span><span class="sxs-lookup"><span data-stu-id="5c1b4-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5c1b4-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="5c1b4-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5c1b4-122">図面に格納されているマスター XML のインスタンスを 1 つ指定します。</span><span class="sxs-lookup"><span data-stu-id="5c1b4-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5c1b4-123">子要素</span><span class="sxs-lookup"><span data-stu-id="5c1b4-123">Child elements</span></span>

<span data-ttu-id="5c1b4-124">なし。</span><span class="sxs-lookup"><span data-stu-id="5c1b4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c1b4-125">属性</span><span class="sxs-lookup"><span data-stu-id="5c1b4-125">Attributes</span></span>

|<span data-ttu-id="5c1b4-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="5c1b4-126">**Attribute**</span></span>|<span data-ttu-id="5c1b4-127">**型**</span><span class="sxs-lookup"><span data-stu-id="5c1b4-127">**Type**</span></span>|<span data-ttu-id="5c1b4-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="5c1b4-128">**Required**</span></span>|<span data-ttu-id="5c1b4-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="5c1b4-129">**Description**</span></span>|<span data-ttu-id="5c1b4-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="5c1b4-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5c1b4-131">r:id</span><span class="sxs-lookup"><span data-stu-id="5c1b4-131">r:id</span></span>  <br/> |<span data-ttu-id="5c1b4-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5c1b4-132">xsd:string</span></span>  <br/> <span data-ttu-id="5c1b4-133">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c1b4-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="5c1b4-134">必須</span><span class="sxs-lookup"><span data-stu-id="5c1b4-134">required</span></span>  <br/> |<span data-ttu-id="5c1b4-135">パーツとの関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="5c1b4-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="5c1b4-136">"rId#"</span><span class="sxs-lookup"><span data-stu-id="5c1b4-136">"rId#"</span></span>  <br/> <span data-ttu-id="5c1b4-137">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c1b4-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c1b4-138">注釈</span><span class="sxs-lookup"><span data-stu-id="5c1b4-138">Remarks</span></span>

<span data-ttu-id="5c1b4-139">**r:id 属性の値** は、次の型 **ST_RelationshipID** があります。</span><span class="sxs-lookup"><span data-stu-id="5c1b4-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="5c1b4-140">この **ST_RelationshipID** は、'rId#' 形式である必要がある文字列で、最後の文字は数値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c1b4-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="5c1b4-141">この数値は **、Rel** 要素のすべての兄弟要素間で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c1b4-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="5c1b4-142">この種類の詳細ST_RelationshipID [ISO/IEC 29500 パート 1 の仕様を参照してください](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)。</span><span class="sxs-lookup"><span data-stu-id="5c1b4-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

