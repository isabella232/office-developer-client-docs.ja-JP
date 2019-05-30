---
title: RefreshConflict_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 7b52bc87af213e9c26f4bc359adf6cf900b34957
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542829"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="25700-102">RefreshConflict_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="25700-102">RefreshConflict_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="25700-103">型情報</span><span class="sxs-lookup"><span data-stu-id="25700-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25700-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="25700-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="25700-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="25700-105">**Schema file**</span></span> <br/> |<span data-ttu-id="25700-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="25700-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="25700-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="25700-107">**Extension base**</span></span> <br/> |<span data-ttu-id="25700-108">None</span><span class="sxs-lookup"><span data-stu-id="25700-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="25700-109">定義</span><span class="sxs-lookup"><span data-stu-id="25700-109">Definition</span></span>

```XML
      <xs:complexType name="RefreshConflict_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="25700-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="25700-110">Elements and attributes</span></span>

<span data-ttu-id="25700-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="25700-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="25700-112">子要素</span><span class="sxs-lookup"><span data-stu-id="25700-112">Child elements</span></span>

<span data-ttu-id="25700-113">なし。</span><span class="sxs-lookup"><span data-stu-id="25700-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25700-114">属性</span><span class="sxs-lookup"><span data-stu-id="25700-114">Attributes</span></span>

|<span data-ttu-id="25700-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="25700-115">**Attribute**</span></span>|<span data-ttu-id="25700-116">**型**</span><span class="sxs-lookup"><span data-stu-id="25700-116">**Type**</span></span>|<span data-ttu-id="25700-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="25700-117">**Required**</span></span>|<span data-ttu-id="25700-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="25700-118">**Description**</span></span>|<span data-ttu-id="25700-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="25700-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="25700-120">PageID</span><span class="sxs-lookup"><span data-stu-id="25700-120">PageID</span></span>  <br/> |<span data-ttu-id="25700-121">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="25700-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="25700-122">必須</span><span class="sxs-lookup"><span data-stu-id="25700-122">required</span></span>  <br/> ||<span data-ttu-id="25700-123">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="25700-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="25700-124">RowID</span><span class="sxs-lookup"><span data-stu-id="25700-124">RowID</span></span>  <br/> |<span data-ttu-id="25700-125">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="25700-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="25700-126">必須</span><span class="sxs-lookup"><span data-stu-id="25700-126">required</span></span>  <br/> ||<span data-ttu-id="25700-127">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="25700-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="25700-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="25700-128">ShapeID</span></span>  <br/> |<span data-ttu-id="25700-129">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="25700-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="25700-130">必須</span><span class="sxs-lookup"><span data-stu-id="25700-130">required</span></span>  <br/> ||<span data-ttu-id="25700-131">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="25700-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

