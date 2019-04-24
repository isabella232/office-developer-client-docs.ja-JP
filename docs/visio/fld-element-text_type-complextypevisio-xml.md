---
title: fld 要素 (Text_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: 対応する field 要素のテキストフィールドの挿入ポイントを示します。
ms.openlocfilehash: a7303697a9471dab68f5b1cf851f60d51650a84e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346215"
---
# <a name="fld-element-texttype-complextype-visio-xml"></a><span data-ttu-id="e6f3e-103">fld 要素 (Text_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="e6f3e-103">fld element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e6f3e-104">対応する**field**要素のテキストフィールドの挿入ポイントを示します。</span><span class="sxs-lookup"><span data-stu-id="e6f3e-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e6f3e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="e6f3e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6f3e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="e6f3e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e6f3e-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="e6f3e-107">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e6f3e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e6f3e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e6f3e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e6f3e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e6f3e-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="e6f3e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e6f3e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="e6f3e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e6f3e-112">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="e6f3e-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e6f3e-113">定義</span><span class="sxs-lookup"><span data-stu-id="e6f3e-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e6f3e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e6f3e-114">Elements and attributes</span></span>

<span data-ttu-id="e6f3e-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e6f3e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e6f3e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="e6f3e-116">Parent elements</span></span>

|<span data-ttu-id="e6f3e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="e6f3e-117">**Element**</span></span>|<span data-ttu-id="e6f3e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="e6f3e-118">**Type**</span></span>|<span data-ttu-id="e6f3e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="e6f3e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e6f3e-120">Text</span><span class="sxs-lookup"><span data-stu-id="e6f3e-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e6f3e-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="e6f3e-121">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e6f3e-122">図形のテキストを格納します。</span><span class="sxs-lookup"><span data-stu-id="e6f3e-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e6f3e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="e6f3e-123">Child elements</span></span>

<span data-ttu-id="e6f3e-124">なし。</span><span class="sxs-lookup"><span data-stu-id="e6f3e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6f3e-125">属性</span><span class="sxs-lookup"><span data-stu-id="e6f3e-125">Attributes</span></span>

|<span data-ttu-id="e6f3e-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="e6f3e-126">**Attribute**</span></span>|<span data-ttu-id="e6f3e-127">**型**</span><span class="sxs-lookup"><span data-stu-id="e6f3e-127">**Type**</span></span>|<span data-ttu-id="e6f3e-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="e6f3e-128">**Required**</span></span>|<span data-ttu-id="e6f3e-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="e6f3e-129">**Description**</span></span>|<span data-ttu-id="e6f3e-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="e6f3e-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e6f3e-131">IX</span><span class="sxs-lookup"><span data-stu-id="e6f3e-131">IX</span></span>  <br/> |<span data-ttu-id="e6f3e-132">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="e6f3e-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e6f3e-133">必須</span><span class="sxs-lookup"><span data-stu-id="e6f3e-133">required</span></span>  <br/> |<span data-ttu-id="e6f3e-134">親要素内の要素の0から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="e6f3e-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="e6f3e-135">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="e6f3e-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

