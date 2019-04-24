---
title: Sheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: dc8930ffa89baf059074a12bb285e6b53e329e41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342869"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="fcf9a-102">Sheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="fcf9a-102">Sheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fcf9a-103">型情報</span><span class="sxs-lookup"><span data-stu-id="fcf9a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fcf9a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fcf9a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fcf9a-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="fcf9a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fcf9a-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="fcf9a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fcf9a-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="fcf9a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fcf9a-108">なし</span><span class="sxs-lookup"><span data-stu-id="fcf9a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fcf9a-109">定義</span><span class="sxs-lookup"><span data-stu-id="fcf9a-109">Definition</span></span>

```XML
        <xs:complexType name="Sheet_Type" abstract="true">
        
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Section"  type="Section_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs: name="" >
    </xs:>
    
      </xs:sequence>
    <xs:attribute name="LineStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="FillStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TextStyle"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fcf9a-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="fcf9a-110">Elements and attributes</span></span>

<span data-ttu-id="fcf9a-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fcf9a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fcf9a-112">子要素</span><span class="sxs-lookup"><span data-stu-id="fcf9a-112">Child elements</span></span>

|<span data-ttu-id="fcf9a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fcf9a-113">**Element**</span></span>|<span data-ttu-id="fcf9a-114">**型**</span><span class="sxs-lookup"><span data-stu-id="fcf9a-114">**Type**</span></span>|<span data-ttu-id="fcf9a-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="fcf9a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fcf9a-116">Cell</span><span class="sxs-lookup"><span data-stu-id="fcf9a-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="fcf9a-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="fcf9a-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="fcf9a-118">Section</span><span class="sxs-lookup"><span data-stu-id="fcf9a-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fcf9a-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="fcf9a-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="fcf9a-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="fcf9a-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="fcf9a-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="fcf9a-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fcf9a-122">属性</span><span class="sxs-lookup"><span data-stu-id="fcf9a-122">Attributes</span></span>

|<span data-ttu-id="fcf9a-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="fcf9a-123">**Attribute**</span></span>|<span data-ttu-id="fcf9a-124">**型**</span><span class="sxs-lookup"><span data-stu-id="fcf9a-124">**Type**</span></span>|<span data-ttu-id="fcf9a-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="fcf9a-125">**Required**</span></span>|<span data-ttu-id="fcf9a-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="fcf9a-126">**Description**</span></span>|<span data-ttu-id="fcf9a-127">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="fcf9a-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fcf9a-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="fcf9a-128">FillStyle</span></span>  <br/> |<span data-ttu-id="fcf9a-129">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="fcf9a-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fcf9a-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="fcf9a-130">optional</span></span>  <br/> ||<span data-ttu-id="fcf9a-131">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="fcf9a-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fcf9a-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="fcf9a-132">LineStyle</span></span>  <br/> |<span data-ttu-id="fcf9a-133">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="fcf9a-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fcf9a-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="fcf9a-134">optional</span></span>  <br/> ||<span data-ttu-id="fcf9a-135">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="fcf9a-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fcf9a-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="fcf9a-136">TextStyle</span></span>  <br/> |<span data-ttu-id="fcf9a-137">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="fcf9a-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fcf9a-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="fcf9a-138">optional</span></span>  <br/> ||<span data-ttu-id="fcf9a-139">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="fcf9a-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

