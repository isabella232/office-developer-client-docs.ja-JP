---
title: AutoLinkComparison 要素 (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: ユーザーインターフェイスで実行された前回正常に完了した自動リンクアクションの図形データ項目と親 DataRecordset 要素の列を比較するルールを定義します。
ms.openlocfilehash: 474acc4c1d259621881ea498decfeaf18b69809e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338319"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="4ceb4-103">AutoLinkComparison 要素 (DataRecordSet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="4ceb4-103">AutoLinkComparison element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4ceb4-104">ユーザーインターフェイスで実行された前回正常に完了した自動リンクアクションの図形データ項目と親**DataRecordset**要素の列を比較するルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="4ceb4-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4ceb4-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="4ceb4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ceb4-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4ceb4-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="4ceb4-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4ceb4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4ceb4-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4ceb4-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="4ceb4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4ceb4-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4ceb4-112">recordsets</span><span class="sxs-lookup"><span data-stu-id="4ceb4-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4ceb4-113">定義</span><span class="sxs-lookup"><span data-stu-id="4ceb4-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4ceb4-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4ceb4-114">Elements and attributes</span></span>

<span data-ttu-id="4ceb4-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ceb4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4ceb4-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4ceb4-116">Parent elements</span></span>

|<span data-ttu-id="4ceb4-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-117">**Element**</span></span>|<span data-ttu-id="4ceb4-118">**型**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-118">**Type**</span></span>|<span data-ttu-id="4ceb4-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4ceb4-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="4ceb4-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4ceb4-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="4ceb4-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4ceb4-122">レコードセット、およびその recordset と図面ページの図形との間のデータバインドを指定します。</span><span class="sxs-lookup"><span data-stu-id="4ceb4-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4ceb4-123">子要素</span><span class="sxs-lookup"><span data-stu-id="4ceb4-123">Child elements</span></span>

<span data-ttu-id="4ceb4-124">なし。</span><span class="sxs-lookup"><span data-stu-id="4ceb4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ceb4-125">属性</span><span class="sxs-lookup"><span data-stu-id="4ceb4-125">Attributes</span></span>

|<span data-ttu-id="4ceb4-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-126">**Attribute**</span></span>|<span data-ttu-id="4ceb4-127">**型**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-127">**Type**</span></span>|<span data-ttu-id="4ceb4-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-128">**Required**</span></span>|<span data-ttu-id="4ceb4-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-129">**Description**</span></span>|<span data-ttu-id="4ceb4-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="4ceb4-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4ceb4-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="4ceb4-131">ColumnName</span></span>  <br/> |<span data-ttu-id="4ceb4-132">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4ceb4-132">xsd:string</span></span>  <br/> |<span data-ttu-id="4ceb4-133">必須</span><span class="sxs-lookup"><span data-stu-id="4ceb4-133">required</span></span>  <br/> |<span data-ttu-id="4ceb4-134">ADO recordset の列名に対応します。</span><span class="sxs-lookup"><span data-stu-id="4ceb4-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="4ceb4-135">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="4ceb4-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4ceb4-136">contexttype</span><span class="sxs-lookup"><span data-stu-id="4ceb4-136">ContextType</span></span>  <br/> |<span data-ttu-id="4ceb4-137">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="4ceb4-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4ceb4-138">必須</span><span class="sxs-lookup"><span data-stu-id="4ceb4-138">required</span></span>  <br/> |<span data-ttu-id="4ceb4-139">比較に使用するグループまたは図形のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="4ceb4-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="4ceb4-140">使用可能な値を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="4ceb4-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="4ceb4-141">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="4ceb4-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4ceb4-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="4ceb4-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="4ceb4-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4ceb4-143">xsd:string</span></span>  <br/> |<span data-ttu-id="4ceb4-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="4ceb4-144">optional</span></span>  <br/> |<span data-ttu-id="4ceb4-145">contexttype の値が2または3の場合、比較を定義するためにこの属性が必要になります。</span><span class="sxs-lookup"><span data-stu-id="4ceb4-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="4ceb4-146">contexttype = 2 の場合、ContextTypeLabel は図形データ項目のラベルである必要があります。 **contexttype** = 3 の場合は、ContextTypeLabel がローカルの行名である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ceb4-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="4ceb4-147">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="4ceb4-147">Values of the xsd:string type.</span></span>  <br/> |
   

