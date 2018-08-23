---
title: Geometry_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 115a1499-ae55-f85c-676c-e78f478c4703
ms.openlocfilehash: 882540e92f9635d6e99716fd8bbbe369c42a6bec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805476"
---
# <a name="geometrytype-complextype-visio-xml"></a><span data-ttu-id="2e4d7-102">Geometry_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="2e4d7-102">Geometry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2e4d7-103">型情報</span><span class="sxs-lookup"><span data-stu-id="2e4d7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e4d7-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="2e4d7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2e4d7-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="2e4d7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2e4d7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2e4d7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2e4d7-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="2e4d7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2e4d7-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="2e4d7-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2e4d7-109">定義</span><span class="sxs-lookup"><span data-stu-id="2e4d7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2e4d7-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="2e4d7-110">Elements and attributes</span></span>

<span data-ttu-id="2e4d7-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e4d7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2e4d7-112">子要素</span><span class="sxs-lookup"><span data-stu-id="2e4d7-112">Child elements</span></span>

|<span data-ttu-id="2e4d7-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="2e4d7-113">**Element**</span></span>|<span data-ttu-id="2e4d7-114">**型**</span><span class="sxs-lookup"><span data-stu-id="2e4d7-114">**Type**</span></span>|<span data-ttu-id="2e4d7-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="2e4d7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2e4d7-116">Cell</span><span class="sxs-lookup"><span data-stu-id="2e4d7-116">Cell</span></span>](cell-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="2e4d7-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2e4d7-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2e4d7-118">Row</span><span class="sxs-lookup"><span data-stu-id="2e4d7-118">Row</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |<span data-ttu-id="2e4d7-119">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="2e4d7-119">GeometryRow_Type</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2e4d7-120">属性</span><span class="sxs-lookup"><span data-stu-id="2e4d7-120">Attributes</span></span>

<span data-ttu-id="2e4d7-121">なし。</span><span class="sxs-lookup"><span data-stu-id="2e4d7-121">None.</span></span>
  

