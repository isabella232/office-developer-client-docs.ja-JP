---
title: Colors 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: ドキュメントのカラーテーブルが含まれます。
ms.openlocfilehash: 6f18926961583e09f83dd7921ca140c07a60ecc3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540176"
---
# <a name="colors-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="be388-103">Colors 要素 (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="be388-103">Colors element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="be388-104">ドキュメントのカラーテーブルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="be388-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be388-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="be388-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be388-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="be388-106">**Element type**</span></span> <br/> |[<span data-ttu-id="be388-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="be388-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="be388-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="be388-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="be388-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="be388-109">**Schema file**</span></span> <br/> |<span data-ttu-id="be388-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="be388-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="be388-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="be388-111">**Document parts**</span></span> <br/> |<span data-ttu-id="be388-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="be388-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="be388-113">定義</span><span class="sxs-lookup"><span data-stu-id="be388-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="be388-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="be388-114">Elements and attributes</span></span>

<span data-ttu-id="be388-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="be388-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="be388-116">親要素</span><span class="sxs-lookup"><span data-stu-id="be388-116">Parent elements</span></span>

|<span data-ttu-id="be388-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="be388-117">**Element**</span></span>|<span data-ttu-id="be388-118">**型**</span><span class="sxs-lookup"><span data-stu-id="be388-118">**Type**</span></span>|<span data-ttu-id="be388-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="be388-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="be388-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="be388-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="be388-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="be388-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be388-122">Microsoft ドキュメントのルートVisioです。</span><span class="sxs-lookup"><span data-stu-id="be388-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="be388-123">子要素</span><span class="sxs-lookup"><span data-stu-id="be388-123">Child elements</span></span>

|<span data-ttu-id="be388-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="be388-124">**Element**</span></span>|<span data-ttu-id="be388-125">**型**</span><span class="sxs-lookup"><span data-stu-id="be388-125">**Type**</span></span>|<span data-ttu-id="be388-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="be388-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="be388-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="be388-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be388-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="be388-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be388-129">カラー テーブル エントリが含まれます。</span><span class="sxs-lookup"><span data-stu-id="be388-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="be388-130">属性</span><span class="sxs-lookup"><span data-stu-id="be388-130">Attributes</span></span>

<span data-ttu-id="be388-131">なし。</span><span class="sxs-lookup"><span data-stu-id="be388-131">None.</span></span>
  

