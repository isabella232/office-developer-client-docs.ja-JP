---
title: HeaderFooter_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5fcf3d9-c11a-ed5e-0bf5-e706259ef30b
ms.openlocfilehash: 581101909096d4ee8a4f44c8e9e95dab0313ed7c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342239"
---
# <a name="headerfootertype-complextype-visio-xml"></a><span data-ttu-id="9c961-102">HeaderFooter_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9c961-102">HeaderFooter_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9c961-103">型情報</span><span class="sxs-lookup"><span data-stu-id="9c961-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c961-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9c961-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9c961-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9c961-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9c961-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="9c961-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9c961-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="9c961-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9c961-108">なし</span><span class="sxs-lookup"><span data-stu-id="9c961-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9c961-109">定義</span><span class="sxs-lookup"><span data-stu-id="9c961-109">Definition</span></span>

```XML
          <xs:complexType name="HeaderFooter_Type">
          
          <xs:all>
    <xs:element name="HeaderMargin"  type="HeaderMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterMargin"  type="FooterMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderLeft"  type="HeaderLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderCenter"  type="HeaderCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderRight"  type="HeaderRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterLeft"  type="FooterLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterCenter"  type="FooterCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterRight"  type="FooterRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderFooterFont"  type="HeaderFooterFont_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="HeaderFooterColor"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9c961-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9c961-110">Elements and attributes</span></span>

<span data-ttu-id="9c961-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c961-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9c961-112">子要素</span><span class="sxs-lookup"><span data-stu-id="9c961-112">Child elements</span></span>

|<span data-ttu-id="9c961-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9c961-113">**Element**</span></span>|<span data-ttu-id="9c961-114">**型**</span><span class="sxs-lookup"><span data-stu-id="9c961-114">**Type**</span></span>|<span data-ttu-id="9c961-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="9c961-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9c961-116">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="9c961-116">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c961-117">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="9c961-117">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9c961-118">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="9c961-118">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c961-119">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="9c961-119">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9c961-120">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="9c961-120">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c961-121">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="9c961-121">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9c961-122">FooterRight</span><span class="sxs-lookup"><span data-stu-id="9c961-122">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c961-123">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="9c961-123">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9c961-124">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="9c961-124">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c961-125">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="9c961-125">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9c961-126">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="9c961-126">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c961-127">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="9c961-127">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9c961-128">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="9c961-128">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c961-129">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="9c961-129">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9c961-130">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="9c961-130">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c961-131">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="9c961-131">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9c961-132">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="9c961-132">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c961-133">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="9c961-133">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9c961-134">属性</span><span class="sxs-lookup"><span data-stu-id="9c961-134">Attributes</span></span>

|<span data-ttu-id="9c961-135">**属性**</span><span class="sxs-lookup"><span data-stu-id="9c961-135">**Attribute**</span></span>|<span data-ttu-id="9c961-136">**型**</span><span class="sxs-lookup"><span data-stu-id="9c961-136">**Type**</span></span>|<span data-ttu-id="9c961-137">**必須**</span><span class="sxs-lookup"><span data-stu-id="9c961-137">**Required**</span></span>|<span data-ttu-id="9c961-138">**説明**</span><span class="sxs-lookup"><span data-stu-id="9c961-138">**Description**</span></span>|<span data-ttu-id="9c961-139">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="9c961-139">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9c961-140">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="9c961-140">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="9c961-141">xsd: string</span><span class="sxs-lookup"><span data-stu-id="9c961-141">xsd:string</span></span>  <br/> |<span data-ttu-id="9c961-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="9c961-142">optional</span></span>  <br/> ||<span data-ttu-id="9c961-143">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="9c961-143">Values of the xsd:string type.</span></span>  <br/> |
   

