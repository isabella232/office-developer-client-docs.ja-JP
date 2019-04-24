---
title: Colors 要素 (VisioDocument_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: 図面のカラーテーブルを含みます。
ms.openlocfilehash: bd46f58dfbb8a596717662b9a0524d59bb508270
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358759"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="994ed-103">Colors 要素 (VisioDocument_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="994ed-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="994ed-104">図面のカラーテーブルを含みます。</span><span class="sxs-lookup"><span data-stu-id="994ed-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="994ed-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="994ed-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="994ed-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="994ed-106">**Element type**</span></span> <br/> |[<span data-ttu-id="994ed-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="994ed-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="994ed-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="994ed-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="994ed-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="994ed-109">**Schema file**</span></span> <br/> |<span data-ttu-id="994ed-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="994ed-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="994ed-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="994ed-111">**Document parts**</span></span> <br/> |<span data-ttu-id="994ed-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="994ed-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="994ed-113">定義</span><span class="sxs-lookup"><span data-stu-id="994ed-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="994ed-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="994ed-114">Elements and attributes</span></span>

<span data-ttu-id="994ed-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="994ed-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="994ed-116">親要素</span><span class="sxs-lookup"><span data-stu-id="994ed-116">Parent elements</span></span>

|<span data-ttu-id="994ed-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="994ed-117">**Element**</span></span>|<span data-ttu-id="994ed-118">**型**</span><span class="sxs-lookup"><span data-stu-id="994ed-118">**Type**</span></span>|<span data-ttu-id="994ed-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="994ed-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="994ed-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="994ed-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="994ed-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="994ed-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="994ed-122">Microsoft Visio 図面のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="994ed-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="994ed-123">子要素</span><span class="sxs-lookup"><span data-stu-id="994ed-123">Child elements</span></span>

|<span data-ttu-id="994ed-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="994ed-124">**Element**</span></span>|<span data-ttu-id="994ed-125">**型**</span><span class="sxs-lookup"><span data-stu-id="994ed-125">**Type**</span></span>|<span data-ttu-id="994ed-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="994ed-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="994ed-127">colorentry</span><span class="sxs-lookup"><span data-stu-id="994ed-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="994ed-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="994ed-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="994ed-129">カラーテーブルエントリを含みます。</span><span class="sxs-lookup"><span data-stu-id="994ed-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="994ed-130">属性</span><span class="sxs-lookup"><span data-stu-id="994ed-130">Attributes</span></span>

<span data-ttu-id="994ed-131">なし。</span><span class="sxs-lookup"><span data-stu-id="994ed-131">None.</span></span>
  

