---
title: ColorEntry 要素 (Colors_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: カラー テーブルのエントリが含まれています。
ms.openlocfilehash: 934680b36428dd272d383ce421e86ae6d5c707cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805037"
---
# <a name="colorentry-element-colorstype-complextype-visio-xml"></a><span data-ttu-id="27688-103">ColorEntry 要素 (Colors_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="27688-103">ColorEntry element (Colors_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="27688-104">カラー テーブルのエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="27688-104">Contains a color table entry.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27688-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="27688-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27688-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="27688-106">**Element type**</span></span> <br/> |[<span data-ttu-id="27688-107">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="27688-107">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="27688-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="27688-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="27688-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="27688-109">**Schema file**</span></span> <br/> |<span data-ttu-id="27688-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="27688-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="27688-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="27688-111">**Document parts**</span></span> <br/> |<span data-ttu-id="27688-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="27688-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="27688-113">定義</span><span class="sxs-lookup"><span data-stu-id="27688-113">Definition</span></span>

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="27688-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="27688-114">Elements and attributes</span></span>

<span data-ttu-id="27688-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="27688-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="27688-116">親要素</span><span class="sxs-lookup"><span data-stu-id="27688-116">Parent elements</span></span>

|<span data-ttu-id="27688-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="27688-117">**Element**</span></span>|<span data-ttu-id="27688-118">**型**</span><span class="sxs-lookup"><span data-stu-id="27688-118">**Type**</span></span>|<span data-ttu-id="27688-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="27688-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="27688-120">色</span><span class="sxs-lookup"><span data-stu-id="27688-120">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="27688-121">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="27688-121">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="27688-122">図面のカラー テーブルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="27688-122">Contains the document's color table.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="27688-123">子要素</span><span class="sxs-lookup"><span data-stu-id="27688-123">Child elements</span></span>

<span data-ttu-id="27688-124">なし。</span><span class="sxs-lookup"><span data-stu-id="27688-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27688-125">属性</span><span class="sxs-lookup"><span data-stu-id="27688-125">Attributes</span></span>

|<span data-ttu-id="27688-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="27688-126">**Attribute**</span></span>|<span data-ttu-id="27688-127">**型**</span><span class="sxs-lookup"><span data-stu-id="27688-127">**Type**</span></span>|<span data-ttu-id="27688-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="27688-128">**Required**</span></span>|<span data-ttu-id="27688-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="27688-129">**Description**</span></span>|<span data-ttu-id="27688-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="27688-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="27688-131">IX</span><span class="sxs-lookup"><span data-stu-id="27688-131">IX</span></span>  <br/> |<span data-ttu-id="27688-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="27688-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="27688-133">必須</span><span class="sxs-lookup"><span data-stu-id="27688-133">required</span></span>  <br/> |<span data-ttu-id="27688-134">その親要素内の要素の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="27688-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="27688-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27688-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="27688-136">RGB</span><span class="sxs-lookup"><span data-stu-id="27688-136">RGB</span></span>  <br/> |<span data-ttu-id="27688-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="27688-137">xsd:string</span></span>  <br/> |<span data-ttu-id="27688-138">必須</span><span class="sxs-lookup"><span data-stu-id="27688-138">required</span></span>  <br/> |<span data-ttu-id="27688-139">カラー テーブルのエントリの 16 進値です。</span><span class="sxs-lookup"><span data-stu-id="27688-139">The hexadecimal value of the color table entry.</span></span>  <br/> |<span data-ttu-id="27688-140">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27688-140">Values of the xsd:string type.</span></span>  <br/> |
   

