---
title: pp 要素 (Text_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: 段落のプロパティの最初の実行を指定します。 実行は、次のタグまで、テキストの末尾に定義されています。
ms.openlocfilehash: ce1bdd89ca9a5eb5b7ce9b73cc2354ccfde1c125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806088"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="e2c75-104">pp 要素 (Text_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="e2c75-104">pp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e2c75-105">段落のプロパティの最初の実行を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2c75-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="e2c75-106">実行は、次のタグまで、テキストの末尾に定義されています。</span><span class="sxs-lookup"><span data-stu-id="e2c75-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2c75-107">要素情報</span><span class="sxs-lookup"><span data-stu-id="e2c75-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2c75-108">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="e2c75-108">**Element type**</span></span> <br/> |[<span data-ttu-id="e2c75-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="e2c75-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e2c75-110">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="e2c75-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e2c75-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e2c75-111">**Schema file**</span></span> <br/> |<span data-ttu-id="e2c75-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e2c75-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e2c75-113">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="e2c75-113">**Document parts**</span></span> <br/> |<span data-ttu-id="e2c75-114"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="e2c75-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e2c75-115">定義</span><span class="sxs-lookup"><span data-stu-id="e2c75-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e2c75-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e2c75-116">Elements and attributes</span></span>

<span data-ttu-id="e2c75-117">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2c75-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e2c75-118">親要素</span><span class="sxs-lookup"><span data-stu-id="e2c75-118">Parent elements</span></span>

|<span data-ttu-id="e2c75-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="e2c75-119">**Element**</span></span>|<span data-ttu-id="e2c75-120">**型**</span><span class="sxs-lookup"><span data-stu-id="e2c75-120">**Type**</span></span>|<span data-ttu-id="e2c75-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="e2c75-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e2c75-122">Text</span><span class="sxs-lookup"><span data-stu-id="e2c75-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e2c75-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="e2c75-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e2c75-124">図形のテキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e2c75-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e2c75-125">子要素</span><span class="sxs-lookup"><span data-stu-id="e2c75-125">Child elements</span></span>

<span data-ttu-id="e2c75-126">なし。</span><span class="sxs-lookup"><span data-stu-id="e2c75-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2c75-127">属性</span><span class="sxs-lookup"><span data-stu-id="e2c75-127">Attributes</span></span>

|<span data-ttu-id="e2c75-128">**属性**</span><span class="sxs-lookup"><span data-stu-id="e2c75-128">**Attribute**</span></span>|<span data-ttu-id="e2c75-129">**型**</span><span class="sxs-lookup"><span data-stu-id="e2c75-129">**Type**</span></span>|<span data-ttu-id="e2c75-130">**必須**</span><span class="sxs-lookup"><span data-stu-id="e2c75-130">**Required**</span></span>|<span data-ttu-id="e2c75-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="e2c75-131">**Description**</span></span>|<span data-ttu-id="e2c75-132">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="e2c75-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e2c75-133">IX</span><span class="sxs-lookup"><span data-stu-id="e2c75-133">IX</span></span>  <br/> |<span data-ttu-id="e2c75-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e2c75-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e2c75-135">必須</span><span class="sxs-lookup"><span data-stu-id="e2c75-135">required</span></span>  <br/> |<span data-ttu-id="e2c75-136">この実行に適用された書式を指定する**段落**要素のインデックス。</span><span class="sxs-lookup"><span data-stu-id="e2c75-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="e2c75-137">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e2c75-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

