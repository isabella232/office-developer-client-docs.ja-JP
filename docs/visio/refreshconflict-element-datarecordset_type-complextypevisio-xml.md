---
title: RefreshConflict 要素 (DataRecordSet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: データ レコード セットが更新された後に、競合がある図形にリンクされているデータ レコード セット内の行を示します。
ms.openlocfilehash: 2da6f98cf7b047564331aaf5a4167e392927a155
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397402"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="ef668-103">RefreshConflict 要素 (DataRecordSet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="ef668-103">RefreshConflict element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ef668-104">データ レコード セットが更新された後に、競合がある図形にリンクされているデータ レコード セット内の行を示します。</span><span class="sxs-lookup"><span data-stu-id="ef668-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef668-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="ef668-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef668-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="ef668-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ef668-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="ef668-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ef668-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="ef668-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ef668-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ef668-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ef668-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ef668-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ef668-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="ef668-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ef668-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="ef668-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ef668-113">定義</span><span class="sxs-lookup"><span data-stu-id="ef668-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ef668-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ef668-114">Elements and attributes</span></span>

<span data-ttu-id="ef668-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef668-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ef668-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ef668-116">Parent elements</span></span>

|<span data-ttu-id="ef668-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="ef668-117">**Element**</span></span>|<span data-ttu-id="ef668-118">**型**</span><span class="sxs-lookup"><span data-stu-id="ef668-118">**Type**</span></span>|<span data-ttu-id="ef668-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="ef668-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ef668-120">データ レコード セット</span><span class="sxs-lookup"><span data-stu-id="ef668-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ef668-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="ef668-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ef668-122">Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。</span><span class="sxs-lookup"><span data-stu-id="ef668-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ef668-123">子要素</span><span class="sxs-lookup"><span data-stu-id="ef668-123">Child elements</span></span>

<span data-ttu-id="ef668-124">なし。</span><span class="sxs-lookup"><span data-stu-id="ef668-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef668-125">属性</span><span class="sxs-lookup"><span data-stu-id="ef668-125">Attributes</span></span>

|<span data-ttu-id="ef668-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="ef668-126">**Attribute**</span></span>|<span data-ttu-id="ef668-127">**型**</span><span class="sxs-lookup"><span data-stu-id="ef668-127">**Type**</span></span>|<span data-ttu-id="ef668-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="ef668-128">**Required**</span></span>|<span data-ttu-id="ef668-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="ef668-129">**Description**</span></span>|<span data-ttu-id="ef668-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="ef668-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ef668-131">PageID</span><span class="sxs-lookup"><span data-stu-id="ef668-131">PageID</span></span>  <br/> |<span data-ttu-id="ef668-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ef668-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ef668-133">必須</span><span class="sxs-lookup"><span data-stu-id="ef668-133">required</span></span>  <br/> |<span data-ttu-id="ef668-134">競合に関連する図形のページの ID です。</span><span class="sxs-lookup"><span data-stu-id="ef668-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="ef668-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ef668-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ef668-136">RowID</span><span class="sxs-lookup"><span data-stu-id="ef668-136">RowID</span></span>  <br/> |<span data-ttu-id="ef668-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ef668-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ef668-138">必須</span><span class="sxs-lookup"><span data-stu-id="ef668-138">required</span></span>  <br/> |<span data-ttu-id="ef668-139">競合データが更新された後の現在の行の元の行の ID です。</span><span class="sxs-lookup"><span data-stu-id="ef668-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="ef668-140">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ef668-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ef668-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="ef668-141">ShapeID</span></span>  <br/> |<span data-ttu-id="ef668-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ef668-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ef668-143">必須</span><span class="sxs-lookup"><span data-stu-id="ef668-143">required</span></span>  <br/> |<span data-ttu-id="ef668-144">競合に関連する図形の図形 ID です。</span><span class="sxs-lookup"><span data-stu-id="ef668-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="ef668-145">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ef668-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

