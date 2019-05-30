---
title: HeaderMargin 要素 (HeaderFooter_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2bb0f4c5-eacf-e09b-2fce-dcff2d927557
description: 文書のヘッダーの余白を指定します。
ms.openlocfilehash: b7c055e818c490399df66e3e7ba626afc9645851
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539128"
---
# <a name="headermargin-element-headerfootertype-complextype-visio-xml"></a><span data-ttu-id="24190-103">HeaderMargin 要素 (HeaderFooter_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="24190-103">HeaderMargin element (HeaderFooter_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="24190-104">文書のヘッダーの余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="24190-104">Specifies the margin of a document's header.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="24190-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="24190-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24190-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="24190-106">**Element type**</span></span> <br/> |[<span data-ttu-id="24190-107">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="24190-107">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="24190-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="24190-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="24190-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="24190-109">**Schema file**</span></span> <br/> |<span data-ttu-id="24190-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="24190-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="24190-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="24190-111">**Document parts**</span></span> <br/> |<span data-ttu-id="24190-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="24190-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="24190-113">定義</span><span class="sxs-lookup"><span data-stu-id="24190-113">Definition</span></span>

```XML
< xs:element name="HeaderMargin" type="HeaderMargin_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="24190-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="24190-114">Elements and attributes</span></span>

<span data-ttu-id="24190-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="24190-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="24190-116">親要素</span><span class="sxs-lookup"><span data-stu-id="24190-116">Parent elements</span></span>

|<span data-ttu-id="24190-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="24190-117">**Element**</span></span>|<span data-ttu-id="24190-118">**型**</span><span class="sxs-lookup"><span data-stu-id="24190-118">**Type**</span></span>|<span data-ttu-id="24190-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="24190-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="24190-120">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="24190-120">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="24190-121">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="24190-121">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="24190-122">文書のヘッダーとフッターの要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="24190-122">Contains elements for a document's header and footer.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="24190-123">子要素</span><span class="sxs-lookup"><span data-stu-id="24190-123">Child elements</span></span>

<span data-ttu-id="24190-124">なし。</span><span class="sxs-lookup"><span data-stu-id="24190-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24190-125">属性</span><span class="sxs-lookup"><span data-stu-id="24190-125">Attributes</span></span>

|<span data-ttu-id="24190-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="24190-126">**Attribute**</span></span>|<span data-ttu-id="24190-127">**型**</span><span class="sxs-lookup"><span data-stu-id="24190-127">**Type**</span></span>|<span data-ttu-id="24190-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="24190-128">**Required**</span></span>|<span data-ttu-id="24190-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="24190-129">**Description**</span></span>|<span data-ttu-id="24190-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="24190-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="24190-131">単位</span><span class="sxs-lookup"><span data-stu-id="24190-131">Unit</span></span>  <br/> |<span data-ttu-id="24190-132">xsd: string</span><span class="sxs-lookup"><span data-stu-id="24190-132">xsd:string</span></span>  <br/> |<span data-ttu-id="24190-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="24190-133">optional</span></span>  <br/> |<span data-ttu-id="24190-134">測定単位を表します。</span><span class="sxs-lookup"><span data-stu-id="24190-134">Represents a unit of measure.</span></span> <span data-ttu-id="24190-135">既定値は DP です。</span><span class="sxs-lookup"><span data-stu-id="24190-135">The default is DP.</span></span>  <br/> |<span data-ttu-id="24190-136">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="24190-136">Values of the xsd:string type.</span></span>  <br/> |
   

