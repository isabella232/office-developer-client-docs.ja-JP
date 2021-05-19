---
title: DataRecordSets 要素 (xml Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: ドキュメント内のすべての DataRecordset 要素を格納します。
ms.openlocfilehash: efa7d58eabc1b1192862dbbe090ddd5008947c1d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542444"
---
# <a name="datarecordsets-element-visio-xml"></a><span data-ttu-id="ff394-103">DataRecordSets 要素 (xml Visio)</span><span class="sxs-lookup"><span data-stu-id="ff394-103">DataRecordSets element (Visio XML)</span></span>

<span data-ttu-id="ff394-104">ドキュメント内のすべての **DataRecordset** 要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="ff394-104">Contains all the **DataRecordset** elements in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ff394-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="ff394-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff394-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="ff394-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ff394-107">DataRecordSets_Type</span><span class="sxs-lookup"><span data-stu-id="ff394-107">DataRecordSets_Type</span></span>](datarecordsets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ff394-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ff394-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ff394-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ff394-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ff394-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ff394-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ff394-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="ff394-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ff394-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="ff394-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ff394-113">定義</span><span class="sxs-lookup"><span data-stu-id="ff394-113">Definition</span></span>

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ff394-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ff394-114">Elements and attributes</span></span>

<span data-ttu-id="ff394-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ff394-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ff394-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ff394-116">Parent elements</span></span>

<span data-ttu-id="ff394-117">なし。</span><span class="sxs-lookup"><span data-stu-id="ff394-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ff394-118">子要素</span><span class="sxs-lookup"><span data-stu-id="ff394-118">Child elements</span></span>

|<span data-ttu-id="ff394-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff394-119">**Element**</span></span>|<span data-ttu-id="ff394-120">**型**</span><span class="sxs-lookup"><span data-stu-id="ff394-120">**Type**</span></span>|<span data-ttu-id="ff394-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="ff394-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ff394-122">DataRecordset</span><span class="sxs-lookup"><span data-stu-id="ff394-122">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ff394-123">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="ff394-123">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ff394-124">ドキュメント内のすべての **DataRecordset** 要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="ff394-124">Contains all the **DataRecordset** elements in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ff394-125">属性</span><span class="sxs-lookup"><span data-stu-id="ff394-125">Attributes</span></span>

|<span data-ttu-id="ff394-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="ff394-126">**Attribute**</span></span>|<span data-ttu-id="ff394-127">**型**</span><span class="sxs-lookup"><span data-stu-id="ff394-127">**Type**</span></span>|<span data-ttu-id="ff394-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="ff394-128">**Required**</span></span>|<span data-ttu-id="ff394-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="ff394-129">**Description**</span></span>|<span data-ttu-id="ff394-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="ff394-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ff394-131">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="ff394-131">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="ff394-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff394-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff394-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="ff394-133">optional</span></span>  <br/> |<span data-ttu-id="ff394-134">ウィンドウが閉じると、[外部データ]ウィンドウ内のアクティブ なデータ レコードセットの ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ff394-134">The ID of the active data recordset in the **External Data** window when the window closes, so that it can be restored the next time the window opens.</span></span>  <br/> |<span data-ttu-id="ff394-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="ff394-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff394-136">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="ff394-136">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="ff394-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ff394-137">xsd:string</span></span>  <br/> |<span data-ttu-id="ff394-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="ff394-138">optional</span></span>  <br/> |<span data-ttu-id="ff394-139">[外部データ] ウィンドウのタブに表示されるデータ レコードセット **の** 順序。</span><span class="sxs-lookup"><span data-stu-id="ff394-139">The order of the data recordsets displayed on the tabs of the **External Data** window.</span></span> <span data-ttu-id="ff394-140">セミコロンで区切られたデータ レコードセットの ID の順序付きリスト。</span><span class="sxs-lookup"><span data-stu-id="ff394-140">An ordered list of data-recordset IDs, separated by semi-colons.</span></span>  <br/> |<span data-ttu-id="ff394-141">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="ff394-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff394-142">NextID</span><span class="sxs-lookup"><span data-stu-id="ff394-142">NextID</span></span>  <br/> |<span data-ttu-id="ff394-143">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff394-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff394-144">必須</span><span class="sxs-lookup"><span data-stu-id="ff394-144">required</span></span>  <br/> |<span data-ttu-id="ff394-145">新しいデータ レコードセットの次の使用可能な ID。</span><span class="sxs-lookup"><span data-stu-id="ff394-145">The next available ID for a new data recordset.</span></span>  <br/> |<span data-ttu-id="ff394-146">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="ff394-146">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

