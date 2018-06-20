---
title: SectionDef_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 426e62ea7a9f990555776e3ac732dd43e614582d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806362"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="77848-102">SectionDef_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="77848-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="77848-103">型情報</span><span class="sxs-lookup"><span data-stu-id="77848-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77848-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="77848-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="77848-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="77848-105">**Schema file**</span></span> <br/> |<span data-ttu-id="77848-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="77848-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="77848-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="77848-107">**Extension base**</span></span> <br/> |<span data-ttu-id="77848-108">なし</span><span class="sxs-lookup"><span data-stu-id="77848-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="77848-109">定義</span><span class="sxs-lookup"><span data-stu-id="77848-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="77848-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="77848-110">Elements and attributes</span></span>

<span data-ttu-id="77848-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="77848-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="77848-112">子要素</span><span class="sxs-lookup"><span data-stu-id="77848-112">Child elements</span></span>

|<span data-ttu-id="77848-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="77848-113">**Element**</span></span>|<span data-ttu-id="77848-114">**型**</span><span class="sxs-lookup"><span data-stu-id="77848-114">**Type**</span></span>|<span data-ttu-id="77848-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="77848-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="77848-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="77848-116">CellDef</span></span>](http://msdn.microsoft.com/library/f0ec7afe-9e0a-b5e5-82dd-4adff1c1607f%28Office.15%29.aspx) <br/> |[<span data-ttu-id="77848-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="77848-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="77848-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="77848-118">RowDef</span></span>](http://msdn.microsoft.com/library/25615be9-1d19-1ba9-4192-7d4a0dfae717%28Office.15%29.aspx) <br/> |[<span data-ttu-id="77848-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="77848-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="77848-120">属性</span><span class="sxs-lookup"><span data-stu-id="77848-120">Attributes</span></span>

|<span data-ttu-id="77848-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="77848-121">**Attribute**</span></span>|<span data-ttu-id="77848-122">**型**</span><span class="sxs-lookup"><span data-stu-id="77848-122">**Type**</span></span>|<span data-ttu-id="77848-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="77848-123">**Required**</span></span>|<span data-ttu-id="77848-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="77848-124">**Description**</span></span>|<span data-ttu-id="77848-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="77848-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="77848-126">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="77848-126">N</span></span>  <br/> |<span data-ttu-id="77848-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="77848-127">xsd:string</span></span>  <br/> |<span data-ttu-id="77848-128">必須</span><span class="sxs-lookup"><span data-stu-id="77848-128">required</span></span>  <br/> ||<span data-ttu-id="77848-129">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="77848-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="77848-130">S</span><span class="sxs-lookup"><span data-stu-id="77848-130">S</span></span>  <br/> |<span data-ttu-id="77848-131">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="77848-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="77848-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="77848-132">optional</span></span>  <br/> ||<span data-ttu-id="77848-133">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="77848-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="77848-134">SV 要素</span><span class="sxs-lookup"><span data-stu-id="77848-134">T</span></span>  <br/> |<span data-ttu-id="77848-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="77848-135">xsd:string</span></span>  <br/> |<span data-ttu-id="77848-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="77848-136">optional</span></span>  <br/> ||<span data-ttu-id="77848-137">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="77848-137">Values of the xsd:string type.</span></span>  <br/> |
   

