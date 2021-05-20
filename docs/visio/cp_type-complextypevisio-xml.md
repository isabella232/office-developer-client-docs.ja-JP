---
title: cp_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e69b0db-f705-61f0-e6ab-811b2acc358e
ms.openlocfilehash: afbba1f5b6e809d1f7ac673c6f77e762aa45ac5b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540540"
---
# <a name="cp_type-complextype-visio-xml"></a><span data-ttu-id="bafe7-102">cp_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bafe7-102">cp_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="bafe7-103">型情報</span><span class="sxs-lookup"><span data-stu-id="bafe7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bafe7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bafe7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bafe7-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="bafe7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bafe7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bafe7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bafe7-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="bafe7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bafe7-108">なし</span><span class="sxs-lookup"><span data-stu-id="bafe7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bafe7-109">定義</span><span class="sxs-lookup"><span data-stu-id="bafe7-109">Definition</span></span>

```XML
      <xs:complexType name="cp_Type">
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bafe7-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="bafe7-110">Elements and attributes</span></span>

<span data-ttu-id="bafe7-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bafe7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bafe7-112">子要素</span><span class="sxs-lookup"><span data-stu-id="bafe7-112">Child elements</span></span>

<span data-ttu-id="bafe7-113">なし。</span><span class="sxs-lookup"><span data-stu-id="bafe7-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bafe7-114">属性</span><span class="sxs-lookup"><span data-stu-id="bafe7-114">Attributes</span></span>

|<span data-ttu-id="bafe7-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="bafe7-115">**Attribute**</span></span>|<span data-ttu-id="bafe7-116">**型**</span><span class="sxs-lookup"><span data-stu-id="bafe7-116">**Type**</span></span>|<span data-ttu-id="bafe7-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="bafe7-117">**Required**</span></span>|<span data-ttu-id="bafe7-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="bafe7-118">**Description**</span></span>|<span data-ttu-id="bafe7-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="bafe7-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bafe7-120">IX</span><span class="sxs-lookup"><span data-stu-id="bafe7-120">IX</span></span>  <br/> |<span data-ttu-id="bafe7-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bafe7-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bafe7-122">必須</span><span class="sxs-lookup"><span data-stu-id="bafe7-122">required</span></span>  <br/> ||<span data-ttu-id="bafe7-123">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="bafe7-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

