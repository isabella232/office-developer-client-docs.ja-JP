---
title: 主キーの要素 (DataRecordSet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: データ レコード セット内の 1 つまたは複数の主キー列を識別します。
ms.openlocfilehash: f720636bbdf2c55baca6d98aa7d0761607e53ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806119"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="946bf-103">主キーの要素 (DataRecordSet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="946bf-103">PrimaryKey element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="946bf-104">データ レコード セット内の 1 つまたは複数の主キー列を識別します。</span><span class="sxs-lookup"><span data-stu-id="946bf-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="946bf-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="946bf-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="946bf-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="946bf-106">**Element type**</span></span> <br/> |[<span data-ttu-id="946bf-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="946bf-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="946bf-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="946bf-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="946bf-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="946bf-109">**Schema file**</span></span> <br/> |<span data-ttu-id="946bf-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="946bf-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="946bf-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="946bf-111">**Document parts**</span></span> <br/> |<span data-ttu-id="946bf-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="946bf-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="946bf-113">定義</span><span class="sxs-lookup"><span data-stu-id="946bf-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="946bf-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="946bf-114">Elements and attributes</span></span>

<span data-ttu-id="946bf-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="946bf-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="946bf-116">親要素</span><span class="sxs-lookup"><span data-stu-id="946bf-116">Parent elements</span></span>

|<span data-ttu-id="946bf-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="946bf-117">**Element**</span></span>|<span data-ttu-id="946bf-118">**型**</span><span class="sxs-lookup"><span data-stu-id="946bf-118">**Type**</span></span>|<span data-ttu-id="946bf-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="946bf-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="946bf-120">データ レコード セット</span><span class="sxs-lookup"><span data-stu-id="946bf-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="946bf-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="946bf-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="946bf-122">Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。</span><span class="sxs-lookup"><span data-stu-id="946bf-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="946bf-123">子要素</span><span class="sxs-lookup"><span data-stu-id="946bf-123">Child elements</span></span>

|<span data-ttu-id="946bf-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="946bf-124">**Element**</span></span>|<span data-ttu-id="946bf-125">**型**</span><span class="sxs-lookup"><span data-stu-id="946bf-125">**Type**</span></span>|<span data-ttu-id="946bf-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="946bf-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="946bf-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="946bf-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="946bf-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="946bf-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="946bf-129">このコンポーネントのレコード セットの個別の行の主キーの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="946bf-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="946bf-130">この子要素の 1 つ以上の出現が必要があります。</span><span class="sxs-lookup"><span data-stu-id="946bf-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="946bf-131">属性</span><span class="sxs-lookup"><span data-stu-id="946bf-131">Attributes</span></span>

|<span data-ttu-id="946bf-132">**属性**</span><span class="sxs-lookup"><span data-stu-id="946bf-132">**Attribute**</span></span>|<span data-ttu-id="946bf-133">**型**</span><span class="sxs-lookup"><span data-stu-id="946bf-133">**Type**</span></span>|<span data-ttu-id="946bf-134">**必須**</span><span class="sxs-lookup"><span data-stu-id="946bf-134">**Required**</span></span>|<span data-ttu-id="946bf-135">**説明**</span><span class="sxs-lookup"><span data-stu-id="946bf-135">**Description**</span></span>|<span data-ttu-id="946bf-136">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="946bf-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="946bf-137">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="946bf-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="946bf-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="946bf-138">xsd:string</span></span>  <br/> |<span data-ttu-id="946bf-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="946bf-139">optional</span></span>  <br/> |<span data-ttu-id="946bf-140">主キーのコンポーネントであるフィールドの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="946bf-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="946bf-141">主キーが指定されている DataRecordSet_Type の DataColumn_Type の子孫要素の**ColumnNameID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="946bf-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="946bf-142">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="946bf-142">Values of the xsd:string type.</span></span>  <br/> |
   

