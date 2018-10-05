---
title: HeaderFooter_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5fcf3d9-c11a-ed5e-0bf5-e706259ef30b
ms.openlocfilehash: 581101909096d4ee8a4f44c8e9e95dab0313ed7c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384508"
---
# <a name="headerfootertype-complextype-visio-xml"></a><span data-ttu-id="4a7c6-102">HeaderFooter_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="4a7c6-102">HeaderFooter_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4a7c6-103">型情報</span><span class="sxs-lookup"><span data-stu-id="4a7c6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a7c6-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="4a7c6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4a7c6-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4a7c6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4a7c6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4a7c6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4a7c6-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="4a7c6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4a7c6-108">なし</span><span class="sxs-lookup"><span data-stu-id="4a7c6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4a7c6-109">定義</span><span class="sxs-lookup"><span data-stu-id="4a7c6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4a7c6-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4a7c6-110">Elements and attributes</span></span>

<span data-ttu-id="4a7c6-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a7c6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4a7c6-112">子要素</span><span class="sxs-lookup"><span data-stu-id="4a7c6-112">Child elements</span></span>

|<span data-ttu-id="4a7c6-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="4a7c6-113">**Element**</span></span>|<span data-ttu-id="4a7c6-114">**型**</span><span class="sxs-lookup"><span data-stu-id="4a7c6-114">**Type**</span></span>|<span data-ttu-id="4a7c6-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="4a7c6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4a7c6-116">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="4a7c6-116">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a7c6-117">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="4a7c6-117">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4a7c6-118">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="4a7c6-118">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a7c6-119">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="4a7c6-119">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4a7c6-120">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="4a7c6-120">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a7c6-121">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="4a7c6-121">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4a7c6-122">FooterRight</span><span class="sxs-lookup"><span data-stu-id="4a7c6-122">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a7c6-123">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="4a7c6-123">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4a7c6-124">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="4a7c6-124">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a7c6-125">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="4a7c6-125">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4a7c6-126">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="4a7c6-126">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a7c6-127">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="4a7c6-127">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4a7c6-128">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="4a7c6-128">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a7c6-129">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="4a7c6-129">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4a7c6-130">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="4a7c6-130">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a7c6-131">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="4a7c6-131">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4a7c6-132">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="4a7c6-132">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a7c6-133">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="4a7c6-133">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4a7c6-134">属性</span><span class="sxs-lookup"><span data-stu-id="4a7c6-134">Attributes</span></span>

|<span data-ttu-id="4a7c6-135">**属性**</span><span class="sxs-lookup"><span data-stu-id="4a7c6-135">**Attribute**</span></span>|<span data-ttu-id="4a7c6-136">**型**</span><span class="sxs-lookup"><span data-stu-id="4a7c6-136">**Type**</span></span>|<span data-ttu-id="4a7c6-137">**必須**</span><span class="sxs-lookup"><span data-stu-id="4a7c6-137">**Required**</span></span>|<span data-ttu-id="4a7c6-138">**説明**</span><span class="sxs-lookup"><span data-stu-id="4a7c6-138">**Description**</span></span>|<span data-ttu-id="4a7c6-139">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="4a7c6-139">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4a7c6-140">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="4a7c6-140">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="4a7c6-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4a7c6-141">xsd:string</span></span>  <br/> |<span data-ttu-id="4a7c6-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="4a7c6-142">optional</span></span>  <br/> ||<span data-ttu-id="4a7c6-143">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a7c6-143">Values of the xsd:string type.</span></span>  <br/> |
   

