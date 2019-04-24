---
title: refreshconflict 要素 (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: データレコードセットの更新後に競合している図形にリンクされているデータレコードセット内の行を示します。
ms.openlocfilehash: 2da6f98cf7b047564331aaf5a4167e392927a155
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360138"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="7378d-103">refreshconflict 要素 (DataRecordSet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="7378d-103">RefreshConflict element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7378d-104">データレコードセットの更新後に競合している図形にリンクされているデータレコードセット内の行を示します。</span><span class="sxs-lookup"><span data-stu-id="7378d-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7378d-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="7378d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7378d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="7378d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7378d-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="7378d-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7378d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7378d-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7378d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="7378d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7378d-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="7378d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7378d-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="7378d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7378d-112">recordsets</span><span class="sxs-lookup"><span data-stu-id="7378d-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7378d-113">定義</span><span class="sxs-lookup"><span data-stu-id="7378d-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7378d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="7378d-114">Elements and attributes</span></span>

<span data-ttu-id="7378d-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7378d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7378d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="7378d-116">Parent elements</span></span>

|<span data-ttu-id="7378d-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="7378d-117">**Element**</span></span>|<span data-ttu-id="7378d-118">**型**</span><span class="sxs-lookup"><span data-stu-id="7378d-118">**Type**</span></span>|<span data-ttu-id="7378d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="7378d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7378d-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="7378d-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7378d-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="7378d-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7378d-122">Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。</span><span class="sxs-lookup"><span data-stu-id="7378d-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7378d-123">子要素</span><span class="sxs-lookup"><span data-stu-id="7378d-123">Child elements</span></span>

<span data-ttu-id="7378d-124">なし。</span><span class="sxs-lookup"><span data-stu-id="7378d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7378d-125">属性</span><span class="sxs-lookup"><span data-stu-id="7378d-125">Attributes</span></span>

|<span data-ttu-id="7378d-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="7378d-126">**Attribute**</span></span>|<span data-ttu-id="7378d-127">**型**</span><span class="sxs-lookup"><span data-stu-id="7378d-127">**Type**</span></span>|<span data-ttu-id="7378d-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="7378d-128">**Required**</span></span>|<span data-ttu-id="7378d-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="7378d-129">**Description**</span></span>|<span data-ttu-id="7378d-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="7378d-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7378d-131">PageID</span><span class="sxs-lookup"><span data-stu-id="7378d-131">PageID</span></span>  <br/> |<span data-ttu-id="7378d-132">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="7378d-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7378d-133">必須</span><span class="sxs-lookup"><span data-stu-id="7378d-133">required</span></span>  <br/> |<span data-ttu-id="7378d-134">競合に関係する図形のページ ID。</span><span class="sxs-lookup"><span data-stu-id="7378d-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="7378d-135">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="7378d-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7378d-136">RowID</span><span class="sxs-lookup"><span data-stu-id="7378d-136">RowID</span></span>  <br/> |<span data-ttu-id="7378d-137">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="7378d-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7378d-138">必須</span><span class="sxs-lookup"><span data-stu-id="7378d-138">required</span></span>  <br/> |<span data-ttu-id="7378d-139">データが更新された後に競合していた行の元の行 ID。</span><span class="sxs-lookup"><span data-stu-id="7378d-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="7378d-140">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="7378d-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7378d-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="7378d-141">ShapeID</span></span>  <br/> |<span data-ttu-id="7378d-142">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="7378d-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7378d-143">必須</span><span class="sxs-lookup"><span data-stu-id="7378d-143">required</span></span>  <br/> |<span data-ttu-id="7378d-144">競合に関係する図形の図形 ID。</span><span class="sxs-lookup"><span data-stu-id="7378d-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="7378d-145">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="7378d-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

