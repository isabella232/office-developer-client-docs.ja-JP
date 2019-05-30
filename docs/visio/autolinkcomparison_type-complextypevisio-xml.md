---
title: AutoLinkComparison_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: eeb58a0e2f401c0e8a2bcf67147bc300bb8535ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537886"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="57dda-102">AutoLinkComparison_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="57dda-102">AutoLinkComparison_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="57dda-103">型情報</span><span class="sxs-lookup"><span data-stu-id="57dda-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57dda-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="57dda-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="57dda-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="57dda-105">**Schema file**</span></span> <br/> |<span data-ttu-id="57dda-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="57dda-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="57dda-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="57dda-107">**Extension base**</span></span> <br/> |<span data-ttu-id="57dda-108">None</span><span class="sxs-lookup"><span data-stu-id="57dda-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="57dda-109">定義</span><span class="sxs-lookup"><span data-stu-id="57dda-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="57dda-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="57dda-110">Elements and attributes</span></span>

<span data-ttu-id="57dda-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="57dda-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="57dda-112">子要素</span><span class="sxs-lookup"><span data-stu-id="57dda-112">Child elements</span></span>

<span data-ttu-id="57dda-113">なし。</span><span class="sxs-lookup"><span data-stu-id="57dda-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57dda-114">属性</span><span class="sxs-lookup"><span data-stu-id="57dda-114">Attributes</span></span>

|<span data-ttu-id="57dda-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="57dda-115">**Attribute**</span></span>|<span data-ttu-id="57dda-116">**型**</span><span class="sxs-lookup"><span data-stu-id="57dda-116">**Type**</span></span>|<span data-ttu-id="57dda-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="57dda-117">**Required**</span></span>|<span data-ttu-id="57dda-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="57dda-118">**Description**</span></span>|<span data-ttu-id="57dda-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="57dda-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="57dda-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="57dda-120">ColumnName</span></span>  <br/> |<span data-ttu-id="57dda-121">xsd: string</span><span class="sxs-lookup"><span data-stu-id="57dda-121">xsd:string</span></span>  <br/> |<span data-ttu-id="57dda-122">必須</span><span class="sxs-lookup"><span data-stu-id="57dda-122">required</span></span>  <br/> ||<span data-ttu-id="57dda-123">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="57dda-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="57dda-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="57dda-124">ContextType</span></span>  <br/> |<span data-ttu-id="57dda-125">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="57dda-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="57dda-126">必須</span><span class="sxs-lookup"><span data-stu-id="57dda-126">required</span></span>  <br/> ||<span data-ttu-id="57dda-127">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="57dda-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="57dda-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="57dda-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="57dda-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="57dda-129">xsd:string</span></span>  <br/> |<span data-ttu-id="57dda-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="57dda-130">optional</span></span>  <br/> ||<span data-ttu-id="57dda-131">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="57dda-131">Values of the xsd:string type.</span></span>  <br/> |
   

