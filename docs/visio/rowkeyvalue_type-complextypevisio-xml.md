---
title: RowKeyValue_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: e629a3a38927b7497d8d4f50299dc6be1b51c37b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541723"
---
# <a name="rowkeyvalue_type-complextype-visio-xml"></a><span data-ttu-id="ad3dc-102">RowKeyValue_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ad3dc-102">RowKeyValue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ad3dc-103">型情報</span><span class="sxs-lookup"><span data-stu-id="ad3dc-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad3dc-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad3dc-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ad3dc-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ad3dc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ad3dc-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ad3dc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ad3dc-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="ad3dc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ad3dc-108">なし</span><span class="sxs-lookup"><span data-stu-id="ad3dc-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad3dc-109">定義</span><span class="sxs-lookup"><span data-stu-id="ad3dc-109">Definition</span></span>

```XML
      <xs:complexType name="RowKeyValue_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Value"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad3dc-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ad3dc-110">Elements and attributes</span></span>

<span data-ttu-id="ad3dc-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad3dc-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ad3dc-112">子要素</span><span class="sxs-lookup"><span data-stu-id="ad3dc-112">Child elements</span></span>

<span data-ttu-id="ad3dc-113">なし。</span><span class="sxs-lookup"><span data-stu-id="ad3dc-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad3dc-114">属性</span><span class="sxs-lookup"><span data-stu-id="ad3dc-114">Attributes</span></span>

|<span data-ttu-id="ad3dc-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="ad3dc-115">**Attribute**</span></span>|<span data-ttu-id="ad3dc-116">**型**</span><span class="sxs-lookup"><span data-stu-id="ad3dc-116">**Type**</span></span>|<span data-ttu-id="ad3dc-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="ad3dc-117">**Required**</span></span>|<span data-ttu-id="ad3dc-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="ad3dc-118">**Description**</span></span>|<span data-ttu-id="ad3dc-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="ad3dc-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad3dc-120">RowID</span><span class="sxs-lookup"><span data-stu-id="ad3dc-120">RowID</span></span>  <br/> |<span data-ttu-id="ad3dc-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad3dc-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad3dc-122">必須</span><span class="sxs-lookup"><span data-stu-id="ad3dc-122">required</span></span>  <br/> ||<span data-ttu-id="ad3dc-123">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="ad3dc-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ad3dc-124">値</span><span class="sxs-lookup"><span data-stu-id="ad3dc-124">Value</span></span>  <br/> |<span data-ttu-id="ad3dc-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ad3dc-125">xsd:string</span></span>  <br/> |<span data-ttu-id="ad3dc-126">必須</span><span class="sxs-lookup"><span data-stu-id="ad3dc-126">required</span></span>  <br/> ||<span data-ttu-id="ad3dc-127">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="ad3dc-127">Values of the xsd:string type.</span></span>  <br/> |
   

