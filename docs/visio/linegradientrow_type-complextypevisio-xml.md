---
title: LineGradientRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b35d58b-ec6f-9b99-01fb-c665630e65d7
ms.openlocfilehash: e48172e8213359244a61716d208b8b98776429af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361132"
---
# <a name="linegradientrowtype-complextype-visio-xml"></a><span data-ttu-id="d81b2-102">LineGradientRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d81b2-102">LineGradientRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d81b2-103">型情報</span><span class="sxs-lookup"><span data-stu-id="d81b2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d81b2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d81b2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d81b2-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d81b2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d81b2-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="d81b2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d81b2-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="d81b2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d81b2-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="d81b2-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d81b2-109">定義</span><span class="sxs-lookup"><span data-stu-id="d81b2-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradientRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="d81b2-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d81b2-110">Elements and attributes</span></span>

<span data-ttu-id="d81b2-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d81b2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d81b2-112">子要素</span><span class="sxs-lookup"><span data-stu-id="d81b2-112">Child elements</span></span>

|<span data-ttu-id="d81b2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d81b2-113">**Element**</span></span>|<span data-ttu-id="d81b2-114">**型**</span><span class="sxs-lookup"><span data-stu-id="d81b2-114">**Type**</span></span>|<span data-ttu-id="d81b2-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="d81b2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d81b2-116">Cell</span><span class="sxs-lookup"><span data-stu-id="d81b2-116">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d81b2-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d81b2-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d81b2-118">属性</span><span class="sxs-lookup"><span data-stu-id="d81b2-118">Attributes</span></span>

<span data-ttu-id="d81b2-119">なし。</span><span class="sxs-lookup"><span data-stu-id="d81b2-119">None.</span></span>
  

