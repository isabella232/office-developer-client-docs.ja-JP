---
title: HeaderMargin 要素 (HeaderFooter_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2bb0f4c5-eacf-e09b-2fce-dcff2d927557
description: 図面のヘッダーの余白を指定します。
ms.openlocfilehash: a0accb08fd2c781e112b7b54e074dccd4c4e4307
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805517"
---
# <a name="headermargin-element-headerfootertype-complextype-visio-xml"></a><span data-ttu-id="d6783-103">HeaderMargin 要素 (HeaderFooter_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="d6783-103">HeaderMargin element (HeaderFooter_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d6783-104">図面のヘッダーの余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="d6783-104">Specifies the margin of a document's header.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6783-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d6783-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6783-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="d6783-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d6783-107">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="d6783-107">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d6783-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="d6783-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d6783-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d6783-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d6783-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d6783-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d6783-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d6783-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d6783-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="d6783-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d6783-113">定義</span><span class="sxs-lookup"><span data-stu-id="d6783-113">Definition</span></span>

```XML
< xs:element name="HeaderMargin" type="HeaderMargin_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d6783-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d6783-114">Elements and attributes</span></span>

<span data-ttu-id="d6783-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d6783-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d6783-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d6783-116">Parent elements</span></span>

|<span data-ttu-id="d6783-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d6783-117">**Element**</span></span>|<span data-ttu-id="d6783-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d6783-118">**Type**</span></span>|<span data-ttu-id="d6783-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d6783-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d6783-120">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="d6783-120">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d6783-121">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="d6783-121">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d6783-122">ドキュメントのヘッダーとフッターの要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d6783-122">Contains elements for a document's header and footer.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d6783-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d6783-123">Child elements</span></span>

<span data-ttu-id="d6783-124">なし。</span><span class="sxs-lookup"><span data-stu-id="d6783-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6783-125">属性</span><span class="sxs-lookup"><span data-stu-id="d6783-125">Attributes</span></span>

|<span data-ttu-id="d6783-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="d6783-126">**Attribute**</span></span>|<span data-ttu-id="d6783-127">**型**</span><span class="sxs-lookup"><span data-stu-id="d6783-127">**Type**</span></span>|<span data-ttu-id="d6783-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="d6783-128">**Required**</span></span>|<span data-ttu-id="d6783-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="d6783-129">**Description**</span></span>|<span data-ttu-id="d6783-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="d6783-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d6783-131">種類</span><span class="sxs-lookup"><span data-stu-id="d6783-131">Unit</span></span>  <br/> |<span data-ttu-id="d6783-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d6783-132">xsd:string</span></span>  <br/> |<span data-ttu-id="d6783-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="d6783-133">optional</span></span>  <br/> |<span data-ttu-id="d6783-134">計量単位を表します。</span><span class="sxs-lookup"><span data-stu-id="d6783-134">Represents a unit of measure.</span></span> <span data-ttu-id="d6783-135">DP は、既定では。</span><span class="sxs-lookup"><span data-stu-id="d6783-135">The default is DP.</span></span>  <br/> |<span data-ttu-id="d6783-136">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d6783-136">Values of the xsd:string type.</span></span>  <br/> |
   

