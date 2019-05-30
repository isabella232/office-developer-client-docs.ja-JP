---
title: RowMap_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: 8564f5a063ac2365de50919168df0b84e8ae100a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538775"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="390d8-102">RowMap_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="390d8-102">RowMap_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="390d8-103">型情報</span><span class="sxs-lookup"><span data-stu-id="390d8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="390d8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="390d8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="390d8-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="390d8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="390d8-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="390d8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="390d8-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="390d8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="390d8-108">None</span><span class="sxs-lookup"><span data-stu-id="390d8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="390d8-109">定義</span><span class="sxs-lookup"><span data-stu-id="390d8-109">Definition</span></span>

```XML
      <xs:complexType name="RowMap_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="390d8-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="390d8-110">Elements and attributes</span></span>

<span data-ttu-id="390d8-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="390d8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="390d8-112">子要素</span><span class="sxs-lookup"><span data-stu-id="390d8-112">Child elements</span></span>

<span data-ttu-id="390d8-113">なし。</span><span class="sxs-lookup"><span data-stu-id="390d8-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="390d8-114">属性</span><span class="sxs-lookup"><span data-stu-id="390d8-114">Attributes</span></span>

|<span data-ttu-id="390d8-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="390d8-115">**Attribute**</span></span>|<span data-ttu-id="390d8-116">**型**</span><span class="sxs-lookup"><span data-stu-id="390d8-116">**Type**</span></span>|<span data-ttu-id="390d8-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="390d8-117">**Required**</span></span>|<span data-ttu-id="390d8-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="390d8-118">**Description**</span></span>|<span data-ttu-id="390d8-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="390d8-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="390d8-120">PageID</span><span class="sxs-lookup"><span data-stu-id="390d8-120">PageID</span></span>  <br/> |<span data-ttu-id="390d8-121">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="390d8-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="390d8-122">必須</span><span class="sxs-lookup"><span data-stu-id="390d8-122">required</span></span>  <br/> ||<span data-ttu-id="390d8-123">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="390d8-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="390d8-124">RowID</span><span class="sxs-lookup"><span data-stu-id="390d8-124">RowID</span></span>  <br/> |<span data-ttu-id="390d8-125">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="390d8-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="390d8-126">必須</span><span class="sxs-lookup"><span data-stu-id="390d8-126">required</span></span>  <br/> ||<span data-ttu-id="390d8-127">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="390d8-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="390d8-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="390d8-128">ShapeID</span></span>  <br/> |<span data-ttu-id="390d8-129">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="390d8-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="390d8-130">必須</span><span class="sxs-lookup"><span data-stu-id="390d8-130">required</span></span>  <br/> ||<span data-ttu-id="390d8-131">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="390d8-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

