---
title: RuleSets_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9bd05541-7cd8-321b-8dd6-fa885c269057
ms.openlocfilehash: 3afb97b513e545774065164b0685c78ebd5a1d71
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541562"
---
# <a name="rulesets_type-complextype-visio-xml"></a><span data-ttu-id="deec3-102">RuleSets_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="deec3-102">RuleSets_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="deec3-103">型情報</span><span class="sxs-lookup"><span data-stu-id="deec3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="deec3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="deec3-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="deec3-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="deec3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="deec3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="deec3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="deec3-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="deec3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="deec3-108">なし</span><span class="sxs-lookup"><span data-stu-id="deec3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="deec3-109">定義</span><span class="sxs-lookup"><span data-stu-id="deec3-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="deec3-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="deec3-110">Elements and attributes</span></span>

<span data-ttu-id="deec3-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="deec3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="deec3-112">子要素</span><span class="sxs-lookup"><span data-stu-id="deec3-112">Child elements</span></span>

|<span data-ttu-id="deec3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="deec3-113">**Element**</span></span>|<span data-ttu-id="deec3-114">**型**</span><span class="sxs-lookup"><span data-stu-id="deec3-114">**Type**</span></span>|<span data-ttu-id="deec3-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="deec3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="deec3-116">RuleSet</span><span class="sxs-lookup"><span data-stu-id="deec3-116">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="deec3-117">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="deec3-117">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="deec3-118">属性</span><span class="sxs-lookup"><span data-stu-id="deec3-118">Attributes</span></span>

<span data-ttu-id="deec3-119">なし。</span><span class="sxs-lookup"><span data-stu-id="deec3-119">None.</span></span>
  

