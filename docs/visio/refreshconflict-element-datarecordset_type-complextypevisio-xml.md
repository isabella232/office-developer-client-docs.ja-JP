---
title: RefreshConflict 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: 図形にリンクされたデータ レコードセット内の行で、データ レコードセットの更新後に競合した状態になっているものを示します。
ms.openlocfilehash: f966ca4a9f23de7a96273615b2404041d1045652
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542836"
---
# <a name="refreshconflict-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="34bfb-103">RefreshConflict 要素 (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="34bfb-103">RefreshConflict element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="34bfb-104">図形にリンクされたデータ レコードセット内の行で、データ レコードセットの更新後に競合した状態になっているものを示します。</span><span class="sxs-lookup"><span data-stu-id="34bfb-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34bfb-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="34bfb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34bfb-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="34bfb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="34bfb-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="34bfb-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="34bfb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="34bfb-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="34bfb-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="34bfb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="34bfb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="34bfb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="34bfb-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="34bfb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="34bfb-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="34bfb-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="34bfb-113">定義</span><span class="sxs-lookup"><span data-stu-id="34bfb-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="34bfb-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="34bfb-114">Elements and attributes</span></span>

<span data-ttu-id="34bfb-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="34bfb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="34bfb-116">親要素</span><span class="sxs-lookup"><span data-stu-id="34bfb-116">Parent elements</span></span>

|<span data-ttu-id="34bfb-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="34bfb-117">**Element**</span></span>|<span data-ttu-id="34bfb-118">**型**</span><span class="sxs-lookup"><span data-stu-id="34bfb-118">**Type**</span></span>|<span data-ttu-id="34bfb-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="34bfb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="34bfb-120">DataRecordset</span><span class="sxs-lookup"><span data-stu-id="34bfb-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="34bfb-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="34bfb-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="34bfb-122">Microsoft Visio で、データベースに対してクエリされたデータの保存、書式設定、更新、表示を行います。</span><span class="sxs-lookup"><span data-stu-id="34bfb-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="34bfb-123">子要素</span><span class="sxs-lookup"><span data-stu-id="34bfb-123">Child elements</span></span>

<span data-ttu-id="34bfb-124">なし。</span><span class="sxs-lookup"><span data-stu-id="34bfb-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34bfb-125">属性</span><span class="sxs-lookup"><span data-stu-id="34bfb-125">Attributes</span></span>

|<span data-ttu-id="34bfb-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="34bfb-126">**Attribute**</span></span>|<span data-ttu-id="34bfb-127">**型**</span><span class="sxs-lookup"><span data-stu-id="34bfb-127">**Type**</span></span>|<span data-ttu-id="34bfb-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="34bfb-128">**Required**</span></span>|<span data-ttu-id="34bfb-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="34bfb-129">**Description**</span></span>|<span data-ttu-id="34bfb-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="34bfb-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="34bfb-131">PageID</span><span class="sxs-lookup"><span data-stu-id="34bfb-131">PageID</span></span>  <br/> |<span data-ttu-id="34bfb-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="34bfb-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="34bfb-133">必須</span><span class="sxs-lookup"><span data-stu-id="34bfb-133">required</span></span>  <br/> |<span data-ttu-id="34bfb-134">競合に関係する図形のページ ID。</span><span class="sxs-lookup"><span data-stu-id="34bfb-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="34bfb-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="34bfb-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="34bfb-136">RowID</span><span class="sxs-lookup"><span data-stu-id="34bfb-136">RowID</span></span>  <br/> |<span data-ttu-id="34bfb-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="34bfb-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="34bfb-138">必須</span><span class="sxs-lookup"><span data-stu-id="34bfb-138">required</span></span>  <br/> |<span data-ttu-id="34bfb-139">データが更新された後、行の元の行 ID が競合しています。</span><span class="sxs-lookup"><span data-stu-id="34bfb-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="34bfb-140">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="34bfb-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="34bfb-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="34bfb-141">ShapeID</span></span>  <br/> |<span data-ttu-id="34bfb-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="34bfb-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="34bfb-143">必須</span><span class="sxs-lookup"><span data-stu-id="34bfb-143">required</span></span>  <br/> |<span data-ttu-id="34bfb-144">競合に関係する図形の図形 ID。</span><span class="sxs-lookup"><span data-stu-id="34bfb-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="34bfb-145">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="34bfb-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

