---
title: headermargin 要素 (HeaderFooter_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2bb0f4c5-eacf-e09b-2fce-dcff2d927557
description: 文書のヘッダーの余白を指定します。
ms.openlocfilehash: d8126ae73b1fb330234698343d14468fcbb3eed8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351668"
---
# <a name="headermargin-element-headerfootertype-complextype-visio-xml"></a><span data-ttu-id="cb7a2-103">headermargin 要素 (HeaderFooter_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="cb7a2-103">HeaderMargin element (HeaderFooter_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="cb7a2-104">文書のヘッダーの余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="cb7a2-104">Specifies the margin of a document's header.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb7a2-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="cb7a2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb7a2-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cb7a2-107">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="cb7a2-107">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cb7a2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cb7a2-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cb7a2-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="cb7a2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cb7a2-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cb7a2-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="cb7a2-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cb7a2-113">定義</span><span class="sxs-lookup"><span data-stu-id="cb7a2-113">Definition</span></span>

```XML
< xs:element name="HeaderMargin" type="HeaderMargin_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cb7a2-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="cb7a2-114">Elements and attributes</span></span>

<span data-ttu-id="cb7a2-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb7a2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cb7a2-116">親要素</span><span class="sxs-lookup"><span data-stu-id="cb7a2-116">Parent elements</span></span>

|<span data-ttu-id="cb7a2-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-117">**Element**</span></span>|<span data-ttu-id="cb7a2-118">**型**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-118">**Type**</span></span>|<span data-ttu-id="cb7a2-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cb7a2-120">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="cb7a2-120">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb7a2-121">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="cb7a2-121">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb7a2-122">文書のヘッダーとフッターの要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="cb7a2-122">Contains elements for a document's header and footer.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cb7a2-123">子要素</span><span class="sxs-lookup"><span data-stu-id="cb7a2-123">Child elements</span></span>

<span data-ttu-id="cb7a2-124">なし。</span><span class="sxs-lookup"><span data-stu-id="cb7a2-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb7a2-125">属性</span><span class="sxs-lookup"><span data-stu-id="cb7a2-125">Attributes</span></span>

|<span data-ttu-id="cb7a2-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-126">**Attribute**</span></span>|<span data-ttu-id="cb7a2-127">**型**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-127">**Type**</span></span>|<span data-ttu-id="cb7a2-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-128">**Required**</span></span>|<span data-ttu-id="cb7a2-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-129">**Description**</span></span>|<span data-ttu-id="cb7a2-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="cb7a2-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cb7a2-131">単位</span><span class="sxs-lookup"><span data-stu-id="cb7a2-131">Unit</span></span>  <br/> |<span data-ttu-id="cb7a2-132">xsd: string</span><span class="sxs-lookup"><span data-stu-id="cb7a2-132">xsd:string</span></span>  <br/> |<span data-ttu-id="cb7a2-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb7a2-133">optional</span></span>  <br/> |<span data-ttu-id="cb7a2-134">測定単位を表します。</span><span class="sxs-lookup"><span data-stu-id="cb7a2-134">Represents a unit of measure.</span></span> <span data-ttu-id="cb7a2-135">既定値は DP です。</span><span class="sxs-lookup"><span data-stu-id="cb7a2-135">The default is DP.</span></span>  <br/> |<span data-ttu-id="cb7a2-136">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb7a2-136">Values of the xsd:string type.</span></span>  <br/> |
   

