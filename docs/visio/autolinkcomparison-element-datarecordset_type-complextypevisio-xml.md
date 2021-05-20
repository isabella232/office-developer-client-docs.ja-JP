---
title: AutoLinkComparison 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: ユーザー インターフェイスで最後に正常に実行された自動リンク アクションからの図形データ アイテムと、親 DataRecordset 要素内の列を比較するルールを定義します。
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537872"
---
# <a name="autolinkcomparison-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="fa9a6-103">AutoLinkComparison 要素 (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fa9a6-103">AutoLinkComparison element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="fa9a6-104">ユーザー インターフェイスで最後に正常に実行された自動リンク アクションからの図形データ アイテムと、親 **DataRecordset** 要素内の列を比較するルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fa9a6-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="fa9a6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa9a6-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="fa9a6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fa9a6-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="fa9a6-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fa9a6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fa9a6-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fa9a6-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="fa9a6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fa9a6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fa9a6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fa9a6-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="fa9a6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fa9a6-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="fa9a6-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fa9a6-113">定義</span><span class="sxs-lookup"><span data-stu-id="fa9a6-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fa9a6-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="fa9a6-114">Elements and attributes</span></span>

<span data-ttu-id="fa9a6-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fa9a6-116">親要素</span><span class="sxs-lookup"><span data-stu-id="fa9a6-116">Parent elements</span></span>

|<span data-ttu-id="fa9a6-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="fa9a6-117">**Element**</span></span>|<span data-ttu-id="fa9a6-118">**型**</span><span class="sxs-lookup"><span data-stu-id="fa9a6-118">**Type**</span></span>|<span data-ttu-id="fa9a6-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="fa9a6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fa9a6-120">DataRecordset</span><span class="sxs-lookup"><span data-stu-id="fa9a6-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fa9a6-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="fa9a6-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fa9a6-122">図面ページ内のレコードセットと図形間のレコードセットとデータ バインドを指定します。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fa9a6-123">子要素</span><span class="sxs-lookup"><span data-stu-id="fa9a6-123">Child elements</span></span>

<span data-ttu-id="fa9a6-124">なし。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa9a6-125">属性</span><span class="sxs-lookup"><span data-stu-id="fa9a6-125">Attributes</span></span>

|<span data-ttu-id="fa9a6-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="fa9a6-126">**Attribute**</span></span>|<span data-ttu-id="fa9a6-127">**型**</span><span class="sxs-lookup"><span data-stu-id="fa9a6-127">**Type**</span></span>|<span data-ttu-id="fa9a6-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="fa9a6-128">**Required**</span></span>|<span data-ttu-id="fa9a6-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="fa9a6-129">**Description**</span></span>|<span data-ttu-id="fa9a6-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="fa9a6-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fa9a6-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="fa9a6-131">ColumnName</span></span>  <br/> |<span data-ttu-id="fa9a6-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fa9a6-132">xsd:string</span></span>  <br/> |<span data-ttu-id="fa9a6-133">必須</span><span class="sxs-lookup"><span data-stu-id="fa9a6-133">required</span></span>  <br/> |<span data-ttu-id="fa9a6-134">ADO レコードセット内の列名に対応します。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="fa9a6-135">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fa9a6-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="fa9a6-136">ContextType</span></span>  <br/> |<span data-ttu-id="fa9a6-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fa9a6-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fa9a6-138">必須</span><span class="sxs-lookup"><span data-stu-id="fa9a6-138">required</span></span>  <br/> |<span data-ttu-id="fa9a6-139">比較に使用するグループまたは図形のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="fa9a6-140">使用できる値を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="fa9a6-141">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fa9a6-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="fa9a6-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="fa9a6-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fa9a6-143">xsd:string</span></span>  <br/> |<span data-ttu-id="fa9a6-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="fa9a6-144">optional</span></span>  <br/> |<span data-ttu-id="fa9a6-145">ContextType 値が 2 または 3 の場合、比較を定義するには、この属性が必要です。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="fa9a6-146">ContextType = 2 の場合、ContextTypeLabel は図形データ項目ラベルである必要があります **。ContextType** = 3 の場合、ContextTypeLabel はローカル行名である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="fa9a6-147">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="fa9a6-147">Values of the xsd:string type.</span></span>  <br/> |
   

