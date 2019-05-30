---
title: AutoLinkComparison 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: ユーザーインターフェイスで実行された前回正常に完了した自動リンクアクションの図形データ項目と親 DataRecordset 要素の列を比較するルールを定義します。
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537872"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="4498e-103">AutoLinkComparison 要素 (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4498e-103">AutoLinkComparison element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4498e-104">ユーザーインターフェイスで実行された前回正常に完了した自動リンクアクションの図形データ項目と親**DataRecordset**要素の列を比較するルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="4498e-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4498e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="4498e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4498e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4498e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4498e-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="4498e-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4498e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4498e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4498e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4498e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4498e-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="4498e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4498e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="4498e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4498e-112">recordsets</span><span class="sxs-lookup"><span data-stu-id="4498e-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4498e-113">定義</span><span class="sxs-lookup"><span data-stu-id="4498e-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4498e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4498e-114">Elements and attributes</span></span>

<span data-ttu-id="4498e-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4498e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4498e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4498e-116">Parent elements</span></span>

|<span data-ttu-id="4498e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="4498e-117">**Element**</span></span>|<span data-ttu-id="4498e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="4498e-118">**Type**</span></span>|<span data-ttu-id="4498e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="4498e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4498e-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="4498e-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4498e-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="4498e-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4498e-122">レコードセット、およびその recordset と図面ページの図形との間のデータバインドを指定します。</span><span class="sxs-lookup"><span data-stu-id="4498e-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4498e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="4498e-123">Child elements</span></span>

<span data-ttu-id="4498e-124">なし。</span><span class="sxs-lookup"><span data-stu-id="4498e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4498e-125">属性</span><span class="sxs-lookup"><span data-stu-id="4498e-125">Attributes</span></span>

|<span data-ttu-id="4498e-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="4498e-126">**Attribute**</span></span>|<span data-ttu-id="4498e-127">**型**</span><span class="sxs-lookup"><span data-stu-id="4498e-127">**Type**</span></span>|<span data-ttu-id="4498e-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="4498e-128">**Required**</span></span>|<span data-ttu-id="4498e-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="4498e-129">**Description**</span></span>|<span data-ttu-id="4498e-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="4498e-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4498e-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="4498e-131">ColumnName</span></span>  <br/> |<span data-ttu-id="4498e-132">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4498e-132">xsd:string</span></span>  <br/> |<span data-ttu-id="4498e-133">必須</span><span class="sxs-lookup"><span data-stu-id="4498e-133">required</span></span>  <br/> |<span data-ttu-id="4498e-134">ADO recordset の列名に対応します。</span><span class="sxs-lookup"><span data-stu-id="4498e-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="4498e-135">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="4498e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4498e-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="4498e-136">ContextType</span></span>  <br/> |<span data-ttu-id="4498e-137">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="4498e-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4498e-138">必須</span><span class="sxs-lookup"><span data-stu-id="4498e-138">required</span></span>  <br/> |<span data-ttu-id="4498e-139">比較に使用するグループまたは図形のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="4498e-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="4498e-140">使用可能な値を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="4498e-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="4498e-141">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="4498e-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4498e-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="4498e-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="4498e-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4498e-143">xsd:string</span></span>  <br/> |<span data-ttu-id="4498e-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="4498e-144">optional</span></span>  <br/> |<span data-ttu-id="4498e-145">ContextType の値が2または3の場合、比較を定義するためにこの属性が必要になります。</span><span class="sxs-lookup"><span data-stu-id="4498e-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="4498e-146">ContextType = 2 の場合、ContextTypeLabel は図形データ項目のラベルである必要があります。 **contexttype** = 3 の場合は、ContextTypeLabel がローカルの行名である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4498e-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="4498e-147">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="4498e-147">Values of the xsd:string type.</span></span>  <br/> |
   

