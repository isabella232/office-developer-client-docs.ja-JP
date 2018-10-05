---
title: RowKeyValue 要素 (PrimaryKey_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: レコード セットの個別の行の主キーの値を指定します。
ms.openlocfilehash: 12d60bb0ccccdcd8c1790678cae4ad1e887e73b6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396724"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a><span data-ttu-id="185ae-103">RowKeyValue 要素 (PrimaryKey_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="185ae-103">RowKeyValue element (PrimaryKey_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="185ae-104">レコード セットの個別の行の主キーの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="185ae-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="185ae-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="185ae-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="185ae-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="185ae-106">**Element type**</span></span> <br/> |[<span data-ttu-id="185ae-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="185ae-107">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="185ae-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="185ae-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="185ae-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="185ae-109">**Schema file**</span></span> <br/> |<span data-ttu-id="185ae-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="185ae-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="185ae-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="185ae-111">**Document parts**</span></span> <br/> |<span data-ttu-id="185ae-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="185ae-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="185ae-113">定義</span><span class="sxs-lookup"><span data-stu-id="185ae-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="185ae-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="185ae-114">Elements and attributes</span></span>

<span data-ttu-id="185ae-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="185ae-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="185ae-116">親要素</span><span class="sxs-lookup"><span data-stu-id="185ae-116">Parent elements</span></span>

|<span data-ttu-id="185ae-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="185ae-117">**Element**</span></span>|<span data-ttu-id="185ae-118">**型**</span><span class="sxs-lookup"><span data-stu-id="185ae-118">**Type**</span></span>|<span data-ttu-id="185ae-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="185ae-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="185ae-120">主キー</span><span class="sxs-lookup"><span data-stu-id="185ae-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="185ae-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="185ae-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="185ae-122">レコード セットの主キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="185ae-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="185ae-123">子要素</span><span class="sxs-lookup"><span data-stu-id="185ae-123">Child elements</span></span>

<span data-ttu-id="185ae-124">なし。</span><span class="sxs-lookup"><span data-stu-id="185ae-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="185ae-125">属性</span><span class="sxs-lookup"><span data-stu-id="185ae-125">Attributes</span></span>

|<span data-ttu-id="185ae-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="185ae-126">**Attribute**</span></span>|<span data-ttu-id="185ae-127">**型**</span><span class="sxs-lookup"><span data-stu-id="185ae-127">**Type**</span></span>|<span data-ttu-id="185ae-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="185ae-128">**Required**</span></span>|<span data-ttu-id="185ae-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="185ae-129">**Description**</span></span>|<span data-ttu-id="185ae-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="185ae-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="185ae-131">RowID</span><span class="sxs-lookup"><span data-stu-id="185ae-131">RowID</span></span>  <br/> |<span data-ttu-id="185ae-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="185ae-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="185ae-133">必須</span><span class="sxs-lookup"><span data-stu-id="185ae-133">required</span></span>  <br/> |<span data-ttu-id="185ae-134">レコード セットの行を識別する一意の値です。</span><span class="sxs-lookup"><span data-stu-id="185ae-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="185ae-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="185ae-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="185ae-136">値</span><span class="sxs-lookup"><span data-stu-id="185ae-136">Value</span></span>  <br/> |<span data-ttu-id="185ae-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="185ae-137">xsd:string</span></span>  <br/> |<span data-ttu-id="185ae-138">必須</span><span class="sxs-lookup"><span data-stu-id="185ae-138">required</span></span>  <br/> |<span data-ttu-id="185ae-139">レコード セットのこの行の主キーの値。</span><span class="sxs-lookup"><span data-stu-id="185ae-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="185ae-140">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="185ae-140">Values of the xsd:string type.</span></span>  <br/> |
   

