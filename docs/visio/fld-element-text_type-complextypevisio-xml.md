---
title: フォルダーの要素 (Text_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: 対応するフィールド要素のテキスト フィールドのテキスト挿入点を示します。
ms.openlocfilehash: a7303697a9471dab68f5b1cf851f60d51650a84e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383325"
---
# <a name="fld-element-texttype-complextype-visio-xml"></a><span data-ttu-id="4a886-103">フォルダーの要素 (Text_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="4a886-103">fld element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4a886-104">対応する**フィールド**要素のテキスト フィールドのテキスト挿入点を示します。</span><span class="sxs-lookup"><span data-stu-id="4a886-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4a886-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="4a886-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a886-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4a886-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4a886-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="4a886-107">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4a886-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="4a886-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4a886-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4a886-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4a886-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4a886-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4a886-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="4a886-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4a886-112"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="4a886-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4a886-113">定義</span><span class="sxs-lookup"><span data-stu-id="4a886-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4a886-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4a886-114">Elements and attributes</span></span>

<span data-ttu-id="4a886-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a886-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4a886-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4a886-116">Parent elements</span></span>

|<span data-ttu-id="4a886-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="4a886-117">**Element**</span></span>|<span data-ttu-id="4a886-118">**型**</span><span class="sxs-lookup"><span data-stu-id="4a886-118">**Type**</span></span>|<span data-ttu-id="4a886-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="4a886-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4a886-120">Text</span><span class="sxs-lookup"><span data-stu-id="4a886-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a886-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="4a886-121">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a886-122">図形のテキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4a886-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4a886-123">子要素</span><span class="sxs-lookup"><span data-stu-id="4a886-123">Child elements</span></span>

<span data-ttu-id="4a886-124">なし。</span><span class="sxs-lookup"><span data-stu-id="4a886-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a886-125">属性</span><span class="sxs-lookup"><span data-stu-id="4a886-125">Attributes</span></span>

|<span data-ttu-id="4a886-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="4a886-126">**Attribute**</span></span>|<span data-ttu-id="4a886-127">**型**</span><span class="sxs-lookup"><span data-stu-id="4a886-127">**Type**</span></span>|<span data-ttu-id="4a886-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="4a886-128">**Required**</span></span>|<span data-ttu-id="4a886-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="4a886-129">**Description**</span></span>|<span data-ttu-id="4a886-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="4a886-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4a886-131">IX</span><span class="sxs-lookup"><span data-stu-id="4a886-131">IX</span></span>  <br/> |<span data-ttu-id="4a886-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4a886-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4a886-133">必須</span><span class="sxs-lookup"><span data-stu-id="4a886-133">required</span></span>  <br/> |<span data-ttu-id="4a886-134">その親要素内の要素の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="4a886-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="4a886-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a886-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

