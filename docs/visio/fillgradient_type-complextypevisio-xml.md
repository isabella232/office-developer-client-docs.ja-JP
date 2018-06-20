---
title: FillGradient_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 82545cdc-890d-1b2f-9c8f-4740f32d0ed7
ms.openlocfilehash: 15500f9ffa8375a8b34a09cd9bd72efa7ad82768
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805366"
---
# <a name="fillgradienttype-complextype-visio-xml"></a><span data-ttu-id="4e52e-102">FillGradient_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="4e52e-102">FillGradient_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4e52e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="4e52e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e52e-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="4e52e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4e52e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4e52e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4e52e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4e52e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4e52e-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="4e52e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4e52e-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="4e52e-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4e52e-109">定義</span><span class="sxs-lookup"><span data-stu-id="4e52e-109">Definition</span></span>

```XML
          <xs:complexType name="FillGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="FillGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4e52e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4e52e-110">Elements and attributes</span></span>

<span data-ttu-id="4e52e-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4e52e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4e52e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="4e52e-112">Child elements</span></span>

|<span data-ttu-id="4e52e-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="4e52e-113">**Element**</span></span>|<span data-ttu-id="4e52e-114">**型**</span><span class="sxs-lookup"><span data-stu-id="4e52e-114">**Type**</span></span>|<span data-ttu-id="4e52e-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="4e52e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4e52e-116">Row</span><span class="sxs-lookup"><span data-stu-id="4e52e-116">Row</span></span>](row-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="4e52e-117">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="4e52e-117">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4e52e-118">属性</span><span class="sxs-lookup"><span data-stu-id="4e52e-118">Attributes</span></span>

<span data-ttu-id="4e52e-119">なし。</span><span class="sxs-lookup"><span data-stu-id="4e52e-119">None.</span></span>
  

