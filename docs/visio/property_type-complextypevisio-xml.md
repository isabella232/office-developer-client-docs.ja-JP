---
title: Property_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4f927461-7122-1742-57f5-e2035890b486
ms.openlocfilehash: ada20c601fcd42bf551a0aea63787aac96062816
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326874"
---
# <a name="propertytype-complextype-visio-xml"></a><span data-ttu-id="62156-102">Property_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="62156-102">Property_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="62156-103">型情報</span><span class="sxs-lookup"><span data-stu-id="62156-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62156-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="62156-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="62156-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="62156-105">**Schema file**</span></span> <br/> |<span data-ttu-id="62156-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="62156-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="62156-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="62156-107">**Extension base**</span></span> <br/> |<span data-ttu-id="62156-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="62156-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="62156-109">定義</span><span class="sxs-lookup"><span data-stu-id="62156-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="62156-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="62156-110">Elements and attributes</span></span>

<span data-ttu-id="62156-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="62156-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="62156-112">子要素</span><span class="sxs-lookup"><span data-stu-id="62156-112">Child elements</span></span>

|<span data-ttu-id="62156-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="62156-113">**Element**</span></span>|<span data-ttu-id="62156-114">**型**</span><span class="sxs-lookup"><span data-stu-id="62156-114">**Type**</span></span>|<span data-ttu-id="62156-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="62156-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62156-116">Row</span><span class="sxs-lookup"><span data-stu-id="62156-116">Row</span></span>](row-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="62156-117">PropertyRow_Type</span><span class="sxs-lookup"><span data-stu-id="62156-117">PropertyRow_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="62156-118">属性</span><span class="sxs-lookup"><span data-stu-id="62156-118">Attributes</span></span>

<span data-ttu-id="62156-119">なし。</span><span class="sxs-lookup"><span data-stu-id="62156-119">None.</span></span>
  

