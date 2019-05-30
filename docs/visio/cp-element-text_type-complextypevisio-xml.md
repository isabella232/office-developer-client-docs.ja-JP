---
title: cp 要素 (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: 対応する Char 要素に従って書式設定された文字プロパティ実行の開始位置を示します。 実行は、テキストの末尾、または次のタグまで定義されます。
ms.openlocfilehash: 70f7d3f8333ff0f2c109862455fbd8cc3b340bf4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540561"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="4d6fc-104">cp 要素 (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4d6fc-104">cp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4d6fc-105">対応する Char 要素に従って書式設定された文字プロパティ実行の開始位置を示します。</span><span class="sxs-lookup"><span data-stu-id="4d6fc-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="4d6fc-106">実行は、テキストの末尾、または次のタグまで定義されます。</span><span class="sxs-lookup"><span data-stu-id="4d6fc-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d6fc-107">要素の情報</span><span class="sxs-lookup"><span data-stu-id="4d6fc-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d6fc-108">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4d6fc-108">**Element type**</span></span> <br/> |[<span data-ttu-id="4d6fc-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="4d6fc-109">cp_Type complexType</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4d6fc-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4d6fc-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4d6fc-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4d6fc-111">**Schema file**</span></span> <br/> |<span data-ttu-id="4d6fc-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4d6fc-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4d6fc-113">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="4d6fc-113">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="4d6fc-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="4d6fc-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4d6fc-115">定義</span><span class="sxs-lookup"><span data-stu-id="4d6fc-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4d6fc-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4d6fc-116">Elements and attributes</span></span>

<span data-ttu-id="4d6fc-117">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d6fc-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4d6fc-118">親要素</span><span class="sxs-lookup"><span data-stu-id="4d6fc-118">Parent elements</span></span>

|<span data-ttu-id="4d6fc-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="4d6fc-119">**Element**</span></span>|<span data-ttu-id="4d6fc-120">**型**</span><span class="sxs-lookup"><span data-stu-id="4d6fc-120">**Type**</span></span>|<span data-ttu-id="4d6fc-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="4d6fc-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4d6fc-122">Text</span><span class="sxs-lookup"><span data-stu-id="4d6fc-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4d6fc-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="4d6fc-123">textType</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4d6fc-124">図形のテキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4d6fc-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4d6fc-125">子要素</span><span class="sxs-lookup"><span data-stu-id="4d6fc-125">Child elements</span></span>

<span data-ttu-id="4d6fc-126">なし。</span><span class="sxs-lookup"><span data-stu-id="4d6fc-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d6fc-127">属性</span><span class="sxs-lookup"><span data-stu-id="4d6fc-127">Attributes</span></span>

|<span data-ttu-id="4d6fc-128">**属性**</span><span class="sxs-lookup"><span data-stu-id="4d6fc-128">**Attribute**</span></span>|<span data-ttu-id="4d6fc-129">**型**</span><span class="sxs-lookup"><span data-stu-id="4d6fc-129">**Type**</span></span>|<span data-ttu-id="4d6fc-130">**必須**</span><span class="sxs-lookup"><span data-stu-id="4d6fc-130">**Required**</span></span>|<span data-ttu-id="4d6fc-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="4d6fc-131">**Description**</span></span>|<span data-ttu-id="4d6fc-132">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="4d6fc-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4d6fc-133">IX</span><span class="sxs-lookup"><span data-stu-id="4d6fc-133">IX</span></span>  <br/> |<span data-ttu-id="4d6fc-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4d6fc-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4d6fc-135">必須</span><span class="sxs-lookup"><span data-stu-id="4d6fc-135">required</span></span>  <br/> |<span data-ttu-id="4d6fc-136">このプロパティが実行する Char 要素インデックス。</span><span class="sxs-lookup"><span data-stu-id="4d6fc-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="4d6fc-137">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="4d6fc-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

