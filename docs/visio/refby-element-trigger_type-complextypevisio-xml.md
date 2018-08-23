---
title: RefBy 要素 (Trigger_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: 図面のページへの参照を指定します。
ms.openlocfilehash: e4726a8fe49a7492cd2f7833bbcf5e6810bae18d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572432"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="4f40e-103">RefBy 要素 (Trigger_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="4f40e-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4f40e-104">図面のページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="4f40e-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f40e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="4f40e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f40e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4f40e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4f40e-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="4f40e-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4f40e-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="4f40e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4f40e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4f40e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4f40e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4f40e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4f40e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="4f40e-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="4f40e-112">定義</span><span class="sxs-lookup"><span data-stu-id="4f40e-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4f40e-113">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4f40e-113">Elements and attributes</span></span>

<span data-ttu-id="4f40e-114">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f40e-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4f40e-115">親要素</span><span class="sxs-lookup"><span data-stu-id="4f40e-115">Parent elements</span></span>

|<span data-ttu-id="4f40e-116">**要素**</span><span class="sxs-lookup"><span data-stu-id="4f40e-116">**Element**</span></span>|<span data-ttu-id="4f40e-117">**型**</span><span class="sxs-lookup"><span data-stu-id="4f40e-117">**Type**</span></span>|<span data-ttu-id="4f40e-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="4f40e-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f40e-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="4f40e-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="4f40e-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="4f40e-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f40e-121">Visio ファイル内のドキュメント パーツ間の関係を再計算するための Microsoft Visio に指示を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f40e-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="4f40e-122">子要素</span><span class="sxs-lookup"><span data-stu-id="4f40e-122">Child elements</span></span>

<span data-ttu-id="4f40e-123">なし。</span><span class="sxs-lookup"><span data-stu-id="4f40e-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f40e-124">属性</span><span class="sxs-lookup"><span data-stu-id="4f40e-124">Attributes</span></span>

|<span data-ttu-id="4f40e-125">**属性**</span><span class="sxs-lookup"><span data-stu-id="4f40e-125">**Attribute**</span></span>|<span data-ttu-id="4f40e-126">**型**</span><span class="sxs-lookup"><span data-stu-id="4f40e-126">**Type**</span></span>|<span data-ttu-id="4f40e-127">**必須**</span><span class="sxs-lookup"><span data-stu-id="4f40e-127">**Required**</span></span>|<span data-ttu-id="4f40e-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="4f40e-128">**Description**</span></span>|<span data-ttu-id="4f40e-129">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="4f40e-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4f40e-130">ID</span><span class="sxs-lookup"><span data-stu-id="4f40e-130">ID</span></span>  <br/> |<span data-ttu-id="4f40e-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4f40e-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4f40e-132">必須</span><span class="sxs-lookup"><span data-stu-id="4f40e-132">required</span></span>  <br/> |<span data-ttu-id="4f40e-133">図面のページの [ID] 属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="4f40e-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="4f40e-134">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f40e-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4f40e-135">SV 要素</span><span class="sxs-lookup"><span data-stu-id="4f40e-135">T</span></span>  <br/> |<span data-ttu-id="4f40e-136">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4f40e-136">xsd:string</span></span>  <br/> |<span data-ttu-id="4f40e-137">必須</span><span class="sxs-lookup"><span data-stu-id="4f40e-137">required</span></span>  <br/> |<span data-ttu-id="4f40e-138">参照型を指定します。</span><span class="sxs-lookup"><span data-stu-id="4f40e-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="4f40e-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f40e-139">Values of the xsd:string type.</span></span>  <br/> |
   

