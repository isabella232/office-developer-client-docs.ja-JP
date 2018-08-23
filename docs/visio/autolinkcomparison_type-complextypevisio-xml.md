---
title: AutoLinkComparison_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: bb1b07a59fbe3fc706bc67db58e67c5b0ec14033
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804788"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="0812f-102">AutoLinkComparison_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="0812f-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0812f-103">型情報</span><span class="sxs-lookup"><span data-stu-id="0812f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0812f-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="0812f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0812f-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0812f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0812f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0812f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0812f-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="0812f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0812f-108">なし</span><span class="sxs-lookup"><span data-stu-id="0812f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0812f-109">定義</span><span class="sxs-lookup"><span data-stu-id="0812f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0812f-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0812f-110">Elements and attributes</span></span>

<span data-ttu-id="0812f-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0812f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0812f-112">子要素</span><span class="sxs-lookup"><span data-stu-id="0812f-112">Child elements</span></span>

<span data-ttu-id="0812f-113">なし。</span><span class="sxs-lookup"><span data-stu-id="0812f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0812f-114">属性</span><span class="sxs-lookup"><span data-stu-id="0812f-114">Attributes</span></span>

|<span data-ttu-id="0812f-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="0812f-115">**Attribute**</span></span>|<span data-ttu-id="0812f-116">**型**</span><span class="sxs-lookup"><span data-stu-id="0812f-116">**Type**</span></span>|<span data-ttu-id="0812f-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="0812f-117">**Required**</span></span>|<span data-ttu-id="0812f-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="0812f-118">**Description**</span></span>|<span data-ttu-id="0812f-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="0812f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0812f-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0812f-120">ColumnName</span></span>  <br/> |<span data-ttu-id="0812f-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0812f-121">xsd:string</span></span>  <br/> |<span data-ttu-id="0812f-122">必須</span><span class="sxs-lookup"><span data-stu-id="0812f-122">required</span></span>  <br/> ||<span data-ttu-id="0812f-123">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0812f-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0812f-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="0812f-124">ContextType</span></span>  <br/> |<span data-ttu-id="0812f-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0812f-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0812f-126">必須</span><span class="sxs-lookup"><span data-stu-id="0812f-126">required</span></span>  <br/> ||<span data-ttu-id="0812f-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0812f-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0812f-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="0812f-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="0812f-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0812f-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0812f-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="0812f-130">optional</span></span>  <br/> ||<span data-ttu-id="0812f-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0812f-131">Values of the xsd:string type.</span></span>  <br/> |
   

