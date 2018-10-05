---
title: Extensions_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f516e1a-e789-8085-1cc3-70514910eb26
ms.openlocfilehash: 7760e1b22a7d573d8f61cf08ed54789f601e9339
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398137"
---
# <a name="extensionstype-complextype-visio-xml"></a><span data-ttu-id="2b616-102">Extensions_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="2b616-102">Extensions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2b616-103">型情報</span><span class="sxs-lookup"><span data-stu-id="2b616-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b616-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="2b616-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2b616-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="2b616-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2b616-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2b616-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2b616-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="2b616-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2b616-108">なし</span><span class="sxs-lookup"><span data-stu-id="2b616-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2b616-109">定義</span><span class="sxs-lookup"><span data-stu-id="2b616-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2b616-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="2b616-110">Elements and attributes</span></span>

<span data-ttu-id="2b616-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b616-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2b616-112">子要素</span><span class="sxs-lookup"><span data-stu-id="2b616-112">Child elements</span></span>

|<span data-ttu-id="2b616-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="2b616-113">**Element**</span></span>|<span data-ttu-id="2b616-114">**型**</span><span class="sxs-lookup"><span data-stu-id="2b616-114">**Type**</span></span>|<span data-ttu-id="2b616-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="2b616-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2b616-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="2b616-116">CellDef</span></span> <br/> |[<span data-ttu-id="2b616-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="2b616-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="2b616-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="2b616-118">FunctionDef</span></span> <br/> |[<span data-ttu-id="2b616-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="2b616-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="2b616-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="2b616-120">SectionDef</span></span> <br/> |[<span data-ttu-id="2b616-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="2b616-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2b616-122">属性</span><span class="sxs-lookup"><span data-stu-id="2b616-122">Attributes</span></span>

<span data-ttu-id="2b616-123">なし。</span><span class="sxs-lookup"><span data-stu-id="2b616-123">None.</span></span>
  

