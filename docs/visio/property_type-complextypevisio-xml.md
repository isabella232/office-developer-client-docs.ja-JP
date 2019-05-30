---
title: Property_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4f927461-7122-1742-57f5-e2035890b486
ms.openlocfilehash: 1eb2d9f11a264138f5d1a325d31e17789d1c9483
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540736"
---
# <a name="propertytype-complextype-visio-xml"></a><span data-ttu-id="2f40c-102">Property_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2f40c-102">Property_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="2f40c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="2f40c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f40c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2f40c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2f40c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="2f40c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2f40c-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="2f40c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2f40c-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="2f40c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2f40c-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="2f40c-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2f40c-109">定義</span><span class="sxs-lookup"><span data-stu-id="2f40c-109">Definition</span></span>

```XML
          <xs:complexType name="Property_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="PropertyRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2f40c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="2f40c-110">Elements and attributes</span></span>

<span data-ttu-id="2f40c-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f40c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2f40c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="2f40c-112">Child elements</span></span>

|<span data-ttu-id="2f40c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2f40c-113">**Element**</span></span>|<span data-ttu-id="2f40c-114">**型**</span><span class="sxs-lookup"><span data-stu-id="2f40c-114">**Type**</span></span>|<span data-ttu-id="2f40c-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="2f40c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2f40c-116">Row</span><span class="sxs-lookup"><span data-stu-id="2f40c-116">Row</span></span>](row-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="2f40c-117">PropertyRow_Type</span><span class="sxs-lookup"><span data-stu-id="2f40c-117">PropertyRow_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2f40c-118">属性</span><span class="sxs-lookup"><span data-stu-id="2f40c-118">Attributes</span></span>

<span data-ttu-id="2f40c-119">なし。</span><span class="sxs-lookup"><span data-stu-id="2f40c-119">None.</span></span>
  

