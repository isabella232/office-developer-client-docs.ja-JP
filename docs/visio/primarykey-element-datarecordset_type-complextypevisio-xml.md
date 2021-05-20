---
title: PrimaryKey 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: データ レコードセット内で 1 つ以上の主キー列を識別します。
ms.openlocfilehash: bd77b1d18490695dc2b0cb43520f42bb845e91ab
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537711"
---
# <a name="primarykey-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="ad4c1-103">PrimaryKey 要素 (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ad4c1-103">PrimaryKey element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ad4c1-104">データ レコードセット内で 1 つ以上の主キー列を識別します。</span><span class="sxs-lookup"><span data-stu-id="ad4c1-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad4c1-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="ad4c1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad4c1-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ad4c1-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="ad4c1-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ad4c1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ad4c1-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ad4c1-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ad4c1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ad4c1-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ad4c1-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="ad4c1-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad4c1-113">定義</span><span class="sxs-lookup"><span data-stu-id="ad4c1-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad4c1-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ad4c1-114">Elements and attributes</span></span>

<span data-ttu-id="ad4c1-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad4c1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ad4c1-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ad4c1-116">Parent elements</span></span>

|<span data-ttu-id="ad4c1-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-117">**Element**</span></span>|<span data-ttu-id="ad4c1-118">**型**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-118">**Type**</span></span>|<span data-ttu-id="ad4c1-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad4c1-120">DataRecordset</span><span class="sxs-lookup"><span data-stu-id="ad4c1-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad4c1-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="ad4c1-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad4c1-122">Microsoft Visio で、データベースに対してクエリされたデータの保存、書式設定、更新、表示を行います。</span><span class="sxs-lookup"><span data-stu-id="ad4c1-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad4c1-123">子要素</span><span class="sxs-lookup"><span data-stu-id="ad4c1-123">Child elements</span></span>

|<span data-ttu-id="ad4c1-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-124">**Element**</span></span>|<span data-ttu-id="ad4c1-125">**型**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-125">**Type**</span></span>|<span data-ttu-id="ad4c1-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad4c1-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="ad4c1-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad4c1-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="ad4c1-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad4c1-129">レコードセットの個々の行の主キーのこのコンポーネントの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ad4c1-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="ad4c1-130">この子要素が少なくとも 1 つ出現する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad4c1-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ad4c1-131">属性</span><span class="sxs-lookup"><span data-stu-id="ad4c1-131">Attributes</span></span>

|<span data-ttu-id="ad4c1-132">**属性**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-132">**Attribute**</span></span>|<span data-ttu-id="ad4c1-133">**型**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-133">**Type**</span></span>|<span data-ttu-id="ad4c1-134">**必須**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-134">**Required**</span></span>|<span data-ttu-id="ad4c1-135">**説明**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-135">**Description**</span></span>|<span data-ttu-id="ad4c1-136">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="ad4c1-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad4c1-137">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="ad4c1-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="ad4c1-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ad4c1-138">xsd:string</span></span>  <br/> |<span data-ttu-id="ad4c1-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="ad4c1-139">optional</span></span>  <br/> |<span data-ttu-id="ad4c1-140">主キーのコンポーネントであるフィールドの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="ad4c1-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="ad4c1-141">主キーが指定されているDataColumn_Typeの子要素DataRecordSet_Type **ColumnNameID** 属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad4c1-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="ad4c1-142">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="ad4c1-142">Values of the xsd:string type.</span></span>  <br/> |
   

