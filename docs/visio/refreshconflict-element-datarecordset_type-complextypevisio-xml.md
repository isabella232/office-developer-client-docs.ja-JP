---
title: RefreshConflict 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: データレコードセットの更新後に競合している図形にリンクされているデータレコードセット内の行を示します。
ms.openlocfilehash: f966ca4a9f23de7a96273615b2404041d1045652
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542836"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="bf605-103">RefreshConflict 要素 (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bf605-103">RefreshConflict element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="bf605-104">データレコードセットの更新後に競合している図形にリンクされているデータレコードセット内の行を示します。</span><span class="sxs-lookup"><span data-stu-id="bf605-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bf605-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="bf605-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf605-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="bf605-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bf605-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="bf605-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bf605-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bf605-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bf605-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="bf605-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bf605-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="bf605-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bf605-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="bf605-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bf605-112">recordsets</span><span class="sxs-lookup"><span data-stu-id="bf605-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bf605-113">定義</span><span class="sxs-lookup"><span data-stu-id="bf605-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bf605-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="bf605-114">Elements and attributes</span></span>

<span data-ttu-id="bf605-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf605-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bf605-116">親要素</span><span class="sxs-lookup"><span data-stu-id="bf605-116">Parent elements</span></span>

|<span data-ttu-id="bf605-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="bf605-117">**Element**</span></span>|<span data-ttu-id="bf605-118">**型**</span><span class="sxs-lookup"><span data-stu-id="bf605-118">**Type**</span></span>|<span data-ttu-id="bf605-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="bf605-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bf605-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="bf605-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bf605-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="bf605-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bf605-122">Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。</span><span class="sxs-lookup"><span data-stu-id="bf605-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bf605-123">子要素</span><span class="sxs-lookup"><span data-stu-id="bf605-123">Child elements</span></span>

<span data-ttu-id="bf605-124">なし。</span><span class="sxs-lookup"><span data-stu-id="bf605-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bf605-125">属性</span><span class="sxs-lookup"><span data-stu-id="bf605-125">Attributes</span></span>

|<span data-ttu-id="bf605-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="bf605-126">**Attribute**</span></span>|<span data-ttu-id="bf605-127">**型**</span><span class="sxs-lookup"><span data-stu-id="bf605-127">**Type**</span></span>|<span data-ttu-id="bf605-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="bf605-128">**Required**</span></span>|<span data-ttu-id="bf605-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="bf605-129">**Description**</span></span>|<span data-ttu-id="bf605-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="bf605-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bf605-131">PageID</span><span class="sxs-lookup"><span data-stu-id="bf605-131">PageID</span></span>  <br/> |<span data-ttu-id="bf605-132">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="bf605-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bf605-133">必須</span><span class="sxs-lookup"><span data-stu-id="bf605-133">required</span></span>  <br/> |<span data-ttu-id="bf605-134">競合に関係する図形のページ ID。</span><span class="sxs-lookup"><span data-stu-id="bf605-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="bf605-135">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="bf605-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bf605-136">RowID</span><span class="sxs-lookup"><span data-stu-id="bf605-136">RowID</span></span>  <br/> |<span data-ttu-id="bf605-137">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="bf605-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bf605-138">必須</span><span class="sxs-lookup"><span data-stu-id="bf605-138">required</span></span>  <br/> |<span data-ttu-id="bf605-139">データが更新された後に競合していた行の元の行 ID。</span><span class="sxs-lookup"><span data-stu-id="bf605-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="bf605-140">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="bf605-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bf605-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="bf605-141">ShapeID</span></span>  <br/> |<span data-ttu-id="bf605-142">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="bf605-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bf605-143">必須</span><span class="sxs-lookup"><span data-stu-id="bf605-143">required</span></span>  <br/> |<span data-ttu-id="bf605-144">競合に関係する図形の図形 ID。</span><span class="sxs-lookup"><span data-stu-id="bf605-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="bf605-145">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="bf605-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

