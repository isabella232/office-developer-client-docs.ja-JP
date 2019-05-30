---
title: DataColumns 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: データレコードセット内のすべての DataColumn 要素を含みます。
ms.openlocfilehash: e42354076c5e3e34c118145e7ec7fcdbd4977372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541198"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="eea9d-103">DataColumns 要素 (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="eea9d-103">DataColumns element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="eea9d-104">データレコードセット内のすべての**DataColumn**要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="eea9d-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="eea9d-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="eea9d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eea9d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="eea9d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="eea9d-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="eea9d-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="eea9d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="eea9d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="eea9d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="eea9d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="eea9d-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="eea9d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="eea9d-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="eea9d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="eea9d-112">recordsets</span><span class="sxs-lookup"><span data-stu-id="eea9d-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eea9d-113">定義</span><span class="sxs-lookup"><span data-stu-id="eea9d-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="eea9d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="eea9d-114">Elements and attributes</span></span>

<span data-ttu-id="eea9d-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="eea9d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="eea9d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="eea9d-116">Parent elements</span></span>

|<span data-ttu-id="eea9d-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="eea9d-117">**Element**</span></span>|<span data-ttu-id="eea9d-118">**型**</span><span class="sxs-lookup"><span data-stu-id="eea9d-118">**Type**</span></span>|<span data-ttu-id="eea9d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="eea9d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="eea9d-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="eea9d-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="eea9d-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="eea9d-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="eea9d-122">Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。</span><span class="sxs-lookup"><span data-stu-id="eea9d-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="eea9d-123">子要素</span><span class="sxs-lookup"><span data-stu-id="eea9d-123">Child elements</span></span>

|<span data-ttu-id="eea9d-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="eea9d-124">**Element**</span></span>|<span data-ttu-id="eea9d-125">**型**</span><span class="sxs-lookup"><span data-stu-id="eea9d-125">**Type**</span></span>|<span data-ttu-id="eea9d-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="eea9d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="eea9d-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="eea9d-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="eea9d-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="eea9d-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="eea9d-129">Visio ユーザーインターフェイスの [**外部データ**] ウィンドウにデータ列を表示する方法を定義し、データの種類と書式を定義することによって、列のデータを修飾します。</span><span class="sxs-lookup"><span data-stu-id="eea9d-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="eea9d-130">属性</span><span class="sxs-lookup"><span data-stu-id="eea9d-130">Attributes</span></span>

|<span data-ttu-id="eea9d-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="eea9d-131">**Attribute**</span></span>|<span data-ttu-id="eea9d-132">**型**</span><span class="sxs-lookup"><span data-stu-id="eea9d-132">**Type**</span></span>|<span data-ttu-id="eea9d-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="eea9d-133">**Required**</span></span>|<span data-ttu-id="eea9d-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="eea9d-134">**Description**</span></span>|<span data-ttu-id="eea9d-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="eea9d-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="eea9d-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="eea9d-136">SortAsc</span></span>  <br/> |<span data-ttu-id="eea9d-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="eea9d-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="eea9d-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="eea9d-138">optional</span></span>  <br/> |<span data-ttu-id="eea9d-139">データの並べ替えの基準となる列を指定します。</span><span class="sxs-lookup"><span data-stu-id="eea9d-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="eea9d-140">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="eea9d-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="eea9d-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="eea9d-141">SortColumn</span></span>  <br/> |<span data-ttu-id="eea9d-142">xsd: string</span><span class="sxs-lookup"><span data-stu-id="eea9d-142">xsd:string</span></span>  <br/> |<span data-ttu-id="eea9d-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="eea9d-143">optional</span></span>  <br/> |<span data-ttu-id="eea9d-144">**Sortcolumn**列を昇順 (1) または降順 (0) のどちらで並べ替えるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="eea9d-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="eea9d-145">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="eea9d-145">Values of the xsd:string type.</span></span>  <br/> |
   

