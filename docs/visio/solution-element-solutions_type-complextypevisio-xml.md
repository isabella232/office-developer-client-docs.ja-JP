---
title: Solution 要素 (Solutions_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: 図面に格納されているソリューション XML の1つのインスタンスを指定します。
ms.openlocfilehash: bb3cd512ff6109467c9d6465ba72c764d83abf96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335267"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a><span data-ttu-id="a00d1-103">Solution 要素 (Solutions_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a00d1-103">Solution element (Solutions_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a00d1-104">図面に格納されているソリューション XML の1つのインスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="a00d1-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a00d1-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="a00d1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a00d1-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a00d1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a00d1-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="a00d1-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a00d1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a00d1-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a00d1-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a00d1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a00d1-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="a00d1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a00d1-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="a00d1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a00d1-112">ソリューション xml</span><span class="sxs-lookup"><span data-stu-id="a00d1-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a00d1-113">定義</span><span class="sxs-lookup"><span data-stu-id="a00d1-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a00d1-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a00d1-114">Elements and attributes</span></span>

<span data-ttu-id="a00d1-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a00d1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a00d1-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a00d1-116">Parent elements</span></span>

|<span data-ttu-id="a00d1-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a00d1-117">**Element**</span></span>|<span data-ttu-id="a00d1-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a00d1-118">**Type**</span></span>|<span data-ttu-id="a00d1-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a00d1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a00d1-120">ソリューション</span><span class="sxs-lookup"><span data-stu-id="a00d1-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="a00d1-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="a00d1-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a00d1-122">ドキュメントに格納されているソリューションのプロパティを格納します。</span><span class="sxs-lookup"><span data-stu-id="a00d1-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a00d1-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a00d1-123">Child elements</span></span>

|<span data-ttu-id="a00d1-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a00d1-124">**Element**</span></span>|<span data-ttu-id="a00d1-125">**型**</span><span class="sxs-lookup"><span data-stu-id="a00d1-125">**Type**</span></span>|<span data-ttu-id="a00d1-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="a00d1-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a00d1-127">Rel</span><span class="sxs-lookup"><span data-stu-id="a00d1-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a00d1-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="a00d1-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a00d1-129">このソリューションに関連付けられているソリューション XML に対するパーツとの関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="a00d1-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a00d1-130">属性</span><span class="sxs-lookup"><span data-stu-id="a00d1-130">Attributes</span></span>

|<span data-ttu-id="a00d1-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="a00d1-131">**Attribute**</span></span>|<span data-ttu-id="a00d1-132">**型**</span><span class="sxs-lookup"><span data-stu-id="a00d1-132">**Type**</span></span>|<span data-ttu-id="a00d1-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="a00d1-133">**Required**</span></span>|<span data-ttu-id="a00d1-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="a00d1-134">**Description**</span></span>|<span data-ttu-id="a00d1-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="a00d1-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a00d1-136">名前</span><span class="sxs-lookup"><span data-stu-id="a00d1-136">Name</span></span>  <br/> |<span data-ttu-id="a00d1-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="a00d1-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a00d1-138">必須</span><span class="sxs-lookup"><span data-stu-id="a00d1-138">required</span></span>  <br/> |<span data-ttu-id="a00d1-139">ソリューションの名前。</span><span class="sxs-lookup"><span data-stu-id="a00d1-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="a00d1-140">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="a00d1-140">Values of the xsd:string type.</span></span>  <br/> |
   

