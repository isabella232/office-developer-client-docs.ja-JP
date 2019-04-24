---
title: Geometry_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 115a1499-ae55-f85c-676c-e78f478c4703
ms.openlocfilehash: 76627f406e8a829a77658cd486b586d8eebd19b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359669"
---
# <a name="geometrytype-complextype-visio-xml"></a><span data-ttu-id="1209f-102">Geometry_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1209f-102">Geometry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1209f-103">型情報</span><span class="sxs-lookup"><span data-stu-id="1209f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1209f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1209f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1209f-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1209f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1209f-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="1209f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1209f-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="1209f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1209f-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="1209f-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1209f-109">定義</span><span class="sxs-lookup"><span data-stu-id="1209f-109">Definition</span></span>

```XML
          <xs:complexType name="Geometry_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Row"  type="GeometryRow_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:choice>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1209f-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1209f-110">Elements and attributes</span></span>

<span data-ttu-id="1209f-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1209f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1209f-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1209f-112">Child elements</span></span>

|<span data-ttu-id="1209f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1209f-113">**Element**</span></span>|<span data-ttu-id="1209f-114">**型**</span><span class="sxs-lookup"><span data-stu-id="1209f-114">**Type**</span></span>|<span data-ttu-id="1209f-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="1209f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1209f-116">Cell</span><span class="sxs-lookup"><span data-stu-id="1209f-116">Cell</span></span>](cell-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1209f-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1209f-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1209f-118">行</span><span class="sxs-lookup"><span data-stu-id="1209f-118">Row</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |<span data-ttu-id="1209f-119">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="1209f-119">GeometryRow_Type</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1209f-120">属性</span><span class="sxs-lookup"><span data-stu-id="1209f-120">Attributes</span></span>

<span data-ttu-id="1209f-121">なし。</span><span class="sxs-lookup"><span data-stu-id="1209f-121">None.</span></span>
  

