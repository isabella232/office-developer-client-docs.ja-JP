---
title: RefreshConflict_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 44910cd305b484771ca3d4f4d49ef8a09a6fc2dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806178"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="54196-102">RefreshConflict_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="54196-102">RefreshConflict_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="54196-103">型情報</span><span class="sxs-lookup"><span data-stu-id="54196-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54196-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="54196-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="54196-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="54196-105">**Schema file**</span></span> <br/> |<span data-ttu-id="54196-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="54196-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="54196-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="54196-107">**Extension base**</span></span> <br/> |<span data-ttu-id="54196-108">なし</span><span class="sxs-lookup"><span data-stu-id="54196-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="54196-109">定義</span><span class="sxs-lookup"><span data-stu-id="54196-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="54196-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="54196-110">Elements and attributes</span></span>

<span data-ttu-id="54196-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="54196-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="54196-112">子要素</span><span class="sxs-lookup"><span data-stu-id="54196-112">Child elements</span></span>

<span data-ttu-id="54196-113">なし。</span><span class="sxs-lookup"><span data-stu-id="54196-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54196-114">属性</span><span class="sxs-lookup"><span data-stu-id="54196-114">Attributes</span></span>

|<span data-ttu-id="54196-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="54196-115">**Attribute**</span></span>|<span data-ttu-id="54196-116">**型**</span><span class="sxs-lookup"><span data-stu-id="54196-116">**Type**</span></span>|<span data-ttu-id="54196-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="54196-117">**Required**</span></span>|<span data-ttu-id="54196-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="54196-118">**Description**</span></span>|<span data-ttu-id="54196-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="54196-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="54196-120">PageID</span><span class="sxs-lookup"><span data-stu-id="54196-120">PageID</span></span>  <br/> |<span data-ttu-id="54196-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="54196-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="54196-122">必須</span><span class="sxs-lookup"><span data-stu-id="54196-122">required</span></span>  <br/> ||<span data-ttu-id="54196-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="54196-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="54196-124">RowID</span><span class="sxs-lookup"><span data-stu-id="54196-124">RowID</span></span>  <br/> |<span data-ttu-id="54196-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="54196-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="54196-126">必須</span><span class="sxs-lookup"><span data-stu-id="54196-126">required</span></span>  <br/> ||<span data-ttu-id="54196-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="54196-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="54196-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="54196-128">ShapeID</span></span>  <br/> |<span data-ttu-id="54196-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="54196-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="54196-130">必須</span><span class="sxs-lookup"><span data-stu-id="54196-130">required</span></span>  <br/> ||<span data-ttu-id="54196-131">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="54196-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

