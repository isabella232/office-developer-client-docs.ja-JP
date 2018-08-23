---
title: RowKeyValue 要素 (PrimaryKey_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: レコード セットの個別の行の主キーの値を指定します。
ms.openlocfilehash: 3b91997b5fe8184eb89f8c53197a512d809171b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806317"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a><span data-ttu-id="6cd2d-103">RowKeyValue 要素 (PrimaryKey_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="6cd2d-103">RowKeyValue element (PrimaryKey_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6cd2d-104">レコード セットの個別の行の主キーの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6cd2d-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6cd2d-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="6cd2d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6cd2d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6cd2d-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="6cd2d-107">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6cd2d-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6cd2d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6cd2d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6cd2d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6cd2d-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6cd2d-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="6cd2d-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6cd2d-113">定義</span><span class="sxs-lookup"><span data-stu-id="6cd2d-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6cd2d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6cd2d-114">Elements and attributes</span></span>

<span data-ttu-id="6cd2d-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cd2d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6cd2d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="6cd2d-116">Parent elements</span></span>

|<span data-ttu-id="6cd2d-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-117">**Element**</span></span>|<span data-ttu-id="6cd2d-118">**型**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-118">**Type**</span></span>|<span data-ttu-id="6cd2d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6cd2d-120">主キー</span><span class="sxs-lookup"><span data-stu-id="6cd2d-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6cd2d-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="6cd2d-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6cd2d-122">レコード セットの主キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="6cd2d-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6cd2d-123">子要素</span><span class="sxs-lookup"><span data-stu-id="6cd2d-123">Child elements</span></span>

<span data-ttu-id="6cd2d-124">なし。</span><span class="sxs-lookup"><span data-stu-id="6cd2d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6cd2d-125">属性</span><span class="sxs-lookup"><span data-stu-id="6cd2d-125">Attributes</span></span>

|<span data-ttu-id="6cd2d-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-126">**Attribute**</span></span>|<span data-ttu-id="6cd2d-127">**型**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-127">**Type**</span></span>|<span data-ttu-id="6cd2d-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-128">**Required**</span></span>|<span data-ttu-id="6cd2d-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-129">**Description**</span></span>|<span data-ttu-id="6cd2d-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="6cd2d-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6cd2d-131">RowID</span><span class="sxs-lookup"><span data-stu-id="6cd2d-131">RowID</span></span>  <br/> |<span data-ttu-id="6cd2d-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6cd2d-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6cd2d-133">必須</span><span class="sxs-lookup"><span data-stu-id="6cd2d-133">required</span></span>  <br/> |<span data-ttu-id="6cd2d-134">レコード セットの行を識別する一意の値です。</span><span class="sxs-lookup"><span data-stu-id="6cd2d-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="6cd2d-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6cd2d-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6cd2d-136">値</span><span class="sxs-lookup"><span data-stu-id="6cd2d-136">Value</span></span>  <br/> |<span data-ttu-id="6cd2d-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6cd2d-137">xsd:string</span></span>  <br/> |<span data-ttu-id="6cd2d-138">必須</span><span class="sxs-lookup"><span data-stu-id="6cd2d-138">required</span></span>  <br/> |<span data-ttu-id="6cd2d-139">レコード セットのこの行の主キーの値。</span><span class="sxs-lookup"><span data-stu-id="6cd2d-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="6cd2d-140">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6cd2d-140">Values of the xsd:string type.</span></span>  <br/> |
   

