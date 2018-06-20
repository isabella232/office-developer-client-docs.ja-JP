---
title: tp 要素 (Text_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: 実行タブのプロパティの先頭を指定します。 実行は、次のタグまで、テキストの末尾に定義されています。
ms.openlocfilehash: 9b98374af4ffbf2eaeaea61dcb1dbb49214f01b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806673"
---
# <a name="tp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="b5f69-104">tp 要素 (Text_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="b5f69-104">tp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b5f69-105">実行タブのプロパティの先頭を指定します。</span><span class="sxs-lookup"><span data-stu-id="b5f69-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="b5f69-106">実行は、次のタグまで、テキストの末尾に定義されています。</span><span class="sxs-lookup"><span data-stu-id="b5f69-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5f69-107">要素情報</span><span class="sxs-lookup"><span data-stu-id="b5f69-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5f69-108">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="b5f69-108">**Element type**</span></span> <br/> |[<span data-ttu-id="b5f69-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="b5f69-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b5f69-110">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="b5f69-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b5f69-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b5f69-111">**Schema file**</span></span> <br/> |<span data-ttu-id="b5f69-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b5f69-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b5f69-113">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="b5f69-113">**Document parts**</span></span> <br/> |<span data-ttu-id="b5f69-114"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="b5f69-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5f69-115">定義</span><span class="sxs-lookup"><span data-stu-id="b5f69-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5f69-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b5f69-116">Elements and attributes</span></span>

<span data-ttu-id="b5f69-117">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5f69-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b5f69-118">親要素</span><span class="sxs-lookup"><span data-stu-id="b5f69-118">Parent elements</span></span>

|<span data-ttu-id="b5f69-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="b5f69-119">**Element**</span></span>|<span data-ttu-id="b5f69-120">**型**</span><span class="sxs-lookup"><span data-stu-id="b5f69-120">**Type**</span></span>|<span data-ttu-id="b5f69-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="b5f69-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5f69-122">Text</span><span class="sxs-lookup"><span data-stu-id="b5f69-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b5f69-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="b5f69-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b5f69-124">図形のテキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5f69-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b5f69-125">子要素</span><span class="sxs-lookup"><span data-stu-id="b5f69-125">Child elements</span></span>

<span data-ttu-id="b5f69-126">なし。</span><span class="sxs-lookup"><span data-stu-id="b5f69-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5f69-127">属性</span><span class="sxs-lookup"><span data-stu-id="b5f69-127">Attributes</span></span>

|<span data-ttu-id="b5f69-128">**属性**</span><span class="sxs-lookup"><span data-stu-id="b5f69-128">**Attribute**</span></span>|<span data-ttu-id="b5f69-129">**型**</span><span class="sxs-lookup"><span data-stu-id="b5f69-129">**Type**</span></span>|<span data-ttu-id="b5f69-130">**必須**</span><span class="sxs-lookup"><span data-stu-id="b5f69-130">**Required**</span></span>|<span data-ttu-id="b5f69-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="b5f69-131">**Description**</span></span>|<span data-ttu-id="b5f69-132">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="b5f69-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b5f69-133">IX</span><span class="sxs-lookup"><span data-stu-id="b5f69-133">IX</span></span>  <br/> |<span data-ttu-id="b5f69-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b5f69-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b5f69-135">必須</span><span class="sxs-lookup"><span data-stu-id="b5f69-135">required</span></span>  <br/> |<span data-ttu-id="b5f69-136">その親要素内の要素の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="b5f69-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="b5f69-137">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5f69-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

