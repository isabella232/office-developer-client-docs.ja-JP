---
title: PropertyRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 813d6dee-b113-c0c9-3f53-c5bfd05b92f2
ms.openlocfilehash: 32940a8e549c9007181217509b3748cc4f449fe0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540729"
---
# <a name="propertyrow_type-complextype-visio-xml"></a><span data-ttu-id="a29f1-102">PropertyRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a29f1-102">PropertyRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a29f1-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a29f1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a29f1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a29f1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a29f1-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a29f1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a29f1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a29f1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a29f1-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a29f1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a29f1-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="a29f1-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a29f1-109">定義</span><span class="sxs-lookup"><span data-stu-id="a29f1-109">Definition</span></span>

```XML
          <xs:complexType name="PropertyRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="a29f1-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a29f1-110">Elements and attributes</span></span>

<span data-ttu-id="a29f1-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a29f1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a29f1-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a29f1-112">Child elements</span></span>

|<span data-ttu-id="a29f1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a29f1-113">**Element**</span></span>|<span data-ttu-id="a29f1-114">**型**</span><span class="sxs-lookup"><span data-stu-id="a29f1-114">**Type**</span></span>|<span data-ttu-id="a29f1-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="a29f1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a29f1-116">Cell</span><span class="sxs-lookup"><span data-stu-id="a29f1-116">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a29f1-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a29f1-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a29f1-118">属性</span><span class="sxs-lookup"><span data-stu-id="a29f1-118">Attributes</span></span>

<span data-ttu-id="a29f1-119">なし。</span><span class="sxs-lookup"><span data-stu-id="a29f1-119">None.</span></span>
  

