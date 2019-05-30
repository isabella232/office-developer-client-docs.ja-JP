---
title: Extensions_Type complexType (Visio XML)
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
# <a name="extensionstype-complextype-visio-xml"></a><span data-ttu-id="d4702-102">Extensions_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d4702-102">Extensions_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d4702-103">型情報</span><span class="sxs-lookup"><span data-stu-id="d4702-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4702-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d4702-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d4702-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d4702-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d4702-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="d4702-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d4702-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="d4702-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d4702-108">None</span><span class="sxs-lookup"><span data-stu-id="d4702-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d4702-109">定義</span><span class="sxs-lookup"><span data-stu-id="d4702-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d4702-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d4702-110">Elements and attributes</span></span>

<span data-ttu-id="d4702-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4702-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d4702-112">子要素</span><span class="sxs-lookup"><span data-stu-id="d4702-112">Child elements</span></span>

|<span data-ttu-id="d4702-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d4702-113">**Element**</span></span>|<span data-ttu-id="d4702-114">**型**</span><span class="sxs-lookup"><span data-stu-id="d4702-114">**Type**</span></span>|<span data-ttu-id="d4702-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="d4702-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4702-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="d4702-116">CellDef</span></span> <br/> |[<span data-ttu-id="d4702-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="d4702-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="d4702-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="d4702-118">FunctionDef</span></span> <br/> |[<span data-ttu-id="d4702-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="d4702-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="d4702-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="d4702-120">SectionDef</span></span> <br/> |[<span data-ttu-id="d4702-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="d4702-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d4702-122">属性</span><span class="sxs-lookup"><span data-stu-id="d4702-122">Attributes</span></span>

<span data-ttu-id="d4702-123">なし。</span><span class="sxs-lookup"><span data-stu-id="d4702-123">None.</span></span>
  

