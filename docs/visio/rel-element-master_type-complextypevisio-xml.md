---
title: Rel の要素 (Master_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: 対応するマスター XML パーツへのリレーションシップを指定します。
ms.openlocfilehash: 82552eeab746d9675f6175b62c34cef4a9c3c418
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393048"
---
# <a name="rel-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="1e1a0-103">Rel の要素 (Master_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="1e1a0-103">Rel element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1e1a0-104">対応するマスター XML パーツへのリレーションシップを指定します。</span><span class="sxs-lookup"><span data-stu-id="1e1a0-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e1a0-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="1e1a0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e1a0-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="1e1a0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1e1a0-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="1e1a0-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1e1a0-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="1e1a0-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1e1a0-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1e1a0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1e1a0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1e1a0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1e1a0-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="1e1a0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1e1a0-112">pages.xml、masters.xml、recordsets.xml、ページ番号の .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="1e1a0-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1e1a0-113">定義</span><span class="sxs-lookup"><span data-stu-id="1e1a0-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1e1a0-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1e1a0-114">Elements and attributes</span></span>

<span data-ttu-id="1e1a0-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e1a0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1e1a0-116">親要素</span><span class="sxs-lookup"><span data-stu-id="1e1a0-116">Parent elements</span></span>

|<span data-ttu-id="1e1a0-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="1e1a0-117">**Element**</span></span>|<span data-ttu-id="1e1a0-118">**型**</span><span class="sxs-lookup"><span data-stu-id="1e1a0-118">**Type**</span></span>|<span data-ttu-id="1e1a0-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="1e1a0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1e1a0-120">Master</span><span class="sxs-lookup"><span data-stu-id="1e1a0-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1e1a0-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="1e1a0-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1e1a0-122">図面に格納されている XML をマスターの 1 つのインスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="1e1a0-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1e1a0-123">子要素</span><span class="sxs-lookup"><span data-stu-id="1e1a0-123">Child elements</span></span>

<span data-ttu-id="1e1a0-124">なし。</span><span class="sxs-lookup"><span data-stu-id="1e1a0-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e1a0-125">属性</span><span class="sxs-lookup"><span data-stu-id="1e1a0-125">Attributes</span></span>

|<span data-ttu-id="1e1a0-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="1e1a0-126">**Attribute**</span></span>|<span data-ttu-id="1e1a0-127">**型**</span><span class="sxs-lookup"><span data-stu-id="1e1a0-127">**Type**</span></span>|<span data-ttu-id="1e1a0-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="1e1a0-128">**Required**</span></span>|<span data-ttu-id="1e1a0-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="1e1a0-129">**Description**</span></span>|<span data-ttu-id="1e1a0-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="1e1a0-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1e1a0-131">r: id</span><span class="sxs-lookup"><span data-stu-id="1e1a0-131">r:id</span></span>  <br/> |<span data-ttu-id="1e1a0-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1e1a0-132">xsd:string</span></span>  <br/> <span data-ttu-id="1e1a0-133">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e1a0-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="1e1a0-134">必須</span><span class="sxs-lookup"><span data-stu-id="1e1a0-134">required</span></span>  <br/> |<span data-ttu-id="1e1a0-135">パーツへのリレーションシップを指定します。</span><span class="sxs-lookup"><span data-stu-id="1e1a0-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="1e1a0-136">「# を削除する」</span><span class="sxs-lookup"><span data-stu-id="1e1a0-136">"rId#"</span></span>  <br/> <span data-ttu-id="1e1a0-137">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e1a0-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e1a0-138">備考</span><span class="sxs-lookup"><span data-stu-id="1e1a0-138">Remarks</span></span>

<span data-ttu-id="1e1a0-139">**R: id**属性の値は、 **ST_RelationshipID**型である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e1a0-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="1e1a0-140">**ST_RelationshipID**型は、文字列形式にする必要がある 'rId #'、最後の文字がいくつかをする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e1a0-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="1e1a0-141">数は、 **Rel**の要素のすべての兄弟要素間で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e1a0-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="1e1a0-142">ST_RelationshipID 型の詳細については、 [ISO/IEC 29500 の第 1 部の仕様](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e1a0-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

