---
title: pp 要素 (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: 段落のプロパティを実行する開始日を指定します。 実行は、テキストの末尾または次のタグまで定義されます。
ms.openlocfilehash: 695958c77f730abed03f50d6ad9c71f4de76dd63
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537739"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="82e9b-104">pp 要素 (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="82e9b-104">pp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="82e9b-105">段落のプロパティを実行する開始日を指定します。</span><span class="sxs-lookup"><span data-stu-id="82e9b-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="82e9b-106">実行は、テキストの末尾または次のタグまで定義されます。</span><span class="sxs-lookup"><span data-stu-id="82e9b-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82e9b-107">要素情報</span><span class="sxs-lookup"><span data-stu-id="82e9b-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82e9b-108">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="82e9b-108">**Element type**</span></span> <br/> |[<span data-ttu-id="82e9b-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="82e9b-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="82e9b-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="82e9b-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="82e9b-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="82e9b-111">**Schema file**</span></span> <br/> |<span data-ttu-id="82e9b-112">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="82e9b-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="82e9b-113">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="82e9b-113">**Document parts**</span></span> <br/> |<span data-ttu-id="82e9b-114">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="82e9b-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="82e9b-115">定義</span><span class="sxs-lookup"><span data-stu-id="82e9b-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="82e9b-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="82e9b-116">Elements and attributes</span></span>

<span data-ttu-id="82e9b-117">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="82e9b-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="82e9b-118">親要素</span><span class="sxs-lookup"><span data-stu-id="82e9b-118">Parent elements</span></span>

|<span data-ttu-id="82e9b-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="82e9b-119">**Element**</span></span>|<span data-ttu-id="82e9b-120">**型**</span><span class="sxs-lookup"><span data-stu-id="82e9b-120">**Type**</span></span>|<span data-ttu-id="82e9b-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="82e9b-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="82e9b-122">Text</span><span class="sxs-lookup"><span data-stu-id="82e9b-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e9b-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="82e9b-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="82e9b-124">図形のテキストを格納します。</span><span class="sxs-lookup"><span data-stu-id="82e9b-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="82e9b-125">子要素</span><span class="sxs-lookup"><span data-stu-id="82e9b-125">Child elements</span></span>

<span data-ttu-id="82e9b-126">なし。</span><span class="sxs-lookup"><span data-stu-id="82e9b-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82e9b-127">属性</span><span class="sxs-lookup"><span data-stu-id="82e9b-127">Attributes</span></span>

|<span data-ttu-id="82e9b-128">**属性**</span><span class="sxs-lookup"><span data-stu-id="82e9b-128">**Attribute**</span></span>|<span data-ttu-id="82e9b-129">**型**</span><span class="sxs-lookup"><span data-stu-id="82e9b-129">**Type**</span></span>|<span data-ttu-id="82e9b-130">**必須**</span><span class="sxs-lookup"><span data-stu-id="82e9b-130">**Required**</span></span>|<span data-ttu-id="82e9b-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="82e9b-131">**Description**</span></span>|<span data-ttu-id="82e9b-132">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="82e9b-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="82e9b-133">IX</span><span class="sxs-lookup"><span data-stu-id="82e9b-133">IX</span></span>  <br/> |<span data-ttu-id="82e9b-134">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="82e9b-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="82e9b-135">必須</span><span class="sxs-lookup"><span data-stu-id="82e9b-135">required</span></span>  <br/> |<span data-ttu-id="82e9b-136">この実行に適用される書式を指定する、[**段落**] 要素のインデックスです。</span><span class="sxs-lookup"><span data-stu-id="82e9b-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="82e9b-137">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="82e9b-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

