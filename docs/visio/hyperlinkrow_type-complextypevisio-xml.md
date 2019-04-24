---
title: HyperlinkRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f8ded1a6-3bbd-0d59-c9f0-ab84341888cd
ms.openlocfilehash: 0056c87f4926f440ffcfd85619fd5ab7cba308db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344836"
---
# <a name="hyperlinkrowtype-complextype-visio-xml"></a><span data-ttu-id="5fdc8-102">HyperlinkRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="5fdc8-102">HyperlinkRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5fdc8-103">型情報</span><span class="sxs-lookup"><span data-stu-id="5fdc8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5fdc8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5fdc8-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5fdc8-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5fdc8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5fdc8-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="5fdc8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5fdc8-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="5fdc8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5fdc8-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="5fdc8-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5fdc8-109">定義</span><span class="sxs-lookup"><span data-stu-id="5fdc8-109">Definition</span></span>

```XML
          <xs:complexType name="HyperlinkRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5fdc8-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5fdc8-110">Elements and attributes</span></span>

<span data-ttu-id="5fdc8-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fdc8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5fdc8-112">子要素</span><span class="sxs-lookup"><span data-stu-id="5fdc8-112">Child elements</span></span>

|<span data-ttu-id="5fdc8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5fdc8-113">**Element**</span></span>|<span data-ttu-id="5fdc8-114">**型**</span><span class="sxs-lookup"><span data-stu-id="5fdc8-114">**Type**</span></span>|<span data-ttu-id="5fdc8-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="5fdc8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5fdc8-116">Cell</span><span class="sxs-lookup"><span data-stu-id="5fdc8-116">Cell</span></span>](cell-element-hyperlink-rowvisio-xml.md) <br/> |[<span data-ttu-id="5fdc8-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="5fdc8-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5fdc8-118">属性</span><span class="sxs-lookup"><span data-stu-id="5fdc8-118">Attributes</span></span>

<span data-ttu-id="5fdc8-119">なし。</span><span class="sxs-lookup"><span data-stu-id="5fdc8-119">None.</span></span>
  

