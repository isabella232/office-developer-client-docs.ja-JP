---
title: Extensions_Type complexType (xml Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f516e1a-e789-8085-1cc3-70514910eb26
ms.openlocfilehash: 7fe070087afab9cdc6eac9e35a230b02ab7d62ab
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542374"
---
# <a name="extensions_type-complextype-visio-xml"></a><span data-ttu-id="b654e-102">Extensions_Type complexType (xml Visio)</span><span class="sxs-lookup"><span data-stu-id="b654e-102">Extensions_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b654e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="b654e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b654e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b654e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b654e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b654e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b654e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b654e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b654e-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="b654e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b654e-108">なし</span><span class="sxs-lookup"><span data-stu-id="b654e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b654e-109">定義</span><span class="sxs-lookup"><span data-stu-id="b654e-109">Definition</span></span>

```XML
          <xs:complexType name="Extensions_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="FunctionDef"  type="FunctionDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="SectionDef"  type="SectionDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b654e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b654e-110">Elements and attributes</span></span>

<span data-ttu-id="b654e-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b654e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b654e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="b654e-112">Child elements</span></span>

|<span data-ttu-id="b654e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b654e-113">**Element**</span></span>|<span data-ttu-id="b654e-114">**型**</span><span class="sxs-lookup"><span data-stu-id="b654e-114">**Type**</span></span>|<span data-ttu-id="b654e-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="b654e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b654e-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="b654e-116">CellDef</span></span> <br/> |[<span data-ttu-id="b654e-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="b654e-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="b654e-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="b654e-118">FunctionDef</span></span> <br/> |[<span data-ttu-id="b654e-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="b654e-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="b654e-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="b654e-120">SectionDef</span></span> <br/> |[<span data-ttu-id="b654e-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="b654e-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b654e-122">属性</span><span class="sxs-lookup"><span data-stu-id="b654e-122">Attributes</span></span>

<span data-ttu-id="b654e-123">なし。</span><span class="sxs-lookup"><span data-stu-id="b654e-123">None.</span></span>
  

