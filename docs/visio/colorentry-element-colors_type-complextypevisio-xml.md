---
title: ColorEntry 要素 (Colors_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: カラー テーブルのエントリが含まれています。
ms.openlocfilehash: 14ef92069ce8d963ce4a0770324843321804c5cd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385341"
---
# <a name="colorentry-element-colorstype-complextype-visio-xml"></a><span data-ttu-id="32038-103">ColorEntry 要素 (Colors_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="32038-103">ColorEntry element (Colors_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="32038-104">カラー テーブルのエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="32038-104">Contains a color table entry.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="32038-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="32038-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32038-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="32038-106">**Element type**</span></span> <br/> |[<span data-ttu-id="32038-107">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="32038-107">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="32038-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="32038-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="32038-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="32038-109">**Schema file**</span></span> <br/> |<span data-ttu-id="32038-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="32038-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="32038-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="32038-111">**Document parts**</span></span> <br/> |<span data-ttu-id="32038-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="32038-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="32038-113">定義</span><span class="sxs-lookup"><span data-stu-id="32038-113">Definition</span></span>

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="32038-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="32038-114">Elements and attributes</span></span>

<span data-ttu-id="32038-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="32038-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="32038-116">親要素</span><span class="sxs-lookup"><span data-stu-id="32038-116">Parent elements</span></span>

|<span data-ttu-id="32038-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="32038-117">**Element**</span></span>|<span data-ttu-id="32038-118">**型**</span><span class="sxs-lookup"><span data-stu-id="32038-118">**Type**</span></span>|<span data-ttu-id="32038-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="32038-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="32038-120">色</span><span class="sxs-lookup"><span data-stu-id="32038-120">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="32038-121">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="32038-121">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="32038-122">図面のカラー テーブルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="32038-122">Contains the document's color table.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="32038-123">子要素</span><span class="sxs-lookup"><span data-stu-id="32038-123">Child elements</span></span>

<span data-ttu-id="32038-124">なし。</span><span class="sxs-lookup"><span data-stu-id="32038-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="32038-125">属性</span><span class="sxs-lookup"><span data-stu-id="32038-125">Attributes</span></span>

|<span data-ttu-id="32038-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="32038-126">**Attribute**</span></span>|<span data-ttu-id="32038-127">**型**</span><span class="sxs-lookup"><span data-stu-id="32038-127">**Type**</span></span>|<span data-ttu-id="32038-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="32038-128">**Required**</span></span>|<span data-ttu-id="32038-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="32038-129">**Description**</span></span>|<span data-ttu-id="32038-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="32038-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="32038-131">IX</span><span class="sxs-lookup"><span data-stu-id="32038-131">IX</span></span>  <br/> |<span data-ttu-id="32038-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="32038-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="32038-133">必須</span><span class="sxs-lookup"><span data-stu-id="32038-133">required</span></span>  <br/> |<span data-ttu-id="32038-134">その親要素内の要素の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="32038-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="32038-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="32038-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="32038-136">RGB</span><span class="sxs-lookup"><span data-stu-id="32038-136">RGB</span></span>  <br/> |<span data-ttu-id="32038-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="32038-137">xsd:string</span></span>  <br/> |<span data-ttu-id="32038-138">必須</span><span class="sxs-lookup"><span data-stu-id="32038-138">required</span></span>  <br/> |<span data-ttu-id="32038-139">カラー テーブルのエントリの 16 進値です。</span><span class="sxs-lookup"><span data-stu-id="32038-139">The hexadecimal value of the color table entry.</span></span>  <br/> |<span data-ttu-id="32038-140">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="32038-140">Values of the xsd:string type.</span></span>  <br/> |
   

