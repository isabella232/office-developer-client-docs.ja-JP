---
title: Shapes_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 7d028939ad6c99ecf4160b95764c86779c399c8e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397612"
---
# <a name="shapestype-complextype-visio-xml"></a><span data-ttu-id="cb896-102">Shapes_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="cb896-102">Shapes_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cb896-103">型情報</span><span class="sxs-lookup"><span data-stu-id="cb896-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb896-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="cb896-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cb896-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="cb896-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cb896-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cb896-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cb896-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="cb896-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cb896-108">なし</span><span class="sxs-lookup"><span data-stu-id="cb896-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cb896-109">定義</span><span class="sxs-lookup"><span data-stu-id="cb896-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cb896-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="cb896-110">Elements and attributes</span></span>

<span data-ttu-id="cb896-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb896-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cb896-112">子要素</span><span class="sxs-lookup"><span data-stu-id="cb896-112">Child elements</span></span>

|<span data-ttu-id="cb896-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="cb896-113">**Element**</span></span>|<span data-ttu-id="cb896-114">**型**</span><span class="sxs-lookup"><span data-stu-id="cb896-114">**Type**</span></span>|<span data-ttu-id="cb896-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb896-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cb896-116">Shape</span><span class="sxs-lookup"><span data-stu-id="cb896-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb896-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="cb896-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cb896-118">属性</span><span class="sxs-lookup"><span data-stu-id="cb896-118">Attributes</span></span>

<span data-ttu-id="cb896-119">なし。</span><span class="sxs-lookup"><span data-stu-id="cb896-119">None.</span></span>
  

