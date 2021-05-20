---
title: PolylineTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e0b87cc0-397d-7640-34ea-2a725d8f0999
ms.openlocfilehash: e1c6c6912105ba593467cd4bb4e4cb0ded460233
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540099"
---
# <a name="polylineto_type-complextype-visio-xml"></a><span data-ttu-id="e7458-102">PolylineTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e7458-102">PolylineTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e7458-103">型情報</span><span class="sxs-lookup"><span data-stu-id="e7458-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7458-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e7458-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e7458-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e7458-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e7458-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e7458-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e7458-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="e7458-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e7458-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="e7458-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e7458-109">定義</span><span class="sxs-lookup"><span data-stu-id="e7458-109">Definition</span></span>

```XML
          <xs:complexType name="PolylineTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="e7458-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e7458-110">Elements and attributes</span></span>

<span data-ttu-id="e7458-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7458-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e7458-112">子要素</span><span class="sxs-lookup"><span data-stu-id="e7458-112">Child elements</span></span>

|<span data-ttu-id="e7458-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e7458-113">**Element**</span></span>|<span data-ttu-id="e7458-114">**型**</span><span class="sxs-lookup"><span data-stu-id="e7458-114">**Type**</span></span>|<span data-ttu-id="e7458-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="e7458-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e7458-116">Cell</span><span class="sxs-lookup"><span data-stu-id="e7458-116">Cell</span></span>](cell-element-polylineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="e7458-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e7458-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e7458-118">属性</span><span class="sxs-lookup"><span data-stu-id="e7458-118">Attributes</span></span>

<span data-ttu-id="e7458-119">なし。</span><span class="sxs-lookup"><span data-stu-id="e7458-119">None.</span></span>
  

