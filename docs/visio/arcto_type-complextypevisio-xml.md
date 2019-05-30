---
title: ArcTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c30c80eb-6327-ebc3-7ea4-8b2fc7525cc0
ms.openlocfilehash: 7fb07f7424e78ffa7b9efec190b839fd7713884a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539699"
---
# <a name="arctotype-complextype-visio-xml"></a><span data-ttu-id="431a8-102">ArcTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="431a8-102">ArcTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="431a8-103">型情報</span><span class="sxs-lookup"><span data-stu-id="431a8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="431a8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="431a8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="431a8-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="431a8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="431a8-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="431a8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="431a8-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="431a8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="431a8-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="431a8-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="431a8-109">定義</span><span class="sxs-lookup"><span data-stu-id="431a8-109">Definition</span></span>

```XML
          <xs:complexType name="ArcTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="431a8-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="431a8-110">Elements and attributes</span></span>

<span data-ttu-id="431a8-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="431a8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="431a8-112">子要素</span><span class="sxs-lookup"><span data-stu-id="431a8-112">Child elements</span></span>

|<span data-ttu-id="431a8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="431a8-113">**Element**</span></span>|<span data-ttu-id="431a8-114">**型**</span><span class="sxs-lookup"><span data-stu-id="431a8-114">**Type**</span></span>|<span data-ttu-id="431a8-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="431a8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="431a8-116">Cell</span><span class="sxs-lookup"><span data-stu-id="431a8-116">Cell</span></span>](cell-element-arcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="431a8-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="431a8-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="431a8-118">属性</span><span class="sxs-lookup"><span data-stu-id="431a8-118">Attributes</span></span>

<span data-ttu-id="431a8-119">なし。</span><span class="sxs-lookup"><span data-stu-id="431a8-119">None.</span></span>
  

