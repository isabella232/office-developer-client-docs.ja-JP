---
title: RefreshConflict_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 25c83a8168744820fa8b570dc37bda0547ab4ea0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346481"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="34c92-102">RefreshConflict_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="34c92-102">RefreshConflict_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="34c92-103">型情報</span><span class="sxs-lookup"><span data-stu-id="34c92-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34c92-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="34c92-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="34c92-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="34c92-105">**Schema file**</span></span> <br/> |<span data-ttu-id="34c92-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="34c92-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="34c92-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="34c92-107">**Extension base**</span></span> <br/> |<span data-ttu-id="34c92-108">なし</span><span class="sxs-lookup"><span data-stu-id="34c92-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="34c92-109">定義</span><span class="sxs-lookup"><span data-stu-id="34c92-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="34c92-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="34c92-110">Elements and attributes</span></span>

<span data-ttu-id="34c92-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="34c92-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="34c92-112">子要素</span><span class="sxs-lookup"><span data-stu-id="34c92-112">Child elements</span></span>

<span data-ttu-id="34c92-113">なし。</span><span class="sxs-lookup"><span data-stu-id="34c92-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34c92-114">属性</span><span class="sxs-lookup"><span data-stu-id="34c92-114">Attributes</span></span>

|<span data-ttu-id="34c92-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="34c92-115">**Attribute**</span></span>|<span data-ttu-id="34c92-116">**型**</span><span class="sxs-lookup"><span data-stu-id="34c92-116">**Type**</span></span>|<span data-ttu-id="34c92-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="34c92-117">**Required**</span></span>|<span data-ttu-id="34c92-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="34c92-118">**Description**</span></span>|<span data-ttu-id="34c92-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="34c92-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="34c92-120">PageID</span><span class="sxs-lookup"><span data-stu-id="34c92-120">PageID</span></span>  <br/> |<span data-ttu-id="34c92-121">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="34c92-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="34c92-122">必須</span><span class="sxs-lookup"><span data-stu-id="34c92-122">required</span></span>  <br/> ||<span data-ttu-id="34c92-123">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="34c92-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="34c92-124">RowID</span><span class="sxs-lookup"><span data-stu-id="34c92-124">RowID</span></span>  <br/> |<span data-ttu-id="34c92-125">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="34c92-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="34c92-126">必須</span><span class="sxs-lookup"><span data-stu-id="34c92-126">required</span></span>  <br/> ||<span data-ttu-id="34c92-127">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="34c92-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="34c92-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="34c92-128">ShapeID</span></span>  <br/> |<span data-ttu-id="34c92-129">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="34c92-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="34c92-130">必須</span><span class="sxs-lookup"><span data-stu-id="34c92-130">required</span></span>  <br/> ||<span data-ttu-id="34c92-131">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="34c92-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

