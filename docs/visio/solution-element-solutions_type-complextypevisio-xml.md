---
title: ソリューションの要素 (Solutions_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: XML は、図面に格納されているソリューションの 1 つのインスタンスを指定します。
ms.openlocfilehash: 06cefcbf9b0191a9dded5548a457c4a0e50a33ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806540"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a><span data-ttu-id="409a6-103">ソリューションの要素 (Solutions_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="409a6-103">Solution element (Solutions_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="409a6-104">XML は、図面に格納されているソリューションの 1 つのインスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="409a6-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="409a6-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="409a6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="409a6-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="409a6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="409a6-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="409a6-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="409a6-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="409a6-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="409a6-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="409a6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="409a6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="409a6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="409a6-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="409a6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="409a6-112">solutions.xml</span><span class="sxs-lookup"><span data-stu-id="409a6-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="409a6-113">定義</span><span class="sxs-lookup"><span data-stu-id="409a6-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="409a6-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="409a6-114">Elements and attributes</span></span>

<span data-ttu-id="409a6-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="409a6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="409a6-116">親要素</span><span class="sxs-lookup"><span data-stu-id="409a6-116">Parent elements</span></span>

|<span data-ttu-id="409a6-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="409a6-117">**Element**</span></span>|<span data-ttu-id="409a6-118">**型**</span><span class="sxs-lookup"><span data-stu-id="409a6-118">**Type**</span></span>|<span data-ttu-id="409a6-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="409a6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="409a6-120">ソリューション</span><span class="sxs-lookup"><span data-stu-id="409a6-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="409a6-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="409a6-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="409a6-122">ドキュメントに格納されているソリューションのプロパティを格納します。</span><span class="sxs-lookup"><span data-stu-id="409a6-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="409a6-123">子要素</span><span class="sxs-lookup"><span data-stu-id="409a6-123">Child elements</span></span>

|<span data-ttu-id="409a6-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="409a6-124">**Element**</span></span>|<span data-ttu-id="409a6-125">**型**</span><span class="sxs-lookup"><span data-stu-id="409a6-125">**Type**</span></span>|<span data-ttu-id="409a6-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="409a6-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="409a6-127">Rel</span><span class="sxs-lookup"><span data-stu-id="409a6-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="409a6-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="409a6-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="409a6-129">XML は、このソリューションに関連付けられているソリューションを使用して、パーツへのリレーションシップを指定します。</span><span class="sxs-lookup"><span data-stu-id="409a6-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="409a6-130">属性</span><span class="sxs-lookup"><span data-stu-id="409a6-130">Attributes</span></span>

|<span data-ttu-id="409a6-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="409a6-131">**Attribute**</span></span>|<span data-ttu-id="409a6-132">**型**</span><span class="sxs-lookup"><span data-stu-id="409a6-132">**Type**</span></span>|<span data-ttu-id="409a6-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="409a6-133">**Required**</span></span>|<span data-ttu-id="409a6-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="409a6-134">**Description**</span></span>|<span data-ttu-id="409a6-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="409a6-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="409a6-136">名前</span><span class="sxs-lookup"><span data-stu-id="409a6-136">Name</span></span>  <br/> |<span data-ttu-id="409a6-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="409a6-137">xsd:string</span></span>  <br/> |<span data-ttu-id="409a6-138">必須</span><span class="sxs-lookup"><span data-stu-id="409a6-138">required</span></span>  <br/> |<span data-ttu-id="409a6-139">ソリューションの名前です。</span><span class="sxs-lookup"><span data-stu-id="409a6-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="409a6-140">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="409a6-140">Values of the xsd:string type.</span></span>  <br/> |
   

