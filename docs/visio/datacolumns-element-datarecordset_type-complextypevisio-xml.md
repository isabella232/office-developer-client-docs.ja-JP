---
title: DataColumns 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: データ レコードセット内のすべての DataColumn 要素を格納します。
ms.openlocfilehash: e42354076c5e3e34c118145e7ec7fcdbd4977372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541198"
---
# <a name="datacolumns-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="7bfd0-103">DataColumns 要素 (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7bfd0-103">DataColumns element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7bfd0-104">データ レコードセット内のすべての **DataColumn** 要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="7bfd0-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7bfd0-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="7bfd0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7bfd0-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7bfd0-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="7bfd0-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7bfd0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7bfd0-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7bfd0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7bfd0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7bfd0-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7bfd0-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="7bfd0-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7bfd0-113">定義</span><span class="sxs-lookup"><span data-stu-id="7bfd0-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7bfd0-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="7bfd0-114">Elements and attributes</span></span>

<span data-ttu-id="7bfd0-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bfd0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7bfd0-116">親要素</span><span class="sxs-lookup"><span data-stu-id="7bfd0-116">Parent elements</span></span>

|<span data-ttu-id="7bfd0-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-117">**Element**</span></span>|<span data-ttu-id="7bfd0-118">**型**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-118">**Type**</span></span>|<span data-ttu-id="7bfd0-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7bfd0-120">DataRecordset</span><span class="sxs-lookup"><span data-stu-id="7bfd0-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7bfd0-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="7bfd0-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7bfd0-122">Microsoft Visio で、データベースに対してクエリされたデータの保存、書式設定、更新、表示を行います。</span><span class="sxs-lookup"><span data-stu-id="7bfd0-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7bfd0-123">子要素</span><span class="sxs-lookup"><span data-stu-id="7bfd0-123">Child elements</span></span>

|<span data-ttu-id="7bfd0-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-124">**Element**</span></span>|<span data-ttu-id="7bfd0-125">**型**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-125">**Type**</span></span>|<span data-ttu-id="7bfd0-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7bfd0-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="7bfd0-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7bfd0-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="7bfd0-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7bfd0-129">Visio ユーザー インターフェイスの **[外部データ]** ウィンドウにデータ列を表示する方法を定義し、データ型と書式を定義することで列内のデータを修飾します。</span><span class="sxs-lookup"><span data-stu-id="7bfd0-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7bfd0-130">属性</span><span class="sxs-lookup"><span data-stu-id="7bfd0-130">Attributes</span></span>

|<span data-ttu-id="7bfd0-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-131">**Attribute**</span></span>|<span data-ttu-id="7bfd0-132">**型**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-132">**Type**</span></span>|<span data-ttu-id="7bfd0-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-133">**Required**</span></span>|<span data-ttu-id="7bfd0-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-134">**Description**</span></span>|<span data-ttu-id="7bfd0-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="7bfd0-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7bfd0-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="7bfd0-136">SortAsc</span></span>  <br/> |<span data-ttu-id="7bfd0-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="7bfd0-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7bfd0-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="7bfd0-138">optional</span></span>  <br/> |<span data-ttu-id="7bfd0-139">データを並べ替える列。</span><span class="sxs-lookup"><span data-stu-id="7bfd0-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="7bfd0-140">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="7bfd0-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7bfd0-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="7bfd0-141">SortColumn</span></span>  <br/> |<span data-ttu-id="7bfd0-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7bfd0-142">xsd:string</span></span>  <br/> |<span data-ttu-id="7bfd0-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="7bfd0-143">optional</span></span>  <br/> |<span data-ttu-id="7bfd0-144">**SortColumn** 列を昇順 (1) または降順 (0) の順序で並べ替えるかどうか。</span><span class="sxs-lookup"><span data-stu-id="7bfd0-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="7bfd0-145">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="7bfd0-145">Values of the xsd:string type.</span></span>  <br/> |
   

