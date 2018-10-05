---
title: RowMap_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: bdc76f35cf2824d5159e945bce7e9dd2a8abe2bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401000"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="88130-102">RowMap_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="88130-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="88130-103">型情報</span><span class="sxs-lookup"><span data-stu-id="88130-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88130-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="88130-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="88130-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="88130-105">**Schema file**</span></span> <br/> |<span data-ttu-id="88130-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="88130-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="88130-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="88130-107">**Extension base**</span></span> <br/> |<span data-ttu-id="88130-108">なし</span><span class="sxs-lookup"><span data-stu-id="88130-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88130-109">定義</span><span class="sxs-lookup"><span data-stu-id="88130-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="88130-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="88130-110">Elements and attributes</span></span>

<span data-ttu-id="88130-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88130-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="88130-112">子要素</span><span class="sxs-lookup"><span data-stu-id="88130-112">Child elements</span></span>

<span data-ttu-id="88130-113">なし。</span><span class="sxs-lookup"><span data-stu-id="88130-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88130-114">属性</span><span class="sxs-lookup"><span data-stu-id="88130-114">Attributes</span></span>

|<span data-ttu-id="88130-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="88130-115">**Attribute**</span></span>|<span data-ttu-id="88130-116">**型**</span><span class="sxs-lookup"><span data-stu-id="88130-116">**Type**</span></span>|<span data-ttu-id="88130-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="88130-117">**Required**</span></span>|<span data-ttu-id="88130-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="88130-118">**Description**</span></span>|<span data-ttu-id="88130-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="88130-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="88130-120">PageID</span><span class="sxs-lookup"><span data-stu-id="88130-120">PageID</span></span>  <br/> |<span data-ttu-id="88130-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88130-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88130-122">必須</span><span class="sxs-lookup"><span data-stu-id="88130-122">required</span></span>  <br/> ||<span data-ttu-id="88130-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88130-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88130-124">RowID</span><span class="sxs-lookup"><span data-stu-id="88130-124">RowID</span></span>  <br/> |<span data-ttu-id="88130-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88130-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88130-126">必須</span><span class="sxs-lookup"><span data-stu-id="88130-126">required</span></span>  <br/> ||<span data-ttu-id="88130-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88130-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88130-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="88130-128">ShapeID</span></span>  <br/> |<span data-ttu-id="88130-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88130-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88130-130">必須</span><span class="sxs-lookup"><span data-stu-id="88130-130">required</span></span>  <br/> ||<span data-ttu-id="88130-131">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88130-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

