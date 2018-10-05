---
title: RefreshConflict_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 25c83a8168744820fa8b570dc37bda0547ab4ea0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383171"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="0b35a-102">RefreshConflict_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="0b35a-102">RefreshConflict_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0b35a-103">型情報</span><span class="sxs-lookup"><span data-stu-id="0b35a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b35a-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="0b35a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0b35a-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0b35a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0b35a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0b35a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0b35a-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="0b35a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0b35a-108">なし</span><span class="sxs-lookup"><span data-stu-id="0b35a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0b35a-109">定義</span><span class="sxs-lookup"><span data-stu-id="0b35a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0b35a-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0b35a-110">Elements and attributes</span></span>

<span data-ttu-id="0b35a-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b35a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0b35a-112">子要素</span><span class="sxs-lookup"><span data-stu-id="0b35a-112">Child elements</span></span>

<span data-ttu-id="0b35a-113">なし。</span><span class="sxs-lookup"><span data-stu-id="0b35a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b35a-114">属性</span><span class="sxs-lookup"><span data-stu-id="0b35a-114">Attributes</span></span>

|<span data-ttu-id="0b35a-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="0b35a-115">**Attribute**</span></span>|<span data-ttu-id="0b35a-116">**型**</span><span class="sxs-lookup"><span data-stu-id="0b35a-116">**Type**</span></span>|<span data-ttu-id="0b35a-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="0b35a-117">**Required**</span></span>|<span data-ttu-id="0b35a-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="0b35a-118">**Description**</span></span>|<span data-ttu-id="0b35a-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="0b35a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0b35a-120">PageID</span><span class="sxs-lookup"><span data-stu-id="0b35a-120">PageID</span></span>  <br/> |<span data-ttu-id="0b35a-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0b35a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0b35a-122">必須</span><span class="sxs-lookup"><span data-stu-id="0b35a-122">required</span></span>  <br/> ||<span data-ttu-id="0b35a-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0b35a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0b35a-124">RowID</span><span class="sxs-lookup"><span data-stu-id="0b35a-124">RowID</span></span>  <br/> |<span data-ttu-id="0b35a-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0b35a-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0b35a-126">必須</span><span class="sxs-lookup"><span data-stu-id="0b35a-126">required</span></span>  <br/> ||<span data-ttu-id="0b35a-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0b35a-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0b35a-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="0b35a-128">ShapeID</span></span>  <br/> |<span data-ttu-id="0b35a-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0b35a-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0b35a-130">必須</span><span class="sxs-lookup"><span data-stu-id="0b35a-130">required</span></span>  <br/> ||<span data-ttu-id="0b35a-131">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0b35a-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

