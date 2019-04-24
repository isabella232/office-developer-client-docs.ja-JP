---
title: RuleInfo_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0548f2b493677ab63ef75548149e709645c0cf75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360467"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="b0463-102">RuleInfo_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b0463-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b0463-103">型情報</span><span class="sxs-lookup"><span data-stu-id="b0463-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0463-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b0463-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b0463-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b0463-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b0463-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="b0463-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b0463-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="b0463-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b0463-108">なし</span><span class="sxs-lookup"><span data-stu-id="b0463-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b0463-109">定義</span><span class="sxs-lookup"><span data-stu-id="b0463-109">Definition</span></span>

```XML
      <xs:complexType name="RuleInfo_Type">
    <xs:attribute name="RuleSetID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RuleID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b0463-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b0463-110">Elements and attributes</span></span>

<span data-ttu-id="b0463-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0463-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b0463-112">子要素</span><span class="sxs-lookup"><span data-stu-id="b0463-112">Child elements</span></span>

<span data-ttu-id="b0463-113">なし。</span><span class="sxs-lookup"><span data-stu-id="b0463-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0463-114">属性</span><span class="sxs-lookup"><span data-stu-id="b0463-114">Attributes</span></span>

|<span data-ttu-id="b0463-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="b0463-115">**Attribute**</span></span>|<span data-ttu-id="b0463-116">**型**</span><span class="sxs-lookup"><span data-stu-id="b0463-116">**Type**</span></span>|<span data-ttu-id="b0463-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="b0463-117">**Required**</span></span>|<span data-ttu-id="b0463-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="b0463-118">**Description**</span></span>|<span data-ttu-id="b0463-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="b0463-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b0463-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="b0463-120">RuleID</span></span>  <br/> |<span data-ttu-id="b0463-121">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="b0463-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b0463-122">必須</span><span class="sxs-lookup"><span data-stu-id="b0463-122">required</span></span>  <br/> ||<span data-ttu-id="b0463-123">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="b0463-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b0463-124">rulesetid</span><span class="sxs-lookup"><span data-stu-id="b0463-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="b0463-125">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="b0463-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b0463-126">必須</span><span class="sxs-lookup"><span data-stu-id="b0463-126">required</span></span>  <br/> ||<span data-ttu-id="b0463-127">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="b0463-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

