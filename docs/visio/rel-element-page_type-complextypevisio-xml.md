---
title: Rel 要素 (Page_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: 対応するページ XML を持つパーツへのリレーションシップを指定します。
ms.openlocfilehash: 19224a7057786677cdb371df887e69e8457649c6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542780"
---
# <a name="rel-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="5c304-103">Rel 要素 (Page_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5c304-103">Rel element (Page_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="5c304-104">対応するページ XML を持つパーツへのリレーションシップを指定します。</span><span class="sxs-lookup"><span data-stu-id="5c304-104">Specifies a relationship to a part with the corresponding page XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c304-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="5c304-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c304-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="5c304-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5c304-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="5c304-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5c304-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5c304-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5c304-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5c304-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5c304-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="5c304-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5c304-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="5c304-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5c304-112">system.xml、masters、config.xml、pages、page # .xml、.master (.xml)</span><span class="sxs-lookup"><span data-stu-id="5c304-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5c304-113">定義</span><span class="sxs-lookup"><span data-stu-id="5c304-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5c304-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5c304-114">Elements and attributes</span></span>

<span data-ttu-id="5c304-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c304-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5c304-116">親要素</span><span class="sxs-lookup"><span data-stu-id="5c304-116">Parent elements</span></span>

|<span data-ttu-id="5c304-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="5c304-117">**Element**</span></span>|<span data-ttu-id="5c304-118">**型**</span><span class="sxs-lookup"><span data-stu-id="5c304-118">**Type**</span></span>|<span data-ttu-id="5c304-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="5c304-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5c304-120">Page</span><span class="sxs-lookup"><span data-stu-id="5c304-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5c304-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="5c304-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5c304-122">図面に格納されているページ XML の1つのインスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="5c304-122">Specifies one instance of page XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5c304-123">子要素</span><span class="sxs-lookup"><span data-stu-id="5c304-123">Child elements</span></span>

<span data-ttu-id="5c304-124">なし。</span><span class="sxs-lookup"><span data-stu-id="5c304-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c304-125">属性</span><span class="sxs-lookup"><span data-stu-id="5c304-125">Attributes</span></span>

|<span data-ttu-id="5c304-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="5c304-126">**Attribute**</span></span>|<span data-ttu-id="5c304-127">**型**</span><span class="sxs-lookup"><span data-stu-id="5c304-127">**Type**</span></span>|<span data-ttu-id="5c304-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="5c304-128">**Required**</span></span>|<span data-ttu-id="5c304-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="5c304-129">**Description**</span></span>|<span data-ttu-id="5c304-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="5c304-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5c304-131">r: id</span><span class="sxs-lookup"><span data-stu-id="5c304-131">r:id</span></span>  <br/> |<span data-ttu-id="5c304-132">xsd: string</span><span class="sxs-lookup"><span data-stu-id="5c304-132">xsd:string</span></span>  <br/> <span data-ttu-id="5c304-133">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c304-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="5c304-134">必須</span><span class="sxs-lookup"><span data-stu-id="5c304-134">required</span></span>  <br/> |<span data-ttu-id="5c304-135">パーツへのリレーションシップを指定します。</span><span class="sxs-lookup"><span data-stu-id="5c304-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="5c304-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="5c304-136">"rId#"</span></span>  <br/> <span data-ttu-id="5c304-137">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c304-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c304-138">注釈</span><span class="sxs-lookup"><span data-stu-id="5c304-138">Remarks</span></span>

<span data-ttu-id="5c304-139">**R: id**属性の値は、 **ST_RelationshipID**型でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="5c304-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="5c304-140">**ST_RelationshipID** type は、' rId # ' という形式で指定する必要があります。最後の文字は数字である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c304-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="5c304-141">この数値は、 **Rel**要素のすべての兄弟要素の間で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c304-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="5c304-142">ST_RelationshipID 型の詳細については、 [ISO/IEC 29500 Part 1 の仕様](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c304-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

