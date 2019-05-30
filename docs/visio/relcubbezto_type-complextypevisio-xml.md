---
title: RelCubBezTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 004dc563-d089-230f-0055-038b72eebbed
ms.openlocfilehash: 7d18a6e4317736b802a761ccbe62e9f01aa1e15d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542719"
---
# <a name="relcubbeztotype-complextype-visio-xml"></a><span data-ttu-id="328fb-102">RelCubBezTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="328fb-102">RelCubBezTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="328fb-103">型情報</span><span class="sxs-lookup"><span data-stu-id="328fb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="328fb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="328fb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="328fb-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="328fb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="328fb-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="328fb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="328fb-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="328fb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="328fb-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="328fb-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="328fb-109">定義</span><span class="sxs-lookup"><span data-stu-id="328fb-109">Definition</span></span>

```XML
          <xs:complexType name="RelCubBezTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="328fb-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="328fb-110">Elements and attributes</span></span>

<span data-ttu-id="328fb-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="328fb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="328fb-112">子要素</span><span class="sxs-lookup"><span data-stu-id="328fb-112">Child elements</span></span>

|<span data-ttu-id="328fb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="328fb-113">**Element**</span></span>|<span data-ttu-id="328fb-114">**型**</span><span class="sxs-lookup"><span data-stu-id="328fb-114">**Type**</span></span>|<span data-ttu-id="328fb-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="328fb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="328fb-116">Cell</span><span class="sxs-lookup"><span data-stu-id="328fb-116">Cell</span></span>](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[<span data-ttu-id="328fb-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="328fb-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="328fb-118">属性</span><span class="sxs-lookup"><span data-stu-id="328fb-118">Attributes</span></span>

<span data-ttu-id="328fb-119">なし。</span><span class="sxs-lookup"><span data-stu-id="328fb-119">None.</span></span>
  

