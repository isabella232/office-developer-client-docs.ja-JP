---
title: tp 要素 (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: 実行するタブ プロパティの先頭を指定します。 実行は、テキストの末尾、または次のタグまで定義されます。
ms.openlocfilehash: dad7a3de715473a75c601c1e391c9d51fc1cab85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542976"
---
# <a name="tp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="df0b9-104">tp 要素 (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="df0b9-104">tp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="df0b9-105">実行するタブ プロパティの先頭を指定します。</span><span class="sxs-lookup"><span data-stu-id="df0b9-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="df0b9-106">実行は、テキストの末尾、または次のタグまで定義されます。</span><span class="sxs-lookup"><span data-stu-id="df0b9-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df0b9-107">要素の情報</span><span class="sxs-lookup"><span data-stu-id="df0b9-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df0b9-108">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="df0b9-108">**Element type**</span></span> <br/> |[<span data-ttu-id="df0b9-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="df0b9-109">tp_Type complexType</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="df0b9-110">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="df0b9-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="df0b9-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="df0b9-111">**Schema file**</span></span> <br/> |<span data-ttu-id="df0b9-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="df0b9-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="df0b9-113">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="df0b9-113">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="df0b9-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="df0b9-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="df0b9-115">定義</span><span class="sxs-lookup"><span data-stu-id="df0b9-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="df0b9-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="df0b9-116">Elements and attributes</span></span>

<span data-ttu-id="df0b9-117">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="df0b9-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="df0b9-118">親要素</span><span class="sxs-lookup"><span data-stu-id="df0b9-118">Parent elements</span></span>

|<span data-ttu-id="df0b9-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="df0b9-119">**Element**</span></span>|<span data-ttu-id="df0b9-120">**型**</span><span class="sxs-lookup"><span data-stu-id="df0b9-120">**Type**</span></span>|<span data-ttu-id="df0b9-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="df0b9-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="df0b9-122">Text</span><span class="sxs-lookup"><span data-stu-id="df0b9-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="df0b9-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="df0b9-123">textType</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="df0b9-124">図形のテキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="df0b9-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="df0b9-125">子要素</span><span class="sxs-lookup"><span data-stu-id="df0b9-125">Child elements</span></span>

<span data-ttu-id="df0b9-126">なし。</span><span class="sxs-lookup"><span data-stu-id="df0b9-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df0b9-127">属性</span><span class="sxs-lookup"><span data-stu-id="df0b9-127">Attributes</span></span>

|<span data-ttu-id="df0b9-128">**属性**</span><span class="sxs-lookup"><span data-stu-id="df0b9-128">**Attribute**</span></span>|<span data-ttu-id="df0b9-129">**型**</span><span class="sxs-lookup"><span data-stu-id="df0b9-129">**Type**</span></span>|<span data-ttu-id="df0b9-130">**必須**</span><span class="sxs-lookup"><span data-stu-id="df0b9-130">**Required**</span></span>|<span data-ttu-id="df0b9-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="df0b9-131">**Description**</span></span>|<span data-ttu-id="df0b9-132">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="df0b9-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="df0b9-133">IX</span><span class="sxs-lookup"><span data-stu-id="df0b9-133">IX</span></span>  <br/> |<span data-ttu-id="df0b9-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="df0b9-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="df0b9-135">必須</span><span class="sxs-lookup"><span data-stu-id="df0b9-135">required</span></span>  <br/> |<span data-ttu-id="df0b9-136">親要素内の要素の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="df0b9-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="df0b9-137">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="df0b9-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

