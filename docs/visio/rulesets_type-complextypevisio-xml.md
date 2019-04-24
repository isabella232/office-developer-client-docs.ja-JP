---
title: RuleSets_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9bd05541-7cd8-321b-8dd6-fa885c269057
ms.openlocfilehash: 41172a4f15b0d9038fd0ffb0c0a7d8c3d4078798
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319041"
---
# <a name="rulesetstype-complextype-visio-xml"></a><span data-ttu-id="1672d-102">RuleSets_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1672d-102">RuleSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1672d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="1672d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1672d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1672d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1672d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1672d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1672d-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="1672d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1672d-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="1672d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1672d-108">なし</span><span class="sxs-lookup"><span data-stu-id="1672d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1672d-109">定義</span><span class="sxs-lookup"><span data-stu-id="1672d-109">Definition</span></span>

```XML
          <xs:complexType name="RuleSets_Type">
          
          <xs:sequence>
    <xs:element name="RuleSet"  type="RuleSet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1672d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1672d-110">Elements and attributes</span></span>

<span data-ttu-id="1672d-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1672d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1672d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1672d-112">Child elements</span></span>

|<span data-ttu-id="1672d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1672d-113">**Element**</span></span>|<span data-ttu-id="1672d-114">**型**</span><span class="sxs-lookup"><span data-stu-id="1672d-114">**Type**</span></span>|<span data-ttu-id="1672d-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="1672d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1672d-116">RuleSet</span><span class="sxs-lookup"><span data-stu-id="1672d-116">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1672d-117">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="1672d-117">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1672d-118">属性</span><span class="sxs-lookup"><span data-stu-id="1672d-118">Attributes</span></span>

<span data-ttu-id="1672d-119">なし。</span><span class="sxs-lookup"><span data-stu-id="1672d-119">None.</span></span>
  

