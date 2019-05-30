---
title: Sheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: b747f2257f2b09083b72a17a59856be0a985b270
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540407"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="386c1-102">Sheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="386c1-102">Sheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="386c1-103">型情報</span><span class="sxs-lookup"><span data-stu-id="386c1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="386c1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="386c1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="386c1-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="386c1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="386c1-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="386c1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="386c1-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="386c1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="386c1-108">None</span><span class="sxs-lookup"><span data-stu-id="386c1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="386c1-109">定義</span><span class="sxs-lookup"><span data-stu-id="386c1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="386c1-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="386c1-110">Elements and attributes</span></span>

<span data-ttu-id="386c1-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="386c1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="386c1-112">子要素</span><span class="sxs-lookup"><span data-stu-id="386c1-112">Child elements</span></span>

|<span data-ttu-id="386c1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="386c1-113">**Element**</span></span>|<span data-ttu-id="386c1-114">**型**</span><span class="sxs-lookup"><span data-stu-id="386c1-114">**Type**</span></span>|<span data-ttu-id="386c1-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="386c1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="386c1-116">Cell</span><span class="sxs-lookup"><span data-stu-id="386c1-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="386c1-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="386c1-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="386c1-118">Section</span><span class="sxs-lookup"><span data-stu-id="386c1-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="386c1-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="386c1-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="386c1-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="386c1-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="386c1-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="386c1-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="386c1-122">属性</span><span class="sxs-lookup"><span data-stu-id="386c1-122">Attributes</span></span>

|<span data-ttu-id="386c1-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="386c1-123">**Attribute**</span></span>|<span data-ttu-id="386c1-124">**型**</span><span class="sxs-lookup"><span data-stu-id="386c1-124">**Type**</span></span>|<span data-ttu-id="386c1-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="386c1-125">**Required**</span></span>|<span data-ttu-id="386c1-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="386c1-126">**Description**</span></span>|<span data-ttu-id="386c1-127">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="386c1-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="386c1-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="386c1-128">FillStyle</span></span>  <br/> |<span data-ttu-id="386c1-129">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="386c1-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="386c1-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="386c1-130">optional</span></span>  <br/> ||<span data-ttu-id="386c1-131">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="386c1-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="386c1-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="386c1-132">LineStyle</span></span>  <br/> |<span data-ttu-id="386c1-133">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="386c1-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="386c1-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="386c1-134">optional</span></span>  <br/> ||<span data-ttu-id="386c1-135">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="386c1-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="386c1-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="386c1-136">TextStyle</span></span>  <br/> |<span data-ttu-id="386c1-137">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="386c1-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="386c1-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="386c1-138">optional</span></span>  <br/> ||<span data-ttu-id="386c1-139">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="386c1-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

