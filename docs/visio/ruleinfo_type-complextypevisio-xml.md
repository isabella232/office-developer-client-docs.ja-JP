---
title: RuleInfo_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0548f2b493677ab63ef75548149e709645c0cf75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382569"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="72ac2-102">RuleInfo_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="72ac2-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="72ac2-103">型情報</span><span class="sxs-lookup"><span data-stu-id="72ac2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72ac2-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="72ac2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="72ac2-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="72ac2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="72ac2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="72ac2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="72ac2-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="72ac2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="72ac2-108">なし</span><span class="sxs-lookup"><span data-stu-id="72ac2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="72ac2-109">定義</span><span class="sxs-lookup"><span data-stu-id="72ac2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="72ac2-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="72ac2-110">Elements and attributes</span></span>

<span data-ttu-id="72ac2-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72ac2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="72ac2-112">子要素</span><span class="sxs-lookup"><span data-stu-id="72ac2-112">Child elements</span></span>

<span data-ttu-id="72ac2-113">なし。</span><span class="sxs-lookup"><span data-stu-id="72ac2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="72ac2-114">属性</span><span class="sxs-lookup"><span data-stu-id="72ac2-114">Attributes</span></span>

|<span data-ttu-id="72ac2-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="72ac2-115">**Attribute**</span></span>|<span data-ttu-id="72ac2-116">**型**</span><span class="sxs-lookup"><span data-stu-id="72ac2-116">**Type**</span></span>|<span data-ttu-id="72ac2-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="72ac2-117">**Required**</span></span>|<span data-ttu-id="72ac2-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="72ac2-118">**Description**</span></span>|<span data-ttu-id="72ac2-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="72ac2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="72ac2-120">規則 Id</span><span class="sxs-lookup"><span data-stu-id="72ac2-120">RuleID</span></span>  <br/> |<span data-ttu-id="72ac2-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="72ac2-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="72ac2-122">必須</span><span class="sxs-lookup"><span data-stu-id="72ac2-122">required</span></span>  <br/> ||<span data-ttu-id="72ac2-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="72ac2-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="72ac2-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="72ac2-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="72ac2-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="72ac2-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="72ac2-126">必須</span><span class="sxs-lookup"><span data-stu-id="72ac2-126">required</span></span>  <br/> ||<span data-ttu-id="72ac2-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="72ac2-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

