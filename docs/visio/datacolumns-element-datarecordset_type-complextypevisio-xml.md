---
title: Datacolumn の要素 (DataRecordSet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: データ レコード セット内のすべての列要素が含まれています。
ms.openlocfilehash: b90b6cb18fc2bd1edc393d58a9d761cfb36ea220
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805160"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="75537-103">Datacolumn の要素 (DataRecordSet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="75537-103">DataColumns element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="75537-104">データ レコード セット内のすべての**列**要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="75537-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="75537-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="75537-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75537-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="75537-106">**Element type**</span></span> <br/> |[<span data-ttu-id="75537-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="75537-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="75537-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="75537-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="75537-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="75537-109">**Schema file**</span></span> <br/> |<span data-ttu-id="75537-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="75537-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="75537-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="75537-111">**Document parts**</span></span> <br/> |<span data-ttu-id="75537-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="75537-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="75537-113">定義</span><span class="sxs-lookup"><span data-stu-id="75537-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="75537-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="75537-114">Elements and attributes</span></span>

<span data-ttu-id="75537-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="75537-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="75537-116">親要素</span><span class="sxs-lookup"><span data-stu-id="75537-116">Parent elements</span></span>

|<span data-ttu-id="75537-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="75537-117">**Element**</span></span>|<span data-ttu-id="75537-118">**型**</span><span class="sxs-lookup"><span data-stu-id="75537-118">**Type**</span></span>|<span data-ttu-id="75537-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="75537-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="75537-120">データ レコード セット</span><span class="sxs-lookup"><span data-stu-id="75537-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75537-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="75537-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75537-122">Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。</span><span class="sxs-lookup"><span data-stu-id="75537-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="75537-123">子要素</span><span class="sxs-lookup"><span data-stu-id="75537-123">Child elements</span></span>

|<span data-ttu-id="75537-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="75537-124">**Element**</span></span>|<span data-ttu-id="75537-125">**型**</span><span class="sxs-lookup"><span data-stu-id="75537-125">**Type**</span></span>|<span data-ttu-id="75537-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="75537-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="75537-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="75537-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75537-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="75537-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75537-129">データ列が Visio ユーザー インターフェイスの [**外部データ**] ウィンドウで表示する方法を定義し、そのデータ型を定義して、書式設定、列のデータが適用されます。</span><span class="sxs-lookup"><span data-stu-id="75537-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="75537-130">属性</span><span class="sxs-lookup"><span data-stu-id="75537-130">Attributes</span></span>

|<span data-ttu-id="75537-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="75537-131">**Attribute**</span></span>|<span data-ttu-id="75537-132">**型**</span><span class="sxs-lookup"><span data-stu-id="75537-132">**Type**</span></span>|<span data-ttu-id="75537-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="75537-133">**Required**</span></span>|<span data-ttu-id="75537-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="75537-134">**Description**</span></span>|<span data-ttu-id="75537-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="75537-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="75537-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="75537-136">SortAsc</span></span>  <br/> |<span data-ttu-id="75537-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="75537-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="75537-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="75537-138">optional</span></span>  <br/> |<span data-ttu-id="75537-139">データの並べ替えを行う列。</span><span class="sxs-lookup"><span data-stu-id="75537-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="75537-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="75537-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="75537-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="75537-141">SortColumn</span></span>  <br/> |<span data-ttu-id="75537-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="75537-142">xsd:string</span></span>  <br/> |<span data-ttu-id="75537-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="75537-143">optional</span></span>  <br/> |<span data-ttu-id="75537-144">**SortColumn**列を昇順 (1) または降順 (0) を並べ替えるかどうか。</span><span class="sxs-lookup"><span data-stu-id="75537-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="75537-145">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="75537-145">Values of the xsd:string type.</span></span>  <br/> |
   

