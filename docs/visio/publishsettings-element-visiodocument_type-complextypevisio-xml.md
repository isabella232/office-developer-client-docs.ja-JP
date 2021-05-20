---
title: PublishSettings 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: 2013 年 2013 年に Visio サービスを使用してダイアグラムを開Microsoft SharePoint Serverします。
ms.openlocfilehash: 611dfe477228995bca6aedff27b468a2d57e7e85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541359"
---
# <a name="publishsettings-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="5d638-103">PublishSettings 要素 (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5d638-103">PublishSettings element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="5d638-104">2013 年 2013 年に Visio サービスを使用してダイアグラムを開Microsoft SharePoint Serverします。</span><span class="sxs-lookup"><span data-stu-id="5d638-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d638-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="5d638-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d638-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="5d638-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5d638-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="5d638-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5d638-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5d638-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5d638-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5d638-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5d638-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5d638-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5d638-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="5d638-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5d638-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="5d638-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5d638-113">定義</span><span class="sxs-lookup"><span data-stu-id="5d638-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5d638-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5d638-114">Elements and attributes</span></span>

<span data-ttu-id="5d638-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d638-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5d638-116">親要素</span><span class="sxs-lookup"><span data-stu-id="5d638-116">Parent elements</span></span>

|<span data-ttu-id="5d638-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="5d638-117">**Element**</span></span>|<span data-ttu-id="5d638-118">**型**</span><span class="sxs-lookup"><span data-stu-id="5d638-118">**Type**</span></span>|<span data-ttu-id="5d638-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="5d638-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5d638-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="5d638-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="5d638-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="5d638-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5d638-122">図面のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d638-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5d638-123">子要素</span><span class="sxs-lookup"><span data-stu-id="5d638-123">Child elements</span></span>

|<span data-ttu-id="5d638-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="5d638-124">**Element**</span></span>|<span data-ttu-id="5d638-125">**型**</span><span class="sxs-lookup"><span data-stu-id="5d638-125">**Type**</span></span>|<span data-ttu-id="5d638-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="5d638-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5d638-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="5d638-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5d638-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="5d638-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5d638-129">[サービス] を使用して、ブラウザーで図面ページを表示Visioします。</span><span class="sxs-lookup"><span data-stu-id="5d638-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="5d638-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="5d638-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5d638-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="5d638-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5d638-132">レコードセットがサービスサービスを使用して更新Visioします。</span><span class="sxs-lookup"><span data-stu-id="5d638-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5d638-133">属性</span><span class="sxs-lookup"><span data-stu-id="5d638-133">Attributes</span></span>

<span data-ttu-id="5d638-134">なし。</span><span class="sxs-lookup"><span data-stu-id="5d638-134">None.</span></span>
  

