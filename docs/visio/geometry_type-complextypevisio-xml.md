---
title: Geometry_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 115a1499-ae55-f85c-676c-e78f478c4703
ms.openlocfilehash: 1b16a32462f997ab80b0b6ef64df8eb202740c47
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542290"
---
# <a name="geometry_type-complextype-visio-xml"></a><span data-ttu-id="23ba7-102">Geometry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="23ba7-102">Geometry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="23ba7-103">型情報</span><span class="sxs-lookup"><span data-stu-id="23ba7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23ba7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="23ba7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="23ba7-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="23ba7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="23ba7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="23ba7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="23ba7-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="23ba7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="23ba7-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="23ba7-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="23ba7-109">定義</span><span class="sxs-lookup"><span data-stu-id="23ba7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="23ba7-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="23ba7-110">Elements and attributes</span></span>

<span data-ttu-id="23ba7-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="23ba7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="23ba7-112">子要素</span><span class="sxs-lookup"><span data-stu-id="23ba7-112">Child elements</span></span>

|<span data-ttu-id="23ba7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="23ba7-113">**Element**</span></span>|<span data-ttu-id="23ba7-114">**型**</span><span class="sxs-lookup"><span data-stu-id="23ba7-114">**Type**</span></span>|<span data-ttu-id="23ba7-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="23ba7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="23ba7-116">Cell</span><span class="sxs-lookup"><span data-stu-id="23ba7-116">Cell</span></span>](cell-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="23ba7-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="23ba7-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23ba7-118">行</span><span class="sxs-lookup"><span data-stu-id="23ba7-118">Row</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |<span data-ttu-id="23ba7-119">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="23ba7-119">GeometryRow_Type</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="23ba7-120">属性</span><span class="sxs-lookup"><span data-stu-id="23ba7-120">Attributes</span></span>

<span data-ttu-id="23ba7-121">なし。</span><span class="sxs-lookup"><span data-stu-id="23ba7-121">None.</span></span>
  

