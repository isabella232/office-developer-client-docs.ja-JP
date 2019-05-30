---
title: Shapes_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 798af3d68df6c430fffb318e5e19c83aea441ca0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542087"
---
# <a name="shapestype-complextype-visio-xml"></a><span data-ttu-id="08fac-102">Shapes_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="08fac-102">Shapes_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="08fac-103">型情報</span><span class="sxs-lookup"><span data-stu-id="08fac-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08fac-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="08fac-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="08fac-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="08fac-105">**Schema file**</span></span> <br/> |<span data-ttu-id="08fac-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="08fac-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="08fac-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="08fac-107">**Extension base**</span></span> <br/> |<span data-ttu-id="08fac-108">None</span><span class="sxs-lookup"><span data-stu-id="08fac-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="08fac-109">定義</span><span class="sxs-lookup"><span data-stu-id="08fac-109">Definition</span></span>

```XML
          <xs:complexType name="Shapes_Type">
          
          <xs:sequence>
    <xs:element name="Shape"  type="ShapeSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="08fac-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="08fac-110">Elements and attributes</span></span>

<span data-ttu-id="08fac-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="08fac-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="08fac-112">子要素</span><span class="sxs-lookup"><span data-stu-id="08fac-112">Child elements</span></span>

|<span data-ttu-id="08fac-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="08fac-113">**Element**</span></span>|<span data-ttu-id="08fac-114">**型**</span><span class="sxs-lookup"><span data-stu-id="08fac-114">**Type**</span></span>|<span data-ttu-id="08fac-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="08fac-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="08fac-116">Shape</span><span class="sxs-lookup"><span data-stu-id="08fac-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="08fac-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="08fac-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="08fac-118">属性</span><span class="sxs-lookup"><span data-stu-id="08fac-118">Attributes</span></span>

<span data-ttu-id="08fac-119">なし。</span><span class="sxs-lookup"><span data-stu-id="08fac-119">None.</span></span>
  

