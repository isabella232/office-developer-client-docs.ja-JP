---
title: SectionDef_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 1d13cf54861435aea2ce0b3aade955575d538891
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395078"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="a95c4-102">SectionDef_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a95c4-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a95c4-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a95c4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a95c4-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a95c4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a95c4-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a95c4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a95c4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a95c4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a95c4-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a95c4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a95c4-108">なし</span><span class="sxs-lookup"><span data-stu-id="a95c4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a95c4-109">定義</span><span class="sxs-lookup"><span data-stu-id="a95c4-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a95c4-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a95c4-110">Elements and attributes</span></span>

<span data-ttu-id="a95c4-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a95c4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a95c4-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a95c4-112">Child elements</span></span>

|<span data-ttu-id="a95c4-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="a95c4-113">**Element**</span></span>|<span data-ttu-id="a95c4-114">**型**</span><span class="sxs-lookup"><span data-stu-id="a95c4-114">**Type**</span></span>|<span data-ttu-id="a95c4-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="a95c4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a95c4-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="a95c4-116">CellDef</span></span> <br/> |[<span data-ttu-id="a95c4-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="a95c4-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="a95c4-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="a95c4-118">RowDef</span></span> <br/> |[<span data-ttu-id="a95c4-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="a95c4-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a95c4-120">属性</span><span class="sxs-lookup"><span data-stu-id="a95c4-120">Attributes</span></span>

|<span data-ttu-id="a95c4-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="a95c4-121">**Attribute**</span></span>|<span data-ttu-id="a95c4-122">**型**</span><span class="sxs-lookup"><span data-stu-id="a95c4-122">**Type**</span></span>|<span data-ttu-id="a95c4-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="a95c4-123">**Required**</span></span>|<span data-ttu-id="a95c4-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="a95c4-124">**Description**</span></span>|<span data-ttu-id="a95c4-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="a95c4-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a95c4-126">N</span><span class="sxs-lookup"><span data-stu-id="a95c4-126">N</span></span>  <br/> |<span data-ttu-id="a95c4-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a95c4-127">xsd:string</span></span>  <br/> |<span data-ttu-id="a95c4-128">必須</span><span class="sxs-lookup"><span data-stu-id="a95c4-128">required</span></span>  <br/> ||<span data-ttu-id="a95c4-129">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a95c4-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a95c4-130">S</span><span class="sxs-lookup"><span data-stu-id="a95c4-130">S</span></span>  <br/> |<span data-ttu-id="a95c4-131">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="a95c4-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="a95c4-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="a95c4-132">optional</span></span>  <br/> ||<span data-ttu-id="a95c4-133">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a95c4-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="a95c4-134">SV 要素</span><span class="sxs-lookup"><span data-stu-id="a95c4-134">T</span></span>  <br/> |<span data-ttu-id="a95c4-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a95c4-135">xsd:string</span></span>  <br/> |<span data-ttu-id="a95c4-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="a95c4-136">optional</span></span>  <br/> ||<span data-ttu-id="a95c4-137">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a95c4-137">Values of the xsd:string type.</span></span>  <br/> |
   

