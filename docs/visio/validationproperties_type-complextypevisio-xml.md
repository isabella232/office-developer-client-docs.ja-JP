---
title: ValidationProperties_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: d83a1ce8e7ad89155726200de2950da755e5d3db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538516"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="9ceda-102">ValidationProperties_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9ceda-102">ValidationProperties_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9ceda-103">型情報</span><span class="sxs-lookup"><span data-stu-id="9ceda-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ceda-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9ceda-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9ceda-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9ceda-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9ceda-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="9ceda-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9ceda-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="9ceda-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9ceda-108">None</span><span class="sxs-lookup"><span data-stu-id="9ceda-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9ceda-109">定義</span><span class="sxs-lookup"><span data-stu-id="9ceda-109">Definition</span></span>

```XML
      <xs:complexType name="ValidationProperties_Type">
    <xs:attribute name="LastValidated"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="ShowIgnored"
  type="xsd:boolean"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9ceda-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9ceda-110">Elements and attributes</span></span>

<span data-ttu-id="9ceda-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ceda-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9ceda-112">子要素</span><span class="sxs-lookup"><span data-stu-id="9ceda-112">Child elements</span></span>

<span data-ttu-id="9ceda-113">なし。</span><span class="sxs-lookup"><span data-stu-id="9ceda-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ceda-114">属性</span><span class="sxs-lookup"><span data-stu-id="9ceda-114">Attributes</span></span>

|<span data-ttu-id="9ceda-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="9ceda-115">**Attribute**</span></span>|<span data-ttu-id="9ceda-116">**型**</span><span class="sxs-lookup"><span data-stu-id="9ceda-116">**Type**</span></span>|<span data-ttu-id="9ceda-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="9ceda-117">**Required**</span></span>|<span data-ttu-id="9ceda-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="9ceda-118">**Description**</span></span>|<span data-ttu-id="9ceda-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="9ceda-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9ceda-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="9ceda-120">LastValidated</span></span>  <br/> |<span data-ttu-id="9ceda-121">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="9ceda-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="9ceda-122">必須</span><span class="sxs-lookup"><span data-stu-id="9ceda-122">required</span></span>  <br/> ||<span data-ttu-id="9ceda-123">Xsd: dateTime 型の値。</span><span class="sxs-lookup"><span data-stu-id="9ceda-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="9ceda-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="9ceda-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="9ceda-125">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="9ceda-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9ceda-126">必須</span><span class="sxs-lookup"><span data-stu-id="9ceda-126">required</span></span>  <br/> ||<span data-ttu-id="9ceda-127">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="9ceda-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

