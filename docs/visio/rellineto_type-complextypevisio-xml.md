---
title: RelLineTo_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e5504166-653d-15d2-75eb-9b36f376b788
ms.openlocfilehash: ca4a270b77fee05957ff04798de1dff1512e837d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396247"
---
# <a name="rellinetotype-complextype-visio-xml"></a><span data-ttu-id="3088c-102">RelLineTo_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="3088c-102">RelLineTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3088c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="3088c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3088c-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="3088c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3088c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="3088c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3088c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3088c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3088c-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="3088c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3088c-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="3088c-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3088c-109">定義</span><span class="sxs-lookup"><span data-stu-id="3088c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3088c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="3088c-110">Elements and attributes</span></span>

<span data-ttu-id="3088c-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3088c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3088c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="3088c-112">Child elements</span></span>

|<span data-ttu-id="3088c-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="3088c-113">**Element**</span></span>|<span data-ttu-id="3088c-114">**型**</span><span class="sxs-lookup"><span data-stu-id="3088c-114">**Type**</span></span>|<span data-ttu-id="3088c-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="3088c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3088c-116">Cell</span><span class="sxs-lookup"><span data-stu-id="3088c-116">Cell</span></span>](cell-element-rellineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="3088c-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="3088c-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3088c-118">属性</span><span class="sxs-lookup"><span data-stu-id="3088c-118">Attributes</span></span>

<span data-ttu-id="3088c-119">なし。</span><span class="sxs-lookup"><span data-stu-id="3088c-119">None.</span></span>
  

