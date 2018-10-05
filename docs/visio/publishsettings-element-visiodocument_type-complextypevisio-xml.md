---
title: PublishSettings 要素 (VisioDocument_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Visio Services を使用して Microsoft SharePoint Server 2013 で、ダイアグラムを開いたときに使用する設定を指定します。
ms.openlocfilehash: 7e926021180d0f32c5e8754fd856081908f4925d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397213"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="26607-103">PublishSettings 要素 (VisioDocument_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="26607-103">PublishSettings element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="26607-104">Visio Services を使用して Microsoft SharePoint Server 2013 で、ダイアグラムを開いたときに使用する設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="26607-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26607-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="26607-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26607-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="26607-106">**Element type**</span></span> <br/> |[<span data-ttu-id="26607-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="26607-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="26607-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="26607-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="26607-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="26607-109">**Schema file**</span></span> <br/> |<span data-ttu-id="26607-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="26607-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="26607-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="26607-111">**Document parts**</span></span> <br/> |<span data-ttu-id="26607-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="26607-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="26607-113">定義</span><span class="sxs-lookup"><span data-stu-id="26607-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="26607-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="26607-114">Elements and attributes</span></span>

<span data-ttu-id="26607-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="26607-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="26607-116">親要素</span><span class="sxs-lookup"><span data-stu-id="26607-116">Parent elements</span></span>

|<span data-ttu-id="26607-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="26607-117">**Element**</span></span>|<span data-ttu-id="26607-118">**型**</span><span class="sxs-lookup"><span data-stu-id="26607-118">**Type**</span></span>|<span data-ttu-id="26607-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="26607-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="26607-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="26607-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="26607-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="26607-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26607-122">図面のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="26607-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="26607-123">子要素</span><span class="sxs-lookup"><span data-stu-id="26607-123">Child elements</span></span>

|<span data-ttu-id="26607-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="26607-124">**Element**</span></span>|<span data-ttu-id="26607-125">**型**</span><span class="sxs-lookup"><span data-stu-id="26607-125">**Type**</span></span>|<span data-ttu-id="26607-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="26607-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="26607-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="26607-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26607-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="26607-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26607-129">図面ページは、Visio Services を使用してブラウザーで表示できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="26607-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="26607-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="26607-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26607-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="26607-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26607-132">レコード セットは、Visio Services を使用してデータを更新するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="26607-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="26607-133">属性</span><span class="sxs-lookup"><span data-stu-id="26607-133">Attributes</span></span>

<span data-ttu-id="26607-134">なし。</span><span class="sxs-lookup"><span data-stu-id="26607-134">None.</span></span>
  

