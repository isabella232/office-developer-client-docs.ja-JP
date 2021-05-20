---
title: SplineKnot_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 114d5460-c5fd-0e31-def4-f943b93bd1ae
ms.openlocfilehash: 6f5bd2c07f4eba0ee2dc2eff26245db2cf221075
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538908"
---
# <a name="splineknot_type-complextype-visio-xml"></a><span data-ttu-id="4ce6d-102">SplineKnot_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4ce6d-102">SplineKnot_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="4ce6d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="4ce6d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ce6d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4ce6d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4ce6d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4ce6d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4ce6d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4ce6d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4ce6d-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="4ce6d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4ce6d-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="4ce6d-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4ce6d-109">定義</span><span class="sxs-lookup"><span data-stu-id="4ce6d-109">Definition</span></span>

```XML
          <xs:complexType name="SplineKnot_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4ce6d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4ce6d-110">Elements and attributes</span></span>

<span data-ttu-id="4ce6d-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ce6d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4ce6d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="4ce6d-112">Child elements</span></span>

|<span data-ttu-id="4ce6d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ce6d-113">**Element**</span></span>|<span data-ttu-id="4ce6d-114">**型**</span><span class="sxs-lookup"><span data-stu-id="4ce6d-114">**Type**</span></span>|<span data-ttu-id="4ce6d-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="4ce6d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4ce6d-116">Cell</span><span class="sxs-lookup"><span data-stu-id="4ce6d-116">Cell</span></span>](cell-element-splineknot-rowvisio-xml.md) <br/> |[<span data-ttu-id="4ce6d-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4ce6d-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4ce6d-118">属性</span><span class="sxs-lookup"><span data-stu-id="4ce6d-118">Attributes</span></span>

<span data-ttu-id="4ce6d-119">なし。</span><span class="sxs-lookup"><span data-stu-id="4ce6d-119">None.</span></span>
  

