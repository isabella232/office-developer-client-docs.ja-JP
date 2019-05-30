---
title: ColorEntry_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: f5ada3fef8d50c2e53f63c797601980f88349868
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540148"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="7669e-102">ColorEntry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7669e-102">ColorEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7669e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="7669e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7669e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7669e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7669e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="7669e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7669e-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="7669e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7669e-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="7669e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7669e-108">None</span><span class="sxs-lookup"><span data-stu-id="7669e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7669e-109">定義</span><span class="sxs-lookup"><span data-stu-id="7669e-109">Definition</span></span>

```XML
      <xs:complexType name="ColorEntry_Type">
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RGB"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7669e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="7669e-110">Elements and attributes</span></span>

<span data-ttu-id="7669e-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7669e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7669e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="7669e-112">Child elements</span></span>

<span data-ttu-id="7669e-113">なし。</span><span class="sxs-lookup"><span data-stu-id="7669e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7669e-114">属性</span><span class="sxs-lookup"><span data-stu-id="7669e-114">Attributes</span></span>

|<span data-ttu-id="7669e-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="7669e-115">**Attribute**</span></span>|<span data-ttu-id="7669e-116">**型**</span><span class="sxs-lookup"><span data-stu-id="7669e-116">**Type**</span></span>|<span data-ttu-id="7669e-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="7669e-117">**Required**</span></span>|<span data-ttu-id="7669e-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="7669e-118">**Description**</span></span>|<span data-ttu-id="7669e-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="7669e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7669e-120">IX</span><span class="sxs-lookup"><span data-stu-id="7669e-120">IX</span></span>  <br/> |<span data-ttu-id="7669e-121">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="7669e-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7669e-122">必須</span><span class="sxs-lookup"><span data-stu-id="7669e-122">required</span></span>  <br/> ||<span data-ttu-id="7669e-123">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="7669e-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7669e-124">RGB</span><span class="sxs-lookup"><span data-stu-id="7669e-124">RGB</span></span>  <br/> |<span data-ttu-id="7669e-125">xsd: string</span><span class="sxs-lookup"><span data-stu-id="7669e-125">xsd:string</span></span>  <br/> |<span data-ttu-id="7669e-126">必須</span><span class="sxs-lookup"><span data-stu-id="7669e-126">required</span></span>  <br/> ||<span data-ttu-id="7669e-127">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="7669e-127">Values of the xsd:string type.</span></span>  <br/> |
   

