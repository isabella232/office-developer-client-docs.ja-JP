---
title: RelEllipticalArcTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 45b2ff30-bca1-fbaa-cc9f-fe9b52b631c4
ms.openlocfilehash: 701676adcb82c2aeee63a975c2a35fc6c5256635
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542723"
---
# <a name="relellipticalarcto_type-complextype-visio-xml"></a><span data-ttu-id="5f843-102">RelEllipticalArcTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5f843-102">RelEllipticalArcTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="5f843-103">型情報</span><span class="sxs-lookup"><span data-stu-id="5f843-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f843-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5f843-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5f843-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5f843-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5f843-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5f843-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5f843-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="5f843-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5f843-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="5f843-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5f843-109">定義</span><span class="sxs-lookup"><span data-stu-id="5f843-109">Definition</span></span>

```XML
          <xs:complexType name="RelEllipticalArcTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="5f843-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5f843-110">Elements and attributes</span></span>

<span data-ttu-id="5f843-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f843-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5f843-112">子要素</span><span class="sxs-lookup"><span data-stu-id="5f843-112">Child elements</span></span>

|<span data-ttu-id="5f843-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f843-113">**Element**</span></span>|<span data-ttu-id="5f843-114">**型**</span><span class="sxs-lookup"><span data-stu-id="5f843-114">**Type**</span></span>|<span data-ttu-id="5f843-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="5f843-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5f843-116">Cell</span><span class="sxs-lookup"><span data-stu-id="5f843-116">Cell</span></span>](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="5f843-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="5f843-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5f843-118">属性</span><span class="sxs-lookup"><span data-stu-id="5f843-118">Attributes</span></span>

<span data-ttu-id="5f843-119">なし。</span><span class="sxs-lookup"><span data-stu-id="5f843-119">None.</span></span>
  

