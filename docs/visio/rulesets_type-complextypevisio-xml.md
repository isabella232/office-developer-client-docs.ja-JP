---
title: RuleSets_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9bd05541-7cd8-321b-8dd6-fa885c269057
ms.openlocfilehash: 41172a4f15b0d9038fd0ffb0c0a7d8c3d4078798
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385922"
---
# <a name="rulesetstype-complextype-visio-xml"></a><span data-ttu-id="573c6-102">RuleSets_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="573c6-102">RuleSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="573c6-103">型情報</span><span class="sxs-lookup"><span data-stu-id="573c6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="573c6-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="573c6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="573c6-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="573c6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="573c6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="573c6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="573c6-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="573c6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="573c6-108">なし</span><span class="sxs-lookup"><span data-stu-id="573c6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="573c6-109">定義</span><span class="sxs-lookup"><span data-stu-id="573c6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="573c6-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="573c6-110">Elements and attributes</span></span>

<span data-ttu-id="573c6-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="573c6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="573c6-112">子要素</span><span class="sxs-lookup"><span data-stu-id="573c6-112">Child elements</span></span>

|<span data-ttu-id="573c6-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="573c6-113">**Element**</span></span>|<span data-ttu-id="573c6-114">**型**</span><span class="sxs-lookup"><span data-stu-id="573c6-114">**Type**</span></span>|<span data-ttu-id="573c6-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="573c6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="573c6-116">ルールセット</span><span class="sxs-lookup"><span data-stu-id="573c6-116">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="573c6-117">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="573c6-117">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="573c6-118">属性</span><span class="sxs-lookup"><span data-stu-id="573c6-118">Attributes</span></span>

<span data-ttu-id="573c6-119">なし。</span><span class="sxs-lookup"><span data-stu-id="573c6-119">None.</span></span>
  

