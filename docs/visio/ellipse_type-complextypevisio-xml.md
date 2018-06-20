---
title: Ellipse_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67dc78e-6639-e32f-4909-945001659d30
ms.openlocfilehash: 84be003154bd8810dc3443a355feee0ec4cec19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805330"
---
# <a name="ellipsetype-complextype-visio-xml"></a><span data-ttu-id="57499-102">Ellipse_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="57499-102">Ellipse_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="57499-103">型情報</span><span class="sxs-lookup"><span data-stu-id="57499-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57499-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="57499-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="57499-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="57499-105">**Schema file**</span></span> <br/> |<span data-ttu-id="57499-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="57499-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="57499-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="57499-107">**Extension base**</span></span> <br/> |<span data-ttu-id="57499-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="57499-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="57499-109">定義</span><span class="sxs-lookup"><span data-stu-id="57499-109">Definition</span></span>

```XML
          <xs:complexType name="Ellipse_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="57499-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="57499-110">Elements and attributes</span></span>

<span data-ttu-id="57499-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="57499-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="57499-112">子要素</span><span class="sxs-lookup"><span data-stu-id="57499-112">Child elements</span></span>

|<span data-ttu-id="57499-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="57499-113">**Element**</span></span>|<span data-ttu-id="57499-114">**型**</span><span class="sxs-lookup"><span data-stu-id="57499-114">**Type**</span></span>|<span data-ttu-id="57499-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="57499-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="57499-116">Cell</span><span class="sxs-lookup"><span data-stu-id="57499-116">Cell</span></span>](cell-element-ellipse-rowvisio-xml.md) <br/> |[<span data-ttu-id="57499-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="57499-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="57499-118">属性</span><span class="sxs-lookup"><span data-stu-id="57499-118">Attributes</span></span>

<span data-ttu-id="57499-119">なし。</span><span class="sxs-lookup"><span data-stu-id="57499-119">None.</span></span>
  

