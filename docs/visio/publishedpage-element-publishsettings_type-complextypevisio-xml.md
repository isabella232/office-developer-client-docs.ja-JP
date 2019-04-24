---
title: publishedpage 要素 (PublishSettings_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Microsoft SharePoint Server 2013 の Visio Services を使用して、図面ページがブラウザーで表示可能かどうかを指定します。
ms.openlocfilehash: 313cabbdd59930df67c807ee3c89df1a6e8c17a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326797"
---
# <a name="publishedpage-element-publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="e0b4a-103">publishedpage 要素 (PublishSettings_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="e0b4a-103">PublishedPage element (PublishSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e0b4a-104">Microsoft SharePoint Server 2013 の Visio Services を使用して、図面ページがブラウザーで表示可能かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e0b4a-104">Specifies whether a drawing page is viewable in the browser using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0b4a-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="e0b4a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0b4a-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="e0b4a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e0b4a-107">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="e0b4a-107">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e0b4a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e0b4a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e0b4a-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e0b4a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e0b4a-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="e0b4a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e0b4a-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="e0b4a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e0b4a-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="e0b4a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e0b4a-113">定義</span><span class="sxs-lookup"><span data-stu-id="e0b4a-113">Definition</span></span>

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e0b4a-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e0b4a-114">Elements and attributes</span></span>

<span data-ttu-id="e0b4a-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0b4a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e0b4a-116">親要素</span><span class="sxs-lookup"><span data-stu-id="e0b4a-116">Parent elements</span></span>

|<span data-ttu-id="e0b4a-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="e0b4a-117">**Element**</span></span>|<span data-ttu-id="e0b4a-118">**型**</span><span class="sxs-lookup"><span data-stu-id="e0b4a-118">**Type**</span></span>|<span data-ttu-id="e0b4a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="e0b4a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e0b4a-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="e0b4a-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0b4a-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="e0b4a-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e0b4a-122">Visio Services を使用して図面を開くときに使用する設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="e0b4a-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e0b4a-123">子要素</span><span class="sxs-lookup"><span data-stu-id="e0b4a-123">Child elements</span></span>

<span data-ttu-id="e0b4a-124">なし。</span><span class="sxs-lookup"><span data-stu-id="e0b4a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0b4a-125">属性</span><span class="sxs-lookup"><span data-stu-id="e0b4a-125">Attributes</span></span>

|<span data-ttu-id="e0b4a-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="e0b4a-126">**Attribute**</span></span>|<span data-ttu-id="e0b4a-127">**型**</span><span class="sxs-lookup"><span data-stu-id="e0b4a-127">**Type**</span></span>|<span data-ttu-id="e0b4a-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="e0b4a-128">**Required**</span></span>|<span data-ttu-id="e0b4a-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="e0b4a-129">**Description**</span></span>|<span data-ttu-id="e0b4a-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="e0b4a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e0b4a-131">ID</span><span class="sxs-lookup"><span data-stu-id="e0b4a-131">ID</span></span>  <br/> |<span data-ttu-id="e0b4a-132">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="e0b4a-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0b4a-133">必須</span><span class="sxs-lookup"><span data-stu-id="e0b4a-133">required</span></span>  <br/> |<span data-ttu-id="e0b4a-134">図面ページの識別子。</span><span class="sxs-lookup"><span data-stu-id="e0b4a-134">The identifier of a drawing page.</span></span>  <br/> |<span data-ttu-id="e0b4a-135">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0b4a-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

