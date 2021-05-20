---
title: Solution 要素 (Solutions_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: 図面に格納されているソリューション XML のインスタンスを 1 つ指定します。
ms.openlocfilehash: 028decf0ac9b33ac33dd1e44ed3992ef7eb38aed
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540267"
---
# <a name="solution-element-solutions_type-complextype-visio-xml"></a><span data-ttu-id="a85c1-103">Solution 要素 (Solutions_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a85c1-103">Solution element (Solutions_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="a85c1-104">図面に格納されているソリューション XML のインスタンスを 1 つ指定します。</span><span class="sxs-lookup"><span data-stu-id="a85c1-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a85c1-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="a85c1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a85c1-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a85c1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a85c1-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="a85c1-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a85c1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a85c1-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a85c1-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a85c1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a85c1-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a85c1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a85c1-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="a85c1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a85c1-112">solutions.xml</span><span class="sxs-lookup"><span data-stu-id="a85c1-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a85c1-113">定義</span><span class="sxs-lookup"><span data-stu-id="a85c1-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a85c1-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a85c1-114">Elements and attributes</span></span>

<span data-ttu-id="a85c1-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a85c1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a85c1-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a85c1-116">Parent elements</span></span>

|<span data-ttu-id="a85c1-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a85c1-117">**Element**</span></span>|<span data-ttu-id="a85c1-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a85c1-118">**Type**</span></span>|<span data-ttu-id="a85c1-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a85c1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a85c1-120">ソリューション</span><span class="sxs-lookup"><span data-stu-id="a85c1-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="a85c1-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="a85c1-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a85c1-122">ドキュメントに格納されているソリューションのプロパティを格納します。</span><span class="sxs-lookup"><span data-stu-id="a85c1-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a85c1-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a85c1-123">Child elements</span></span>

|<span data-ttu-id="a85c1-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a85c1-124">**Element**</span></span>|<span data-ttu-id="a85c1-125">**型**</span><span class="sxs-lookup"><span data-stu-id="a85c1-125">**Type**</span></span>|<span data-ttu-id="a85c1-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="a85c1-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a85c1-127">Rel</span><span class="sxs-lookup"><span data-stu-id="a85c1-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a85c1-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="a85c1-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a85c1-129">このソリューションに関連付けられたソリューション XML を持つパーツとの関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="a85c1-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a85c1-130">属性</span><span class="sxs-lookup"><span data-stu-id="a85c1-130">Attributes</span></span>

|<span data-ttu-id="a85c1-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="a85c1-131">**Attribute**</span></span>|<span data-ttu-id="a85c1-132">**型**</span><span class="sxs-lookup"><span data-stu-id="a85c1-132">**Type**</span></span>|<span data-ttu-id="a85c1-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="a85c1-133">**Required**</span></span>|<span data-ttu-id="a85c1-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="a85c1-134">**Description**</span></span>|<span data-ttu-id="a85c1-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="a85c1-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a85c1-136">名前</span><span class="sxs-lookup"><span data-stu-id="a85c1-136">Name</span></span>  <br/> |<span data-ttu-id="a85c1-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a85c1-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a85c1-138">必須</span><span class="sxs-lookup"><span data-stu-id="a85c1-138">required</span></span>  <br/> |<span data-ttu-id="a85c1-139">ソリューションの名前。</span><span class="sxs-lookup"><span data-stu-id="a85c1-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="a85c1-140">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="a85c1-140">Values of the xsd:string type.</span></span>  <br/> |
   

