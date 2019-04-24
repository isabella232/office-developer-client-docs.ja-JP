---
title: rowmap 要素 (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: データレコードセットの行を図形にマップします。
ms.openlocfilehash: 2dffa49d66e8e447b4e31d771179c74eecad21da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332516"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="3c79c-103">rowmap 要素 (DataRecordSet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="3c79c-103">RowMap element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3c79c-104">データレコードセットの行を図形にマップします。</span><span class="sxs-lookup"><span data-stu-id="3c79c-104">Maps a data-recordset row to a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c79c-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="3c79c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c79c-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="3c79c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3c79c-107">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="3c79c-107">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3c79c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3c79c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3c79c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="3c79c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3c79c-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="3c79c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3c79c-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="3c79c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3c79c-112">recordsets</span><span class="sxs-lookup"><span data-stu-id="3c79c-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3c79c-113">定義</span><span class="sxs-lookup"><span data-stu-id="3c79c-113">Definition</span></span>

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3c79c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="3c79c-114">Elements and attributes</span></span>

<span data-ttu-id="3c79c-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c79c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3c79c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="3c79c-116">Parent elements</span></span>

****

|<span data-ttu-id="3c79c-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="3c79c-117">**Element**</span></span>|<span data-ttu-id="3c79c-118">**型**</span><span class="sxs-lookup"><span data-stu-id="3c79c-118">**Type**</span></span>|<span data-ttu-id="3c79c-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="3c79c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3c79c-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="3c79c-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c79c-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="3c79c-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3c79c-122">Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。</span><span class="sxs-lookup"><span data-stu-id="3c79c-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3c79c-123">子要素</span><span class="sxs-lookup"><span data-stu-id="3c79c-123">Child elements</span></span>

<span data-ttu-id="3c79c-124">なし。</span><span class="sxs-lookup"><span data-stu-id="3c79c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c79c-125">属性</span><span class="sxs-lookup"><span data-stu-id="3c79c-125">Attributes</span></span>

|<span data-ttu-id="3c79c-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="3c79c-126">**Attribute**</span></span>|<span data-ttu-id="3c79c-127">**型**</span><span class="sxs-lookup"><span data-stu-id="3c79c-127">**Type**</span></span>|<span data-ttu-id="3c79c-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="3c79c-128">**Required**</span></span>|<span data-ttu-id="3c79c-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="3c79c-129">**Description**</span></span>|<span data-ttu-id="3c79c-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="3c79c-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3c79c-131">PageID</span><span class="sxs-lookup"><span data-stu-id="3c79c-131">PageID</span></span>  <br/> |<span data-ttu-id="3c79c-132">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="3c79c-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3c79c-133">必須</span><span class="sxs-lookup"><span data-stu-id="3c79c-133">required</span></span>  <br/> |<span data-ttu-id="3c79c-134">**RowID**で識別されるデータレコードセット行のデータにリンクされている図形のページ ID。</span><span class="sxs-lookup"><span data-stu-id="3c79c-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="3c79c-135">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="3c79c-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3c79c-136">RowID</span><span class="sxs-lookup"><span data-stu-id="3c79c-136">RowID</span></span>  <br/> |<span data-ttu-id="3c79c-137">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="3c79c-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3c79c-138">必須</span><span class="sxs-lookup"><span data-stu-id="3c79c-138">required</span></span>  <br/> |<span data-ttu-id="3c79c-139">データレコードセット内で一意の行 ID。</span><span class="sxs-lookup"><span data-stu-id="3c79c-139">Row ID of the row, unique within the data recordset.</span></span>  <br/> |<span data-ttu-id="3c79c-140">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="3c79c-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3c79c-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="3c79c-141">ShapeID</span></span>  <br/> |<span data-ttu-id="3c79c-142">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="3c79c-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3c79c-143">必須</span><span class="sxs-lookup"><span data-stu-id="3c79c-143">required</span></span>  <br/> |<span data-ttu-id="3c79c-144">**RowID**で識別されるデータレコードセット行のデータにリンクされている図形の図形 ID。</span><span class="sxs-lookup"><span data-stu-id="3c79c-144">Shape ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="3c79c-145">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="3c79c-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

