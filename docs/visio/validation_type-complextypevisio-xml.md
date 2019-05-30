---
title: Validation_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bc106ec-879a-0a4b-8c04-a5734eb0097a
ms.openlocfilehash: 7c7b3c8b1a5fdb52ee835c87e18941b902b51734
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538530"
---
# <a name="validationtype-complextype-visio-xml"></a><span data-ttu-id="cb717-102">Validation_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="cb717-102">Validation_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="cb717-103">型情報</span><span class="sxs-lookup"><span data-stu-id="cb717-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb717-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cb717-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cb717-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="cb717-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cb717-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="cb717-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cb717-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="cb717-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cb717-108">None</span><span class="sxs-lookup"><span data-stu-id="cb717-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cb717-109">定義</span><span class="sxs-lookup"><span data-stu-id="cb717-109">Definition</span></span>

```XML
          <xs:complexType name="Validation_Type">
          
          <xs:sequence>
    <xs:element name="ValidationProperties"  type="ValidationProperties_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleSets"  type="RuleSets_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Issues"  type="Issues_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cb717-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="cb717-110">Elements and attributes</span></span>

<span data-ttu-id="cb717-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb717-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cb717-112">子要素</span><span class="sxs-lookup"><span data-stu-id="cb717-112">Child elements</span></span>

|<span data-ttu-id="cb717-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cb717-113">**Element**</span></span>|<span data-ttu-id="cb717-114">**型**</span><span class="sxs-lookup"><span data-stu-id="cb717-114">**Type**</span></span>|<span data-ttu-id="cb717-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb717-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cb717-116">Issues</span><span class="sxs-lookup"><span data-stu-id="cb717-116">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb717-117">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="cb717-117">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="cb717-118">RuleSets</span><span class="sxs-lookup"><span data-stu-id="cb717-118">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb717-119">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="cb717-119">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="cb717-120">ValidationProperties プロパティ</span><span class="sxs-lookup"><span data-stu-id="cb717-120">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb717-121">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="cb717-121">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cb717-122">属性</span><span class="sxs-lookup"><span data-stu-id="cb717-122">Attributes</span></span>

<span data-ttu-id="cb717-123">なし。</span><span class="sxs-lookup"><span data-stu-id="cb717-123">None.</span></span>
  

