---
title: VisioDocument_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5003f98e-4fed-73f8-be55-5b068d9cbffe
ms.openlocfilehash: 8c0a5976139aee2f3aee41b3709ce5fd1ac5c00d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538474"
---
# <a name="visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="adc25-102">VisioDocument_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="adc25-102">VisioDocument_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="adc25-103">型情報</span><span class="sxs-lookup"><span data-stu-id="adc25-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="adc25-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="adc25-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="adc25-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="adc25-105">**Schema file**</span></span> <br/> |<span data-ttu-id="adc25-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="adc25-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="adc25-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="adc25-107">**Extension base**</span></span> <br/> |<span data-ttu-id="adc25-108">None</span><span class="sxs-lookup"><span data-stu-id="adc25-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="adc25-109">定義</span><span class="sxs-lookup"><span data-stu-id="adc25-109">Definition</span></span>

```XML
          <xs:complexType name="VisioDocument_Type">
          
          <xs:sequence>
    <xs:element name="DocumentSettings"  type="DocumentSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Colors"  type="Colors_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FaceNames"  type="FaceNames_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="StyleSheets"  type="StyleSheets_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DocumentSheet"  type="DocumentSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="EventList"  type="EventList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderFooter"  type="HeaderFooter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PublishSettings"  type="PublishSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs: name="" >
    </xs:>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="adc25-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="adc25-110">Elements and attributes</span></span>

<span data-ttu-id="adc25-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="adc25-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="adc25-112">子要素</span><span class="sxs-lookup"><span data-stu-id="adc25-112">Child elements</span></span>

|<span data-ttu-id="adc25-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="adc25-113">**Element**</span></span>|<span data-ttu-id="adc25-114">**型**</span><span class="sxs-lookup"><span data-stu-id="adc25-114">**Type**</span></span>|<span data-ttu-id="adc25-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="adc25-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="adc25-116">Colors</span><span class="sxs-lookup"><span data-stu-id="adc25-116">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="adc25-117">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="adc25-117">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="adc25-118">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="adc25-118">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="adc25-119">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="adc25-119">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="adc25-120">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="adc25-120">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="adc25-121">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="adc25-121">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="adc25-122">EventList</span><span class="sxs-lookup"><span data-stu-id="adc25-122">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="adc25-123">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="adc25-123">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="adc25-124">FaceNames 方法</span><span class="sxs-lookup"><span data-stu-id="adc25-124">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="adc25-125">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="adc25-125">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="adc25-126">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="adc25-126">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="adc25-127">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="adc25-127">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="adc25-128">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="adc25-128">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="adc25-129">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="adc25-129">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="adc25-130">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="adc25-130">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="adc25-131">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="adc25-131">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="adc25-132">属性</span><span class="sxs-lookup"><span data-stu-id="adc25-132">Attributes</span></span>

<span data-ttu-id="adc25-133">なし。</span><span class="sxs-lookup"><span data-stu-id="adc25-133">None.</span></span>
  

