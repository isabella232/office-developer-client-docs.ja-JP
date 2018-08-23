---
title: Validation_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bc106ec-879a-0a4b-8c04-a5734eb0097a
ms.openlocfilehash: 26e7dec4ea54e118afd85ec25f334e69849a57dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19806755"
---
# <a name="validationtype-complextype-visio-xml"></a><span data-ttu-id="5859e-102">Validation_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="5859e-102">Validation_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5859e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="5859e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5859e-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="5859e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5859e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5859e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5859e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5859e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5859e-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="5859e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5859e-108">なし</span><span class="sxs-lookup"><span data-stu-id="5859e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5859e-109">定義</span><span class="sxs-lookup"><span data-stu-id="5859e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5859e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5859e-110">Elements and attributes</span></span>

<span data-ttu-id="5859e-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5859e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5859e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="5859e-112">Child elements</span></span>

|<span data-ttu-id="5859e-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="5859e-113">**Element**</span></span>|<span data-ttu-id="5859e-114">**型**</span><span class="sxs-lookup"><span data-stu-id="5859e-114">**Type**</span></span>|<span data-ttu-id="5859e-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="5859e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5859e-116">問題</span><span class="sxs-lookup"><span data-stu-id="5859e-116">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5859e-117">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="5859e-117">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5859e-118">ルールセット</span><span class="sxs-lookup"><span data-stu-id="5859e-118">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5859e-119">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="5859e-119">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5859e-120">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="5859e-120">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5859e-121">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="5859e-121">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5859e-122">属性</span><span class="sxs-lookup"><span data-stu-id="5859e-122">Attributes</span></span>

<span data-ttu-id="5859e-123">なし。</span><span class="sxs-lookup"><span data-stu-id="5859e-123">None.</span></span>
  

