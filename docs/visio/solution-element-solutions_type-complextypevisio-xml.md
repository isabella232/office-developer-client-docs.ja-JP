---
title: Solution 要素 (Solutions_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: 図面に格納されているソリューション XML の1つのインスタンスを指定します。
ms.openlocfilehash: 028decf0ac9b33ac33dd1e44ed3992ef7eb38aed
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540267"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a><span data-ttu-id="8488f-103">Solution 要素 (Solutions_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8488f-103">Solution element (Solutions_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8488f-104">図面に格納されているソリューション XML の1つのインスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="8488f-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8488f-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="8488f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8488f-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8488f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8488f-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="8488f-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8488f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8488f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8488f-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8488f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8488f-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="8488f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8488f-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="8488f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8488f-112">ソリューション xml</span><span class="sxs-lookup"><span data-stu-id="8488f-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8488f-113">定義</span><span class="sxs-lookup"><span data-stu-id="8488f-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8488f-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8488f-114">Elements and attributes</span></span>

<span data-ttu-id="8488f-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8488f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8488f-116">親要素</span><span class="sxs-lookup"><span data-stu-id="8488f-116">Parent elements</span></span>

|<span data-ttu-id="8488f-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="8488f-117">**Element**</span></span>|<span data-ttu-id="8488f-118">**型**</span><span class="sxs-lookup"><span data-stu-id="8488f-118">**Type**</span></span>|<span data-ttu-id="8488f-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="8488f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8488f-120">ソリューション</span><span class="sxs-lookup"><span data-stu-id="8488f-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="8488f-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="8488f-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8488f-122">ドキュメントに格納されているソリューションのプロパティを格納します。</span><span class="sxs-lookup"><span data-stu-id="8488f-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8488f-123">子要素</span><span class="sxs-lookup"><span data-stu-id="8488f-123">Child elements</span></span>

|<span data-ttu-id="8488f-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="8488f-124">**Element**</span></span>|<span data-ttu-id="8488f-125">**型**</span><span class="sxs-lookup"><span data-stu-id="8488f-125">**Type**</span></span>|<span data-ttu-id="8488f-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="8488f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8488f-127">Rel</span><span class="sxs-lookup"><span data-stu-id="8488f-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8488f-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="8488f-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8488f-129">このソリューションに関連付けられているソリューション XML に対するパーツとの関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="8488f-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8488f-130">属性</span><span class="sxs-lookup"><span data-stu-id="8488f-130">Attributes</span></span>

|<span data-ttu-id="8488f-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="8488f-131">**Attribute**</span></span>|<span data-ttu-id="8488f-132">**型**</span><span class="sxs-lookup"><span data-stu-id="8488f-132">**Type**</span></span>|<span data-ttu-id="8488f-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="8488f-133">**Required**</span></span>|<span data-ttu-id="8488f-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="8488f-134">**Description**</span></span>|<span data-ttu-id="8488f-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="8488f-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8488f-136">名前</span><span class="sxs-lookup"><span data-stu-id="8488f-136">Name</span></span>  <br/> |<span data-ttu-id="8488f-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="8488f-137">xsd:string</span></span>  <br/> |<span data-ttu-id="8488f-138">必須</span><span class="sxs-lookup"><span data-stu-id="8488f-138">required</span></span>  <br/> |<span data-ttu-id="8488f-139">ソリューションの名前。</span><span class="sxs-lookup"><span data-stu-id="8488f-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="8488f-140">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="8488f-140">Values of the xsd:string type.</span></span>  <br/> |
   

