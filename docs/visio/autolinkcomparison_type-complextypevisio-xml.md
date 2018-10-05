---
title: AutoLinkComparison_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: 235b63777d21955a2f2062757d6a54e899b169ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389751"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="199df-102">AutoLinkComparison_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="199df-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="199df-103">型情報</span><span class="sxs-lookup"><span data-stu-id="199df-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="199df-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="199df-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="199df-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="199df-105">**Schema file**</span></span> <br/> |<span data-ttu-id="199df-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="199df-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="199df-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="199df-107">**Extension base**</span></span> <br/> |<span data-ttu-id="199df-108">なし</span><span class="sxs-lookup"><span data-stu-id="199df-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="199df-109">定義</span><span class="sxs-lookup"><span data-stu-id="199df-109">Definition</span></span>

```XML
      <xs:complexType name="AutoLinkComparison_Type">
    <xs:attribute name="ColumnName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ContextType"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ContextTypeLabel"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="199df-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="199df-110">Elements and attributes</span></span>

<span data-ttu-id="199df-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="199df-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="199df-112">子要素</span><span class="sxs-lookup"><span data-stu-id="199df-112">Child elements</span></span>

<span data-ttu-id="199df-113">なし。</span><span class="sxs-lookup"><span data-stu-id="199df-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="199df-114">属性</span><span class="sxs-lookup"><span data-stu-id="199df-114">Attributes</span></span>

|<span data-ttu-id="199df-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="199df-115">**Attribute**</span></span>|<span data-ttu-id="199df-116">**型**</span><span class="sxs-lookup"><span data-stu-id="199df-116">**Type**</span></span>|<span data-ttu-id="199df-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="199df-117">**Required**</span></span>|<span data-ttu-id="199df-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="199df-118">**Description**</span></span>|<span data-ttu-id="199df-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="199df-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="199df-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="199df-120">ColumnName</span></span>  <br/> |<span data-ttu-id="199df-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="199df-121">xsd:string</span></span>  <br/> |<span data-ttu-id="199df-122">必須</span><span class="sxs-lookup"><span data-stu-id="199df-122">required</span></span>  <br/> ||<span data-ttu-id="199df-123">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="199df-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="199df-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="199df-124">ContextType</span></span>  <br/> |<span data-ttu-id="199df-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="199df-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="199df-126">必須</span><span class="sxs-lookup"><span data-stu-id="199df-126">required</span></span>  <br/> ||<span data-ttu-id="199df-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="199df-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="199df-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="199df-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="199df-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="199df-129">xsd:string</span></span>  <br/> |<span data-ttu-id="199df-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="199df-130">optional</span></span>  <br/> ||<span data-ttu-id="199df-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="199df-131">Values of the xsd:string type.</span></span>  <br/> |
   

