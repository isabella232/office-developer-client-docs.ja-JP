---
title: RowMap 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: データ レコードセットの行を図形にマップします。
ms.openlocfilehash: 178ceb06d64bfc9ef50f75dd22f8bd94f09f5c33
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540771"
---
# <a name="rowmap-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="59e66-103">RowMap 要素 (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="59e66-103">RowMap element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="59e66-104">データ レコードセットの行を図形にマップします。</span><span class="sxs-lookup"><span data-stu-id="59e66-104">Maps a data-recordset row to a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59e66-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="59e66-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59e66-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="59e66-106">**Element type**</span></span> <br/> |[<span data-ttu-id="59e66-107">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="59e66-107">RowMap_Type complexType</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="59e66-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="59e66-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="59e66-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="59e66-109">**Schema file**</span></span> <br/> |<span data-ttu-id="59e66-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="59e66-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="59e66-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="59e66-111">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="59e66-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="59e66-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="59e66-113">定義</span><span class="sxs-lookup"><span data-stu-id="59e66-113">Definition</span></span>

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="59e66-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="59e66-114">Elements and attributes</span></span>

<span data-ttu-id="59e66-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="59e66-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="59e66-116">親要素</span><span class="sxs-lookup"><span data-stu-id="59e66-116">Parent elements</span></span>

****

|<span data-ttu-id="59e66-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="59e66-117">**Element**</span></span>|<span data-ttu-id="59e66-118">**型**</span><span class="sxs-lookup"><span data-stu-id="59e66-118">**Type**</span></span>|<span data-ttu-id="59e66-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="59e66-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="59e66-120">DataRecordset</span><span class="sxs-lookup"><span data-stu-id="59e66-120">DataRecordset</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59e66-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="59e66-121">DataRecordSet_Type complexType</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59e66-122">Microsoft Visio で、データベースに対してクエリされたデータの保存、書式設定、更新、表示を行います。</span><span class="sxs-lookup"><span data-stu-id="59e66-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="59e66-123">子要素</span><span class="sxs-lookup"><span data-stu-id="59e66-123">Child elements</span></span>

<span data-ttu-id="59e66-124">なし。</span><span class="sxs-lookup"><span data-stu-id="59e66-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59e66-125">属性</span><span class="sxs-lookup"><span data-stu-id="59e66-125">Attributes</span></span>

|<span data-ttu-id="59e66-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="59e66-126">**Attribute**</span></span>|<span data-ttu-id="59e66-127">**型**</span><span class="sxs-lookup"><span data-stu-id="59e66-127">**Type**</span></span>|<span data-ttu-id="59e66-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="59e66-128">**Required**</span></span>|<span data-ttu-id="59e66-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="59e66-129">**Description**</span></span>|<span data-ttu-id="59e66-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="59e66-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="59e66-131">PageID</span><span class="sxs-lookup"><span data-stu-id="59e66-131">PageID</span></span>  <br/> |<span data-ttu-id="59e66-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="59e66-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="59e66-133">必須</span><span class="sxs-lookup"><span data-stu-id="59e66-133">required</span></span>  <br/> |<span data-ttu-id="59e66-134">**RowID** で識別されるデータレコードセット行のデータにリンクされている図形のページ ID。</span><span class="sxs-lookup"><span data-stu-id="59e66-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="59e66-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="59e66-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="59e66-136">RowID</span><span class="sxs-lookup"><span data-stu-id="59e66-136">RowID</span></span>  <br/> |<span data-ttu-id="59e66-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="59e66-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="59e66-138">必須</span><span class="sxs-lookup"><span data-stu-id="59e66-138">required</span></span>  <br/> |<span data-ttu-id="59e66-139">データレコードセット内の一意の行の ID。</span><span class="sxs-lookup"><span data-stu-id="59e66-139">Row ID of the row, unique within the data recordset.</span></span>  <br/> |<span data-ttu-id="59e66-140">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="59e66-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="59e66-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="59e66-141">shapeId</span></span>  <br/> |<span data-ttu-id="59e66-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="59e66-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="59e66-143">必須</span><span class="sxs-lookup"><span data-stu-id="59e66-143">required</span></span>  <br/> |<span data-ttu-id="59e66-144">**RowID** で識別されるデータレコードセット行のデータにリンクされている図形の Shape ID。</span><span class="sxs-lookup"><span data-stu-id="59e66-144">Shape ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="59e66-145">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="59e66-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

