---
title: DataColumns 要素 (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: データレコードセット内のすべての DataColumn 要素を含みます。
ms.openlocfilehash: a7a0a8faefdb965384e435ee3a9b059a3acbc3f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345249"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="9b8ca-103">DataColumns 要素 (DataRecordSet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9b8ca-103">DataColumns element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9b8ca-104">データレコードセット内のすべての**DataColumn**要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="9b8ca-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9b8ca-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="9b8ca-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b8ca-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9b8ca-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="9b8ca-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9b8ca-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9b8ca-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9b8ca-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="9b8ca-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9b8ca-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9b8ca-112">recordsets</span><span class="sxs-lookup"><span data-stu-id="9b8ca-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9b8ca-113">定義</span><span class="sxs-lookup"><span data-stu-id="9b8ca-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9b8ca-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9b8ca-114">Elements and attributes</span></span>

<span data-ttu-id="9b8ca-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b8ca-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9b8ca-116">親要素</span><span class="sxs-lookup"><span data-stu-id="9b8ca-116">Parent elements</span></span>

|<span data-ttu-id="9b8ca-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-117">**Element**</span></span>|<span data-ttu-id="9b8ca-118">**型**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-118">**Type**</span></span>|<span data-ttu-id="9b8ca-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9b8ca-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="9b8ca-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9b8ca-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="9b8ca-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9b8ca-122">Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。</span><span class="sxs-lookup"><span data-stu-id="9b8ca-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9b8ca-123">子要素</span><span class="sxs-lookup"><span data-stu-id="9b8ca-123">Child elements</span></span>

|<span data-ttu-id="9b8ca-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-124">**Element**</span></span>|<span data-ttu-id="9b8ca-125">**型**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-125">**Type**</span></span>|<span data-ttu-id="9b8ca-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9b8ca-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="9b8ca-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9b8ca-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="9b8ca-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9b8ca-129">Visio ユーザーインターフェイスの [**外部データ**] ウィンドウにデータ列を表示する方法を定義し、データの種類と書式を定義することによって、列のデータを修飾します。</span><span class="sxs-lookup"><span data-stu-id="9b8ca-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9b8ca-130">属性</span><span class="sxs-lookup"><span data-stu-id="9b8ca-130">Attributes</span></span>

|<span data-ttu-id="9b8ca-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-131">**Attribute**</span></span>|<span data-ttu-id="9b8ca-132">**型**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-132">**Type**</span></span>|<span data-ttu-id="9b8ca-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-133">**Required**</span></span>|<span data-ttu-id="9b8ca-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-134">**Description**</span></span>|<span data-ttu-id="9b8ca-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="9b8ca-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9b8ca-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="9b8ca-136">SortAsc</span></span>  <br/> |<span data-ttu-id="9b8ca-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="9b8ca-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9b8ca-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="9b8ca-138">optional</span></span>  <br/> |<span data-ttu-id="9b8ca-139">データの並べ替えの基準となる列を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b8ca-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="9b8ca-140">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="9b8ca-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9b8ca-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="9b8ca-141">SortColumn</span></span>  <br/> |<span data-ttu-id="9b8ca-142">xsd: string</span><span class="sxs-lookup"><span data-stu-id="9b8ca-142">xsd:string</span></span>  <br/> |<span data-ttu-id="9b8ca-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="9b8ca-143">optional</span></span>  <br/> |<span data-ttu-id="9b8ca-144">**sortcolumn**列を昇順 (1) または降順 (0) のどちらで並べ替えるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9b8ca-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="9b8ca-145">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="9b8ca-145">Values of the xsd:string type.</span></span>  <br/> |
   

