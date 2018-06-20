---
title: PublishedPage 要素 (PublishSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: 図面ページは、Microsoft SharePoint Server 2013 で Visio Services を使用してブラウザーで表示できるかどうかを指定します。
ms.openlocfilehash: 5cdbb03aaac3393c16c6ed0169842153374f668e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806128"
---
# <a name="publishedpage-element-publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="ecc1f-103">PublishedPage 要素 (PublishSettings_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="ecc1f-103">PublishedPage element (PublishSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ecc1f-104">図面ページは、Microsoft SharePoint Server 2013 で Visio Services を使用してブラウザーで表示できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="ecc1f-104">Specifies whether a drawing page is viewable in the browser using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ecc1f-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="ecc1f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ecc1f-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="ecc1f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ecc1f-107">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="ecc1f-107">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ecc1f-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="ecc1f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ecc1f-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ecc1f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ecc1f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ecc1f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ecc1f-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="ecc1f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ecc1f-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="ecc1f-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ecc1f-113">定義</span><span class="sxs-lookup"><span data-stu-id="ecc1f-113">Definition</span></span>

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ecc1f-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ecc1f-114">Elements and attributes</span></span>

<span data-ttu-id="ecc1f-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ecc1f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ecc1f-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ecc1f-116">Parent elements</span></span>

|<span data-ttu-id="ecc1f-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="ecc1f-117">**Element**</span></span>|<span data-ttu-id="ecc1f-118">**型**</span><span class="sxs-lookup"><span data-stu-id="ecc1f-118">**Type**</span></span>|<span data-ttu-id="ecc1f-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="ecc1f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ecc1f-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="ecc1f-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ecc1f-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ecc1f-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ecc1f-122">Visio Services を使用して、ダイアグラムを開いたときに使用する設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="ecc1f-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ecc1f-123">子要素</span><span class="sxs-lookup"><span data-stu-id="ecc1f-123">Child elements</span></span>

<span data-ttu-id="ecc1f-124">なし。</span><span class="sxs-lookup"><span data-stu-id="ecc1f-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ecc1f-125">属性</span><span class="sxs-lookup"><span data-stu-id="ecc1f-125">Attributes</span></span>

|<span data-ttu-id="ecc1f-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="ecc1f-126">**Attribute**</span></span>|<span data-ttu-id="ecc1f-127">**型**</span><span class="sxs-lookup"><span data-stu-id="ecc1f-127">**Type**</span></span>|<span data-ttu-id="ecc1f-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="ecc1f-128">**Required**</span></span>|<span data-ttu-id="ecc1f-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="ecc1f-129">**Description**</span></span>|<span data-ttu-id="ecc1f-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="ecc1f-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ecc1f-131">ID</span><span class="sxs-lookup"><span data-stu-id="ecc1f-131">ID</span></span>  <br/> |<span data-ttu-id="ecc1f-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ecc1f-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ecc1f-133">必須</span><span class="sxs-lookup"><span data-stu-id="ecc1f-133">required</span></span>  <br/> |<span data-ttu-id="ecc1f-134">図面ページの識別子です。</span><span class="sxs-lookup"><span data-stu-id="ecc1f-134">The identifier of a drawing page.</span></span>  <br/> |<span data-ttu-id="ecc1f-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ecc1f-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

