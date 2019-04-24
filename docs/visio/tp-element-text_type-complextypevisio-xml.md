---
title: tp 要素 (Text_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: tabs プロパティの実行開始を指定します。 実行は、テキストの末尾または次のタグまで定義されます。
ms.openlocfilehash: 3f27ea0babefa0ea69cbbc361031c57602649107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307701"
---
# <a name="tp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="b3ba1-104">tp 要素 (Text_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b3ba1-104">tp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b3ba1-105">tabs プロパティの実行開始を指定します。</span><span class="sxs-lookup"><span data-stu-id="b3ba1-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="b3ba1-106">実行は、テキストの末尾または次のタグまで定義されます。</span><span class="sxs-lookup"><span data-stu-id="b3ba1-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3ba1-107">要素情報</span><span class="sxs-lookup"><span data-stu-id="b3ba1-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3ba1-108">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="b3ba1-108">**Element type**</span></span> <br/> |[<span data-ttu-id="b3ba1-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="b3ba1-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b3ba1-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b3ba1-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b3ba1-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b3ba1-111">**Schema file**</span></span> <br/> |<span data-ttu-id="b3ba1-112">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="b3ba1-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b3ba1-113">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="b3ba1-113">**Document parts**</span></span> <br/> |<span data-ttu-id="b3ba1-114">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="b3ba1-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b3ba1-115">定義</span><span class="sxs-lookup"><span data-stu-id="b3ba1-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b3ba1-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b3ba1-116">Elements and attributes</span></span>

<span data-ttu-id="b3ba1-117">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3ba1-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b3ba1-118">親要素</span><span class="sxs-lookup"><span data-stu-id="b3ba1-118">Parent elements</span></span>

|<span data-ttu-id="b3ba1-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="b3ba1-119">**Element**</span></span>|<span data-ttu-id="b3ba1-120">**型**</span><span class="sxs-lookup"><span data-stu-id="b3ba1-120">**Type**</span></span>|<span data-ttu-id="b3ba1-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="b3ba1-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b3ba1-122">Text</span><span class="sxs-lookup"><span data-stu-id="b3ba1-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b3ba1-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="b3ba1-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b3ba1-124">図形のテキストを格納します。</span><span class="sxs-lookup"><span data-stu-id="b3ba1-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b3ba1-125">子要素</span><span class="sxs-lookup"><span data-stu-id="b3ba1-125">Child elements</span></span>

<span data-ttu-id="b3ba1-126">なし。</span><span class="sxs-lookup"><span data-stu-id="b3ba1-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3ba1-127">属性</span><span class="sxs-lookup"><span data-stu-id="b3ba1-127">Attributes</span></span>

|<span data-ttu-id="b3ba1-128">**属性**</span><span class="sxs-lookup"><span data-stu-id="b3ba1-128">**Attribute**</span></span>|<span data-ttu-id="b3ba1-129">**型**</span><span class="sxs-lookup"><span data-stu-id="b3ba1-129">**Type**</span></span>|<span data-ttu-id="b3ba1-130">**必須**</span><span class="sxs-lookup"><span data-stu-id="b3ba1-130">**Required**</span></span>|<span data-ttu-id="b3ba1-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="b3ba1-131">**Description**</span></span>|<span data-ttu-id="b3ba1-132">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="b3ba1-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b3ba1-133">IX</span><span class="sxs-lookup"><span data-stu-id="b3ba1-133">IX</span></span>  <br/> |<span data-ttu-id="b3ba1-134">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="b3ba1-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b3ba1-135">必須</span><span class="sxs-lookup"><span data-stu-id="b3ba1-135">required</span></span>  <br/> |<span data-ttu-id="b3ba1-136">親要素内の要素の0から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="b3ba1-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="b3ba1-137">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="b3ba1-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

