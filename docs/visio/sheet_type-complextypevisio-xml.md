---
title: Sheet_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: f171f250fbe37ebf1d0d434709b06ab56804407f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806459"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="12a10-102">Sheet_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="12a10-102">Sheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="12a10-103">型情報</span><span class="sxs-lookup"><span data-stu-id="12a10-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12a10-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="12a10-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="12a10-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="12a10-105">**Schema file**</span></span> <br/> |<span data-ttu-id="12a10-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="12a10-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="12a10-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="12a10-107">**Extension base**</span></span> <br/> |<span data-ttu-id="12a10-108">なし</span><span class="sxs-lookup"><span data-stu-id="12a10-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="12a10-109">定義</span><span class="sxs-lookup"><span data-stu-id="12a10-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="12a10-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="12a10-110">Elements and attributes</span></span>

<span data-ttu-id="12a10-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="12a10-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="12a10-112">子要素</span><span class="sxs-lookup"><span data-stu-id="12a10-112">Child elements</span></span>

|<span data-ttu-id="12a10-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="12a10-113">**Element**</span></span>|<span data-ttu-id="12a10-114">**型**</span><span class="sxs-lookup"><span data-stu-id="12a10-114">**Type**</span></span>|<span data-ttu-id="12a10-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="12a10-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="12a10-116">Cell</span><span class="sxs-lookup"><span data-stu-id="12a10-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="12a10-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="12a10-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="12a10-118">セクション</span><span class="sxs-lookup"><span data-stu-id="12a10-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="12a10-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="12a10-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="12a10-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="12a10-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="12a10-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="12a10-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="12a10-122">属性</span><span class="sxs-lookup"><span data-stu-id="12a10-122">Attributes</span></span>

|<span data-ttu-id="12a10-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="12a10-123">**Attribute**</span></span>|<span data-ttu-id="12a10-124">**型**</span><span class="sxs-lookup"><span data-stu-id="12a10-124">**Type**</span></span>|<span data-ttu-id="12a10-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="12a10-125">**Required**</span></span>|<span data-ttu-id="12a10-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="12a10-126">**Description**</span></span>|<span data-ttu-id="12a10-127">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="12a10-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="12a10-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="12a10-128">FillStyle</span></span>  <br/> |<span data-ttu-id="12a10-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="12a10-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="12a10-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="12a10-130">optional</span></span>  <br/> ||<span data-ttu-id="12a10-131">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="12a10-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="12a10-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="12a10-132">LineStyle</span></span>  <br/> |<span data-ttu-id="12a10-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="12a10-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="12a10-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="12a10-134">optional</span></span>  <br/> ||<span data-ttu-id="12a10-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="12a10-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="12a10-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="12a10-136">TextStyle</span></span>  <br/> |<span data-ttu-id="12a10-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="12a10-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="12a10-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="12a10-138">optional</span></span>  <br/> ||<span data-ttu-id="12a10-139">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="12a10-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

