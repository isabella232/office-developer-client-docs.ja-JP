---
title: rowkeyvalue 要素 (PrimaryKey_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: recordset の個々の行の主キーの値を指定します。
ms.openlocfilehash: 12d60bb0ccccdcd8c1790678cae4ad1e887e73b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283504"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a><span data-ttu-id="01226-103">rowkeyvalue 要素 (PrimaryKey_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="01226-103">RowKeyValue element (PrimaryKey_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="01226-104">recordset の個々の行の主キーの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="01226-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01226-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="01226-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01226-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="01226-106">**Element type**</span></span> <br/> |[<span data-ttu-id="01226-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="01226-107">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="01226-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="01226-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="01226-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="01226-109">**Schema file**</span></span> <br/> |<span data-ttu-id="01226-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="01226-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="01226-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="01226-111">**Document parts**</span></span> <br/> |<span data-ttu-id="01226-112">recordsets</span><span class="sxs-lookup"><span data-stu-id="01226-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="01226-113">定義</span><span class="sxs-lookup"><span data-stu-id="01226-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="01226-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="01226-114">Elements and attributes</span></span>

<span data-ttu-id="01226-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="01226-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="01226-116">親要素</span><span class="sxs-lookup"><span data-stu-id="01226-116">Parent elements</span></span>

|<span data-ttu-id="01226-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="01226-117">**Element**</span></span>|<span data-ttu-id="01226-118">**型**</span><span class="sxs-lookup"><span data-stu-id="01226-118">**Type**</span></span>|<span data-ttu-id="01226-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="01226-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="01226-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="01226-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="01226-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="01226-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01226-122">recordset の主キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="01226-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="01226-123">子要素</span><span class="sxs-lookup"><span data-stu-id="01226-123">Child elements</span></span>

<span data-ttu-id="01226-124">なし。</span><span class="sxs-lookup"><span data-stu-id="01226-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01226-125">属性</span><span class="sxs-lookup"><span data-stu-id="01226-125">Attributes</span></span>

|<span data-ttu-id="01226-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="01226-126">**Attribute**</span></span>|<span data-ttu-id="01226-127">**型**</span><span class="sxs-lookup"><span data-stu-id="01226-127">**Type**</span></span>|<span data-ttu-id="01226-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="01226-128">**Required**</span></span>|<span data-ttu-id="01226-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="01226-129">**Description**</span></span>|<span data-ttu-id="01226-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="01226-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="01226-131">RowID</span><span class="sxs-lookup"><span data-stu-id="01226-131">RowID</span></span>  <br/> |<span data-ttu-id="01226-132">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="01226-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="01226-133">必須</span><span class="sxs-lookup"><span data-stu-id="01226-133">required</span></span>  <br/> |<span data-ttu-id="01226-134">recordset の行を識別する一意の値。</span><span class="sxs-lookup"><span data-stu-id="01226-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="01226-135">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="01226-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="01226-136">値</span><span class="sxs-lookup"><span data-stu-id="01226-136">Value</span></span>  <br/> |<span data-ttu-id="01226-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="01226-137">xsd:string</span></span>  <br/> |<span data-ttu-id="01226-138">必須</span><span class="sxs-lookup"><span data-stu-id="01226-138">required</span></span>  <br/> |<span data-ttu-id="01226-139">recordset のこの行の主キーの値。</span><span class="sxs-lookup"><span data-stu-id="01226-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="01226-140">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="01226-140">Values of the xsd:string type.</span></span>  <br/> |
   

