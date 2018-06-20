---
title: RelLineTo_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e5504166-653d-15d2-75eb-9b36f376b788
ms.openlocfilehash: 953130a69e477aeef836aa8b95d3979e84e8ba79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806188"
---
# <a name="rellinetotype-complextype-visio-xml"></a><span data-ttu-id="ddd4c-102">RelLineTo_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="ddd4c-102">RelLineTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ddd4c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="ddd4c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ddd4c-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="ddd4c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ddd4c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ddd4c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ddd4c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ddd4c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ddd4c-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="ddd4c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ddd4c-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="ddd4c-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ddd4c-109">定義</span><span class="sxs-lookup"><span data-stu-id="ddd4c-109">Definition</span></span>

```XML
          <xs:complexType name="RelLineTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="ddd4c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ddd4c-110">Elements and attributes</span></span>

<span data-ttu-id="ddd4c-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ddd4c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ddd4c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="ddd4c-112">Child elements</span></span>

|<span data-ttu-id="ddd4c-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="ddd4c-113">**Element**</span></span>|<span data-ttu-id="ddd4c-114">**型**</span><span class="sxs-lookup"><span data-stu-id="ddd4c-114">**Type**</span></span>|<span data-ttu-id="ddd4c-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="ddd4c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ddd4c-116">Cell</span><span class="sxs-lookup"><span data-stu-id="ddd4c-116">Cell</span></span>](cell-element-rellineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="ddd4c-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ddd4c-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ddd4c-118">属性</span><span class="sxs-lookup"><span data-stu-id="ddd4c-118">Attributes</span></span>

<span data-ttu-id="ddd4c-119">なし。</span><span class="sxs-lookup"><span data-stu-id="ddd4c-119">None.</span></span>
  

