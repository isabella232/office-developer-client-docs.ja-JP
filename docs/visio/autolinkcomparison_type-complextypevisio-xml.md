---
title: AutoLinkComparison_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: 235b63777d21955a2f2062757d6a54e899b169ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338599"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="73f02-102">AutoLinkComparison_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="73f02-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="73f02-103">型情報</span><span class="sxs-lookup"><span data-stu-id="73f02-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73f02-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="73f02-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="73f02-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="73f02-105">**Schema file**</span></span> <br/> |<span data-ttu-id="73f02-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="73f02-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="73f02-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="73f02-107">**Extension base**</span></span> <br/> |<span data-ttu-id="73f02-108">None</span><span class="sxs-lookup"><span data-stu-id="73f02-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="73f02-109">定義</span><span class="sxs-lookup"><span data-stu-id="73f02-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="73f02-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="73f02-110">Elements and attributes</span></span>

<span data-ttu-id="73f02-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="73f02-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="73f02-112">子要素</span><span class="sxs-lookup"><span data-stu-id="73f02-112">Child elements</span></span>

<span data-ttu-id="73f02-113">なし。</span><span class="sxs-lookup"><span data-stu-id="73f02-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73f02-114">属性</span><span class="sxs-lookup"><span data-stu-id="73f02-114">Attributes</span></span>

|<span data-ttu-id="73f02-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="73f02-115">**Attribute**</span></span>|<span data-ttu-id="73f02-116">**型**</span><span class="sxs-lookup"><span data-stu-id="73f02-116">**Type**</span></span>|<span data-ttu-id="73f02-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="73f02-117">**Required**</span></span>|<span data-ttu-id="73f02-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="73f02-118">**Description**</span></span>|<span data-ttu-id="73f02-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="73f02-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="73f02-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="73f02-120">ColumnName</span></span>  <br/> |<span data-ttu-id="73f02-121">xsd: string</span><span class="sxs-lookup"><span data-stu-id="73f02-121">xsd:string</span></span>  <br/> |<span data-ttu-id="73f02-122">必須</span><span class="sxs-lookup"><span data-stu-id="73f02-122">required</span></span>  <br/> ||<span data-ttu-id="73f02-123">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="73f02-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="73f02-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="73f02-124">ContextType</span></span>  <br/> |<span data-ttu-id="73f02-125">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="73f02-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="73f02-126">必須</span><span class="sxs-lookup"><span data-stu-id="73f02-126">required</span></span>  <br/> ||<span data-ttu-id="73f02-127">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="73f02-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="73f02-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="73f02-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="73f02-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="73f02-129">xsd:string</span></span>  <br/> |<span data-ttu-id="73f02-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="73f02-130">optional</span></span>  <br/> ||<span data-ttu-id="73f02-131">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="73f02-131">Values of the xsd:string type.</span></span>  <br/> |
   

