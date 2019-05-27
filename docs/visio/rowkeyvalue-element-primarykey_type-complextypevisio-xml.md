---
title: RowKeyValue 要素 (PrimaryKey_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: レコードセットの各行の主キーの値を指定します。
ms.openlocfilehash: 12d60bb0ccccdcd8c1790678cae4ad1e887e73b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283504"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a><span data-ttu-id="94914-103">RowKeyValue 要素 (PrimaryKey_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="94914-103">RowKeyValue element (PrimaryKey_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="94914-104">レコードセットの各行の主キーの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="94914-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94914-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="94914-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94914-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="94914-106">**Element type**</span></span> <br/> |[<span data-ttu-id="94914-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="94914-107">RowKeyValue_Type complexType</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="94914-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="94914-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="94914-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="94914-109">**Schema file**</span></span> <br/> |<span data-ttu-id="94914-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="94914-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="94914-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="94914-111">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="94914-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="94914-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="94914-113">定義</span><span class="sxs-lookup"><span data-stu-id="94914-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="94914-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="94914-114">Elements and attributes</span></span>

<span data-ttu-id="94914-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="94914-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="94914-116">親要素</span><span class="sxs-lookup"><span data-stu-id="94914-116">Parent elements</span></span>

|<span data-ttu-id="94914-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="94914-117">**Element**</span></span>|<span data-ttu-id="94914-118">**型**</span><span class="sxs-lookup"><span data-stu-id="94914-118">**Type**</span></span>|<span data-ttu-id="94914-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="94914-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="94914-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="94914-120">PrimaryKey element</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="94914-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="94914-121">PrimaryKey_Type complexType</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="94914-122">レコードセットの主キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="94914-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="94914-123">子要素</span><span class="sxs-lookup"><span data-stu-id="94914-123">Child elements</span></span>

<span data-ttu-id="94914-124">なし。</span><span class="sxs-lookup"><span data-stu-id="94914-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94914-125">属性</span><span class="sxs-lookup"><span data-stu-id="94914-125">Attributes</span></span>

|<span data-ttu-id="94914-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="94914-126">**Attribute**</span></span>|<span data-ttu-id="94914-127">**型**</span><span class="sxs-lookup"><span data-stu-id="94914-127">**Type**</span></span>|<span data-ttu-id="94914-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="94914-128">**Required**</span></span>|<span data-ttu-id="94914-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="94914-129">**Description**</span></span>|<span data-ttu-id="94914-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="94914-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="94914-131">RowID</span><span class="sxs-lookup"><span data-stu-id="94914-131">RowID</span></span>  <br/> |<span data-ttu-id="94914-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="94914-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="94914-133">必須</span><span class="sxs-lookup"><span data-stu-id="94914-133">required</span></span>  <br/> |<span data-ttu-id="94914-134">レコードセットの行を識別する一意の値です。</span><span class="sxs-lookup"><span data-stu-id="94914-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="94914-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="94914-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="94914-136">値</span><span class="sxs-lookup"><span data-stu-id="94914-136">Value</span></span>  <br/> |<span data-ttu-id="94914-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="94914-137">xsd:string</span></span>  <br/> |<span data-ttu-id="94914-138">必須</span><span class="sxs-lookup"><span data-stu-id="94914-138">required</span></span>  <br/> |<span data-ttu-id="94914-139">レコードセットのこの行の主キーの値です。</span><span class="sxs-lookup"><span data-stu-id="94914-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="94914-140">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="94914-140">Values of the xsd:string type.</span></span>  <br/> |
   

