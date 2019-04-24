---
title: SectionDef_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 1d13cf54861435aea2ce0b3aade955575d538891
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326076"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="bddd9-102">SectionDef_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="bddd9-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bddd9-103">型情報</span><span class="sxs-lookup"><span data-stu-id="bddd9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bddd9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bddd9-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bddd9-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="bddd9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bddd9-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="bddd9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bddd9-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="bddd9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bddd9-108">なし</span><span class="sxs-lookup"><span data-stu-id="bddd9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bddd9-109">定義</span><span class="sxs-lookup"><span data-stu-id="bddd9-109">Definition</span></span>

```XML
          <xs:complexType name="SectionDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowDef"  type="RowDef_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bddd9-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="bddd9-110">Elements and attributes</span></span>

<span data-ttu-id="bddd9-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bddd9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bddd9-112">子要素</span><span class="sxs-lookup"><span data-stu-id="bddd9-112">Child elements</span></span>

|<span data-ttu-id="bddd9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bddd9-113">**Element**</span></span>|<span data-ttu-id="bddd9-114">**型**</span><span class="sxs-lookup"><span data-stu-id="bddd9-114">**Type**</span></span>|<span data-ttu-id="bddd9-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="bddd9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bddd9-116">celldef</span><span class="sxs-lookup"><span data-stu-id="bddd9-116">CellDef</span></span> <br/> |[<span data-ttu-id="bddd9-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="bddd9-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="bddd9-118">rowdef</span><span class="sxs-lookup"><span data-stu-id="bddd9-118">RowDef</span></span> <br/> |[<span data-ttu-id="bddd9-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="bddd9-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bddd9-120">属性</span><span class="sxs-lookup"><span data-stu-id="bddd9-120">Attributes</span></span>

|<span data-ttu-id="bddd9-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="bddd9-121">**Attribute**</span></span>|<span data-ttu-id="bddd9-122">**型**</span><span class="sxs-lookup"><span data-stu-id="bddd9-122">**Type**</span></span>|<span data-ttu-id="bddd9-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="bddd9-123">**Required**</span></span>|<span data-ttu-id="bddd9-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="bddd9-124">**Description**</span></span>|<span data-ttu-id="bddd9-125">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="bddd9-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bddd9-126">N</span><span class="sxs-lookup"><span data-stu-id="bddd9-126">N</span></span>  <br/> |<span data-ttu-id="bddd9-127">xsd: string</span><span class="sxs-lookup"><span data-stu-id="bddd9-127">xsd:string</span></span>  <br/> |<span data-ttu-id="bddd9-128">必須</span><span class="sxs-lookup"><span data-stu-id="bddd9-128">required</span></span>  <br/> ||<span data-ttu-id="bddd9-129">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="bddd9-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bddd9-130">S</span><span class="sxs-lookup"><span data-stu-id="bddd9-130">S</span></span>  <br/> |<span data-ttu-id="bddd9-131">xsd: アン signedbyte</span><span class="sxs-lookup"><span data-stu-id="bddd9-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="bddd9-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="bddd9-132">optional</span></span>  <br/> ||<span data-ttu-id="bddd9-133">xsd:/signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="bddd9-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="bddd9-134">T</span><span class="sxs-lookup"><span data-stu-id="bddd9-134">T</span></span>  <br/> |<span data-ttu-id="bddd9-135">xsd: string</span><span class="sxs-lookup"><span data-stu-id="bddd9-135">xsd:string</span></span>  <br/> |<span data-ttu-id="bddd9-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="bddd9-136">optional</span></span>  <br/> ||<span data-ttu-id="bddd9-137">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="bddd9-137">Values of the xsd:string type.</span></span>  <br/> |
   

