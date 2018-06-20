---
title: RowMap 要素 (DataRecordSet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: レコード セットのデータ行を図形にマップします。
ms.openlocfilehash: aefae8c625f35feacd6d0fdf04f128c423db299b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806321"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="8f902-103">RowMap 要素 (DataRecordSet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="8f902-103">RowMap element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8f902-104">レコード セットのデータ行を図形にマップします。</span><span class="sxs-lookup"><span data-stu-id="8f902-104">Maps a data-recordset row to a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8f902-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="8f902-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f902-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="8f902-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8f902-107">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="8f902-107">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8f902-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="8f902-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8f902-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8f902-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8f902-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8f902-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8f902-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="8f902-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8f902-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="8f902-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8f902-113">定義</span><span class="sxs-lookup"><span data-stu-id="8f902-113">Definition</span></span>

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8f902-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8f902-114">Elements and attributes</span></span>

<span data-ttu-id="8f902-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f902-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8f902-116">親要素</span><span class="sxs-lookup"><span data-stu-id="8f902-116">Parent elements</span></span>

****

|<span data-ttu-id="8f902-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="8f902-117">**Element**</span></span>|<span data-ttu-id="8f902-118">**型**</span><span class="sxs-lookup"><span data-stu-id="8f902-118">**Type**</span></span>|<span data-ttu-id="8f902-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="8f902-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8f902-120">データ レコード セット</span><span class="sxs-lookup"><span data-stu-id="8f902-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8f902-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="8f902-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8f902-122">Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。</span><span class="sxs-lookup"><span data-stu-id="8f902-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8f902-123">子要素</span><span class="sxs-lookup"><span data-stu-id="8f902-123">Child elements</span></span>

<span data-ttu-id="8f902-124">なし。</span><span class="sxs-lookup"><span data-stu-id="8f902-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8f902-125">属性</span><span class="sxs-lookup"><span data-stu-id="8f902-125">Attributes</span></span>

|<span data-ttu-id="8f902-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="8f902-126">**Attribute**</span></span>|<span data-ttu-id="8f902-127">**型**</span><span class="sxs-lookup"><span data-stu-id="8f902-127">**Type**</span></span>|<span data-ttu-id="8f902-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="8f902-128">**Required**</span></span>|<span data-ttu-id="8f902-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="8f902-129">**Description**</span></span>|<span data-ttu-id="8f902-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="8f902-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8f902-131">PageID</span><span class="sxs-lookup"><span data-stu-id="8f902-131">PageID</span></span>  <br/> |<span data-ttu-id="8f902-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8f902-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8f902-133">必須</span><span class="sxs-lookup"><span data-stu-id="8f902-133">required</span></span>  <br/> |<span data-ttu-id="8f902-134">**RowID**で識別されるデータ レコード セット行のデータにリンクされている図形のページの ID です。</span><span class="sxs-lookup"><span data-stu-id="8f902-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="8f902-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8f902-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8f902-136">RowID</span><span class="sxs-lookup"><span data-stu-id="8f902-136">RowID</span></span>  <br/> |<span data-ttu-id="8f902-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8f902-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8f902-138">必須</span><span class="sxs-lookup"><span data-stu-id="8f902-138">required</span></span>  <br/> |<span data-ttu-id="8f902-139">データ レコード セット内で一意の行の行 ID です。</span><span class="sxs-lookup"><span data-stu-id="8f902-139">Row ID of the row, unique within the data recordset.</span></span>  <br/> |<span data-ttu-id="8f902-140">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8f902-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8f902-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="8f902-141">ShapeID</span></span>  <br/> |<span data-ttu-id="8f902-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8f902-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8f902-143">必須</span><span class="sxs-lookup"><span data-stu-id="8f902-143">required</span></span>  <br/> |<span data-ttu-id="8f902-144">**RowID**で識別されるデータ レコード セット行のデータにリンクされた図形の図形 ID です。</span><span class="sxs-lookup"><span data-stu-id="8f902-144">Shape ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="8f902-145">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8f902-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

