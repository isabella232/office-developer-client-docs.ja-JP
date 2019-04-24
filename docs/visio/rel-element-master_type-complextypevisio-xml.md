---
title: Rel 要素 (Master_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: 対応するマスター XML を持つパーツへのリレーションシップを指定します。
ms.openlocfilehash: 82552eeab746d9675f6175b62c34cef4a9c3c418
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320007"
---
# <a name="rel-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="73b0c-103">Rel 要素 (Master_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="73b0c-103">Rel element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="73b0c-104">対応するマスター XML を持つパーツへのリレーションシップを指定します。</span><span class="sxs-lookup"><span data-stu-id="73b0c-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73b0c-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="73b0c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73b0c-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="73b0c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="73b0c-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="73b0c-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="73b0c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="73b0c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="73b0c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="73b0c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="73b0c-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="73b0c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="73b0c-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="73b0c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="73b0c-112">system.xml、masters、config.xml、pages、page # .xml、.master (.xml)</span><span class="sxs-lookup"><span data-stu-id="73b0c-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="73b0c-113">定義</span><span class="sxs-lookup"><span data-stu-id="73b0c-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="73b0c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="73b0c-114">Elements and attributes</span></span>

<span data-ttu-id="73b0c-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="73b0c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="73b0c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="73b0c-116">Parent elements</span></span>

|<span data-ttu-id="73b0c-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="73b0c-117">**Element**</span></span>|<span data-ttu-id="73b0c-118">**型**</span><span class="sxs-lookup"><span data-stu-id="73b0c-118">**Type**</span></span>|<span data-ttu-id="73b0c-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="73b0c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="73b0c-120">Master</span><span class="sxs-lookup"><span data-stu-id="73b0c-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="73b0c-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="73b0c-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="73b0c-122">図面に格納されているマスタ XML の1つのインスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="73b0c-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="73b0c-123">子要素</span><span class="sxs-lookup"><span data-stu-id="73b0c-123">Child elements</span></span>

<span data-ttu-id="73b0c-124">なし。</span><span class="sxs-lookup"><span data-stu-id="73b0c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73b0c-125">属性</span><span class="sxs-lookup"><span data-stu-id="73b0c-125">Attributes</span></span>

|<span data-ttu-id="73b0c-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="73b0c-126">**Attribute**</span></span>|<span data-ttu-id="73b0c-127">**型**</span><span class="sxs-lookup"><span data-stu-id="73b0c-127">**Type**</span></span>|<span data-ttu-id="73b0c-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="73b0c-128">**Required**</span></span>|<span data-ttu-id="73b0c-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="73b0c-129">**Description**</span></span>|<span data-ttu-id="73b0c-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="73b0c-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="73b0c-131">r: id</span><span class="sxs-lookup"><span data-stu-id="73b0c-131">r:id</span></span>  <br/> |<span data-ttu-id="73b0c-132">xsd: string</span><span class="sxs-lookup"><span data-stu-id="73b0c-132">xsd:string</span></span>  <br/> <span data-ttu-id="73b0c-133">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73b0c-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="73b0c-134">必須</span><span class="sxs-lookup"><span data-stu-id="73b0c-134">required</span></span>  <br/> |<span data-ttu-id="73b0c-135">パーツへのリレーションシップを指定します。</span><span class="sxs-lookup"><span data-stu-id="73b0c-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="73b0c-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="73b0c-136">"rId#"</span></span>  <br/> <span data-ttu-id="73b0c-137">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73b0c-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73b0c-138">解説</span><span class="sxs-lookup"><span data-stu-id="73b0c-138">Remarks</span></span>

<span data-ttu-id="73b0c-139">**r: id**属性の値は、 **ST_RelationshipID**型でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="73b0c-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="73b0c-140">**ST_RelationshipID** type は、' rId # ' という形式で指定する必要があります。最後の文字は数字である必要があります。</span><span class="sxs-lookup"><span data-stu-id="73b0c-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="73b0c-141">この数値は、 **Rel**要素のすべての兄弟要素の間で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="73b0c-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="73b0c-142">ST_RelationshipID 型の詳細については、 [ISO/IEC 29500 Part 1 の仕様](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73b0c-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

