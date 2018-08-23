---
title: Rel の要素 (Solution_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: XML は、このソリューションに関連付けられているソリューションを使用して、パーツへのリレーションシップを指定します。
ms.openlocfilehash: 59d9db3f7e0897abf278a27229c07fd3942cee79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806173"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a><span data-ttu-id="b9b7a-103">Rel の要素 (Solution_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="b9b7a-103">Rel element (Solution_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b9b7a-104">XML は、このソリューションに関連付けられているソリューションを使用して、パーツへのリレーションシップを指定します。</span><span class="sxs-lookup"><span data-stu-id="b9b7a-104">Specifies a relationship to a part with the solution XML associated with this solution.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9b7a-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="b9b7a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9b7a-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="b9b7a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b9b7a-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="b9b7a-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b9b7a-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="b9b7a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b9b7a-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b9b7a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b9b7a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b9b7a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b9b7a-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="b9b7a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b9b7a-112">pages.xml、masters.xml、recordsets.xml、ページ番号の .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="b9b7a-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b9b7a-113">定義</span><span class="sxs-lookup"><span data-stu-id="b9b7a-113">Definition</span></span>

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b9b7a-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b9b7a-114">Elements and attributes</span></span>

<span data-ttu-id="b9b7a-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9b7a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b9b7a-116">親要素</span><span class="sxs-lookup"><span data-stu-id="b9b7a-116">Parent elements</span></span>

|<span data-ttu-id="b9b7a-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="b9b7a-117">**Element**</span></span>|<span data-ttu-id="b9b7a-118">**型**</span><span class="sxs-lookup"><span data-stu-id="b9b7a-118">**Type**</span></span>|<span data-ttu-id="b9b7a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="b9b7a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b9b7a-120">Solution</span><span class="sxs-lookup"><span data-stu-id="b9b7a-120">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b9b7a-121">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="b9b7a-121">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b9b7a-122">XML は、図面に格納されているソリューションの 1 つのインスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="b9b7a-122">Specifies one instance of solution XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b9b7a-123">子要素</span><span class="sxs-lookup"><span data-stu-id="b9b7a-123">Child elements</span></span>

<span data-ttu-id="b9b7a-124">なし。</span><span class="sxs-lookup"><span data-stu-id="b9b7a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9b7a-125">属性</span><span class="sxs-lookup"><span data-stu-id="b9b7a-125">Attributes</span></span>

|<span data-ttu-id="b9b7a-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="b9b7a-126">**Attribute**</span></span>|<span data-ttu-id="b9b7a-127">**型**</span><span class="sxs-lookup"><span data-stu-id="b9b7a-127">**Type**</span></span>|<span data-ttu-id="b9b7a-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="b9b7a-128">**Required**</span></span>|<span data-ttu-id="b9b7a-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="b9b7a-129">**Description**</span></span>|<span data-ttu-id="b9b7a-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="b9b7a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b9b7a-131">r: id</span><span class="sxs-lookup"><span data-stu-id="b9b7a-131">r:id</span></span>  <br/> |<span data-ttu-id="b9b7a-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b9b7a-132">xsd:string</span></span>  <br/> <span data-ttu-id="b9b7a-133">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9b7a-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="b9b7a-134">必須</span><span class="sxs-lookup"><span data-stu-id="b9b7a-134">required</span></span>  <br/> |<span data-ttu-id="b9b7a-135">パーツへのリレーションシップを指定します。</span><span class="sxs-lookup"><span data-stu-id="b9b7a-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="b9b7a-136">「# を削除する」</span><span class="sxs-lookup"><span data-stu-id="b9b7a-136">"rId#"</span></span>  <br/> <span data-ttu-id="b9b7a-137">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9b7a-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9b7a-138">注釈</span><span class="sxs-lookup"><span data-stu-id="b9b7a-138">Remarks</span></span>

<span data-ttu-id="b9b7a-139">**R: id**属性の値は、 **ST_RelationshipID**型である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9b7a-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="b9b7a-140">**ST_RelationshipID**型は、文字列形式にする必要がある 'rId #'、最後の文字がいくつかをする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9b7a-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="b9b7a-141">数は、 **Rel**の要素のすべての兄弟要素間で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9b7a-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="b9b7a-142">ST_RelationshipID 型の詳細については、 [ISO/IEC 29500 の第 1 部の仕様](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9b7a-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

