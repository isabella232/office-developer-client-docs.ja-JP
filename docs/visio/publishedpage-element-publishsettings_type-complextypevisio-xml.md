---
title: PublishedPage 要素 (PublishSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: 図面ページを 2013 の [サービス] を使用してブラウザー Visio表示Microsoft SharePoint Serverします。
ms.openlocfilehash: 614c01f12b9a7525620704e5417a106e8703c983
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538376"
---
# <a name="publishedpage-element-publishsettings_type-complextype-visio-xml"></a><span data-ttu-id="a2794-103">PublishedPage 要素 (PublishSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a2794-103">PublishedPage element (PublishSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="a2794-104">図面ページを 2013 の [サービス] を使用してブラウザー Visio表示Microsoft SharePoint Serverします。</span><span class="sxs-lookup"><span data-stu-id="a2794-104">Specifies whether a drawing page is viewable in the browser using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a2794-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="a2794-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2794-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a2794-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a2794-107">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="a2794-107">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a2794-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a2794-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a2794-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a2794-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a2794-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a2794-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a2794-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="a2794-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a2794-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="a2794-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a2794-113">定義</span><span class="sxs-lookup"><span data-stu-id="a2794-113">Definition</span></span>

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a2794-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a2794-114">Elements and attributes</span></span>

<span data-ttu-id="a2794-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2794-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a2794-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a2794-116">Parent elements</span></span>

|<span data-ttu-id="a2794-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a2794-117">**Element**</span></span>|<span data-ttu-id="a2794-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a2794-118">**Type**</span></span>|<span data-ttu-id="a2794-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a2794-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a2794-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="a2794-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2794-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a2794-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a2794-122">[サービス] を使用してダイアグラムを開く際に使用する設定Visioします。</span><span class="sxs-lookup"><span data-stu-id="a2794-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a2794-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a2794-123">Child elements</span></span>

<span data-ttu-id="a2794-124">なし。</span><span class="sxs-lookup"><span data-stu-id="a2794-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2794-125">属性</span><span class="sxs-lookup"><span data-stu-id="a2794-125">Attributes</span></span>

|<span data-ttu-id="a2794-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="a2794-126">**Attribute**</span></span>|<span data-ttu-id="a2794-127">**型**</span><span class="sxs-lookup"><span data-stu-id="a2794-127">**Type**</span></span>|<span data-ttu-id="a2794-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="a2794-128">**Required**</span></span>|<span data-ttu-id="a2794-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="a2794-129">**Description**</span></span>|<span data-ttu-id="a2794-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="a2794-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a2794-131">ID</span><span class="sxs-lookup"><span data-stu-id="a2794-131">ID</span></span>  <br/> |<span data-ttu-id="a2794-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2794-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2794-133">必須</span><span class="sxs-lookup"><span data-stu-id="a2794-133">required</span></span>  <br/> |<span data-ttu-id="a2794-134">図面ページの識別子。</span><span class="sxs-lookup"><span data-stu-id="a2794-134">The identifier of a drawing page.</span></span>  <br/> |<span data-ttu-id="a2794-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="a2794-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

