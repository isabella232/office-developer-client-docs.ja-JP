---
title: SectionDef_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: cd85dd97a8de7bc9a9ca34fd19669dd294fe6905
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589757"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="8ad3f-102">SectionDef_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="8ad3f-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="8ad3f-103">型情報</span><span class="sxs-lookup"><span data-stu-id="8ad3f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ad3f-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="8ad3f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8ad3f-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8ad3f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8ad3f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8ad3f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8ad3f-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="8ad3f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8ad3f-108">なし</span><span class="sxs-lookup"><span data-stu-id="8ad3f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8ad3f-109">定義</span><span class="sxs-lookup"><span data-stu-id="8ad3f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8ad3f-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8ad3f-110">Elements and attributes</span></span>

<span data-ttu-id="8ad3f-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ad3f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8ad3f-112">子要素</span><span class="sxs-lookup"><span data-stu-id="8ad3f-112">Child elements</span></span>

|<span data-ttu-id="8ad3f-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="8ad3f-113">**Element**</span></span>|<span data-ttu-id="8ad3f-114">**型**</span><span class="sxs-lookup"><span data-stu-id="8ad3f-114">**Type**</span></span>|<span data-ttu-id="8ad3f-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="8ad3f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8ad3f-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="8ad3f-116">CellDef</span></span> <br/> |[<span data-ttu-id="8ad3f-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="8ad3f-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="8ad3f-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="8ad3f-118">RowDef</span></span> <br/> |[<span data-ttu-id="8ad3f-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="8ad3f-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8ad3f-120">属性</span><span class="sxs-lookup"><span data-stu-id="8ad3f-120">Attributes</span></span>

|<span data-ttu-id="8ad3f-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="8ad3f-121">**Attribute**</span></span>|<span data-ttu-id="8ad3f-122">**型**</span><span class="sxs-lookup"><span data-stu-id="8ad3f-122">**Type**</span></span>|<span data-ttu-id="8ad3f-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="8ad3f-123">**Required**</span></span>|<span data-ttu-id="8ad3f-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="8ad3f-124">**Description**</span></span>|<span data-ttu-id="8ad3f-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="8ad3f-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8ad3f-126">N</span><span class="sxs-lookup"><span data-stu-id="8ad3f-126">N</span></span>  <br/> |<span data-ttu-id="8ad3f-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8ad3f-127">xsd:string</span></span>  <br/> |<span data-ttu-id="8ad3f-128">必須</span><span class="sxs-lookup"><span data-stu-id="8ad3f-128">required</span></span>  <br/> ||<span data-ttu-id="8ad3f-129">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ad3f-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8ad3f-130">S</span><span class="sxs-lookup"><span data-stu-id="8ad3f-130">S</span></span>  <br/> |<span data-ttu-id="8ad3f-131">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="8ad3f-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8ad3f-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="8ad3f-132">optional</span></span>  <br/> ||<span data-ttu-id="8ad3f-133">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ad3f-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8ad3f-134">SV 要素</span><span class="sxs-lookup"><span data-stu-id="8ad3f-134">T</span></span>  <br/> |<span data-ttu-id="8ad3f-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8ad3f-135">xsd:string</span></span>  <br/> |<span data-ttu-id="8ad3f-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="8ad3f-136">optional</span></span>  <br/> ||<span data-ttu-id="8ad3f-137">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ad3f-137">Values of the xsd:string type.</span></span>  <br/> |
   

