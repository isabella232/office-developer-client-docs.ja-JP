---
title: 主キーの要素 (DataRecordSet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: データ レコード セット内の 1 つまたは複数の主キー列を識別します。
ms.openlocfilehash: c001c343c33e65c3990744b885f1c345575b1ab3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396359"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="b8751-103">主キーの要素 (DataRecordSet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="b8751-103">PrimaryKey element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b8751-104">データ レコード セット内の 1 つまたは複数の主キー列を識別します。</span><span class="sxs-lookup"><span data-stu-id="b8751-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8751-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="b8751-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8751-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="b8751-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b8751-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="b8751-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b8751-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="b8751-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b8751-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b8751-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b8751-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b8751-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b8751-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="b8751-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b8751-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="b8751-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b8751-113">定義</span><span class="sxs-lookup"><span data-stu-id="b8751-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b8751-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b8751-114">Elements and attributes</span></span>

<span data-ttu-id="b8751-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8751-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b8751-116">親要素</span><span class="sxs-lookup"><span data-stu-id="b8751-116">Parent elements</span></span>

|<span data-ttu-id="b8751-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="b8751-117">**Element**</span></span>|<span data-ttu-id="b8751-118">**型**</span><span class="sxs-lookup"><span data-stu-id="b8751-118">**Type**</span></span>|<span data-ttu-id="b8751-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="b8751-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b8751-120">データ レコード セット</span><span class="sxs-lookup"><span data-stu-id="b8751-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b8751-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="b8751-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b8751-122">Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。</span><span class="sxs-lookup"><span data-stu-id="b8751-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b8751-123">子要素</span><span class="sxs-lookup"><span data-stu-id="b8751-123">Child elements</span></span>

|<span data-ttu-id="b8751-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="b8751-124">**Element**</span></span>|<span data-ttu-id="b8751-125">**型**</span><span class="sxs-lookup"><span data-stu-id="b8751-125">**Type**</span></span>|<span data-ttu-id="b8751-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="b8751-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b8751-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="b8751-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b8751-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="b8751-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b8751-129">このコンポーネントのレコード セットの個別の行の主キーの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b8751-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="b8751-130">この子要素の 1 つ以上の出現が必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8751-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b8751-131">属性</span><span class="sxs-lookup"><span data-stu-id="b8751-131">Attributes</span></span>

|<span data-ttu-id="b8751-132">**属性**</span><span class="sxs-lookup"><span data-stu-id="b8751-132">**Attribute**</span></span>|<span data-ttu-id="b8751-133">**型**</span><span class="sxs-lookup"><span data-stu-id="b8751-133">**Type**</span></span>|<span data-ttu-id="b8751-134">**必須**</span><span class="sxs-lookup"><span data-stu-id="b8751-134">**Required**</span></span>|<span data-ttu-id="b8751-135">**説明**</span><span class="sxs-lookup"><span data-stu-id="b8751-135">**Description**</span></span>|<span data-ttu-id="b8751-136">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="b8751-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b8751-137">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="b8751-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="b8751-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b8751-138">xsd:string</span></span>  <br/> |<span data-ttu-id="b8751-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="b8751-139">optional</span></span>  <br/> |<span data-ttu-id="b8751-140">主キーのコンポーネントであるフィールドの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="b8751-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="b8751-141">主キーが指定されている DataRecordSet_Type の DataColumn_Type の子孫要素の**ColumnNameID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8751-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="b8751-142">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8751-142">Values of the xsd:string type.</span></span>  <br/> |
   

