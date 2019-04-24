---
title: ControlRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f9ee251-e685-e56c-3c8a-cb727ad62064
ms.openlocfilehash: 7cd09b4644cc72648bf880a3c187fa59274e6e02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282972"
---
# <a name="controlrowtype-complextype-visio-xml"></a><span data-ttu-id="91baf-102">ControlRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="91baf-102">ControlRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="91baf-103">型情報</span><span class="sxs-lookup"><span data-stu-id="91baf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91baf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="91baf-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="91baf-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="91baf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="91baf-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="91baf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="91baf-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="91baf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="91baf-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="91baf-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="91baf-109">定義</span><span class="sxs-lookup"><span data-stu-id="91baf-109">Definition</span></span>

```XML
          <xs:complexType name="ControlRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedIndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="91baf-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="91baf-110">Elements and attributes</span></span>

<span data-ttu-id="91baf-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="91baf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="91baf-112">子要素</span><span class="sxs-lookup"><span data-stu-id="91baf-112">Child elements</span></span>

|<span data-ttu-id="91baf-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="91baf-113">**Element**</span></span>|<span data-ttu-id="91baf-114">**型**</span><span class="sxs-lookup"><span data-stu-id="91baf-114">**Type**</span></span>|<span data-ttu-id="91baf-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="91baf-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="91baf-116">Cell</span><span class="sxs-lookup"><span data-stu-id="91baf-116">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="91baf-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="91baf-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="91baf-118">属性</span><span class="sxs-lookup"><span data-stu-id="91baf-118">Attributes</span></span>

<span data-ttu-id="91baf-119">なし。</span><span class="sxs-lookup"><span data-stu-id="91baf-119">None.</span></span>
  

