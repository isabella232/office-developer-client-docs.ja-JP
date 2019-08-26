---
title: RowKeyValue 要素 (PrimaryKey_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: レコードセットの各行の主キーの値を指定します。
ms.openlocfilehash: b21f479a9c0404dc8a3b737208e4d0d634b556f4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538131"
---
# <a name="rowkeyvalue-element-primarykey_type-complextype-visio-xml"></a><span data-ttu-id="ceda7-103">RowKeyValue 要素 (PrimaryKey_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ceda7-103">RowKeyValue element (PrimaryKey_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ceda7-104">レコードセットの各行の主キーの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ceda7-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ceda7-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="ceda7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ceda7-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="ceda7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ceda7-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="ceda7-107">RowKeyValue_Type complexType</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ceda7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ceda7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ceda7-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ceda7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ceda7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ceda7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ceda7-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="ceda7-111">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="ceda7-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="ceda7-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ceda7-113">定義</span><span class="sxs-lookup"><span data-stu-id="ceda7-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ceda7-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ceda7-114">Elements and attributes</span></span>

<span data-ttu-id="ceda7-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ceda7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ceda7-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ceda7-116">Parent elements</span></span>

|<span data-ttu-id="ceda7-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="ceda7-117">**Element**</span></span>|<span data-ttu-id="ceda7-118">**型**</span><span class="sxs-lookup"><span data-stu-id="ceda7-118">**Type**</span></span>|<span data-ttu-id="ceda7-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="ceda7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ceda7-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ceda7-120">PrimaryKey element</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ceda7-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="ceda7-121">PrimaryKey_Type complexType</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ceda7-122">レコードセットの主キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="ceda7-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ceda7-123">子要素</span><span class="sxs-lookup"><span data-stu-id="ceda7-123">Child elements</span></span>

<span data-ttu-id="ceda7-124">なし。</span><span class="sxs-lookup"><span data-stu-id="ceda7-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ceda7-125">属性</span><span class="sxs-lookup"><span data-stu-id="ceda7-125">Attributes</span></span>

|<span data-ttu-id="ceda7-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="ceda7-126">**Attribute**</span></span>|<span data-ttu-id="ceda7-127">**型**</span><span class="sxs-lookup"><span data-stu-id="ceda7-127">**Type**</span></span>|<span data-ttu-id="ceda7-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="ceda7-128">**Required**</span></span>|<span data-ttu-id="ceda7-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="ceda7-129">**Description**</span></span>|<span data-ttu-id="ceda7-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="ceda7-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ceda7-131">RowID</span><span class="sxs-lookup"><span data-stu-id="ceda7-131">RowID</span></span>  <br/> |<span data-ttu-id="ceda7-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ceda7-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ceda7-133">必須</span><span class="sxs-lookup"><span data-stu-id="ceda7-133">required</span></span>  <br/> |<span data-ttu-id="ceda7-134">レコードセットの行を識別する一意の値です。</span><span class="sxs-lookup"><span data-stu-id="ceda7-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="ceda7-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="ceda7-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ceda7-136">値</span><span class="sxs-lookup"><span data-stu-id="ceda7-136">Value</span></span>  <br/> |<span data-ttu-id="ceda7-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ceda7-137">xsd:string</span></span>  <br/> |<span data-ttu-id="ceda7-138">必須</span><span class="sxs-lookup"><span data-stu-id="ceda7-138">required</span></span>  <br/> |<span data-ttu-id="ceda7-139">レコードセットのこの行の主キーの値です。</span><span class="sxs-lookup"><span data-stu-id="ceda7-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="ceda7-140">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="ceda7-140">Values of the xsd:string type.</span></span>  <br/> |
   

