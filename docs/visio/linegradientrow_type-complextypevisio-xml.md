---
title: LineGradientRow_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b35d58b-ec6f-9b99-01fb-c665630e65d7
ms.openlocfilehash: e21ae09918c1814f2daedfdfb42f52b7d8f515ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805739"
---
# <a name="linegradientrowtype-complextype-visio-xml"></a><span data-ttu-id="a84c5-102">LineGradientRow_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a84c5-102">LineGradientRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a84c5-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a84c5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a84c5-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a84c5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a84c5-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a84c5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a84c5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a84c5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a84c5-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="a84c5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a84c5-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="a84c5-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a84c5-109">定義</span><span class="sxs-lookup"><span data-stu-id="a84c5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a84c5-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a84c5-110">Elements and attributes</span></span>

<span data-ttu-id="a84c5-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a84c5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a84c5-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a84c5-112">Child elements</span></span>

|<span data-ttu-id="a84c5-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="a84c5-113">**Element**</span></span>|<span data-ttu-id="a84c5-114">**型**</span><span class="sxs-lookup"><span data-stu-id="a84c5-114">**Type**</span></span>|<span data-ttu-id="a84c5-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="a84c5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a84c5-116">Cell</span><span class="sxs-lookup"><span data-stu-id="a84c5-116">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a84c5-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a84c5-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a84c5-118">属性</span><span class="sxs-lookup"><span data-stu-id="a84c5-118">Attributes</span></span>

<span data-ttu-id="a84c5-119">なし。</span><span class="sxs-lookup"><span data-stu-id="a84c5-119">None.</span></span>
  

