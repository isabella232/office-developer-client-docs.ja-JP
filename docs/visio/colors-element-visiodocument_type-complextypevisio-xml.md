---
title: Colors 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: 図面のカラーテーブルを含みます。
ms.openlocfilehash: 6f18926961583e09f83dd7921ca140c07a60ecc3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540176"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="8f510-103">Colors 要素 (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8f510-103">Colors element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8f510-104">図面のカラーテーブルを含みます。</span><span class="sxs-lookup"><span data-stu-id="8f510-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8f510-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="8f510-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f510-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8f510-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8f510-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="8f510-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8f510-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8f510-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8f510-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8f510-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8f510-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="8f510-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8f510-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="8f510-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8f510-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="8f510-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8f510-113">定義</span><span class="sxs-lookup"><span data-stu-id="8f510-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8f510-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8f510-114">Elements and attributes</span></span>

<span data-ttu-id="8f510-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f510-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8f510-116">親要素</span><span class="sxs-lookup"><span data-stu-id="8f510-116">Parent elements</span></span>

|<span data-ttu-id="8f510-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="8f510-117">**Element**</span></span>|<span data-ttu-id="8f510-118">**型**</span><span class="sxs-lookup"><span data-stu-id="8f510-118">**Type**</span></span>|<span data-ttu-id="8f510-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="8f510-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8f510-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="8f510-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="8f510-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="8f510-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8f510-122">Microsoft Visio 図面のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="8f510-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8f510-123">子要素</span><span class="sxs-lookup"><span data-stu-id="8f510-123">Child elements</span></span>

|<span data-ttu-id="8f510-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="8f510-124">**Element**</span></span>|<span data-ttu-id="8f510-125">**型**</span><span class="sxs-lookup"><span data-stu-id="8f510-125">**Type**</span></span>|<span data-ttu-id="8f510-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="8f510-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8f510-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="8f510-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8f510-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="8f510-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8f510-129">カラーテーブルエントリを含みます。</span><span class="sxs-lookup"><span data-stu-id="8f510-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8f510-130">属性</span><span class="sxs-lookup"><span data-stu-id="8f510-130">Attributes</span></span>

<span data-ttu-id="8f510-131">なし。</span><span class="sxs-lookup"><span data-stu-id="8f510-131">None.</span></span>
  

