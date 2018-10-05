---
title: AutoLinkComparison 要素 (DataRecordSet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: 前回成功した自動リンクで実行されたアクション ユーザー インターフェイスからの図形データ項目の親データ レコード セットの要素内の列を比較するルールを定義します。
ms.openlocfilehash: 474acc4c1d259621881ea498decfeaf18b69809e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385719"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="35d8e-103">AutoLinkComparison 要素 (DataRecordSet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="35d8e-103">AutoLinkComparison element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="35d8e-104">前回成功した自動リンクで実行されたアクション ユーザー インターフェイスからの図形データ項目の親**データ レコード セット**の要素内の列を比較するルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="35d8e-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="35d8e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="35d8e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35d8e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="35d8e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="35d8e-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="35d8e-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="35d8e-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="35d8e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="35d8e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="35d8e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="35d8e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="35d8e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="35d8e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="35d8e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="35d8e-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="35d8e-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="35d8e-113">定義</span><span class="sxs-lookup"><span data-stu-id="35d8e-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="35d8e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="35d8e-114">Elements and attributes</span></span>

<span data-ttu-id="35d8e-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="35d8e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="35d8e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="35d8e-116">Parent elements</span></span>

|<span data-ttu-id="35d8e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="35d8e-117">**Element**</span></span>|<span data-ttu-id="35d8e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="35d8e-118">**Type**</span></span>|<span data-ttu-id="35d8e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="35d8e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="35d8e-120">データ レコード セット</span><span class="sxs-lookup"><span data-stu-id="35d8e-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="35d8e-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="35d8e-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="35d8e-122">図面ページで、レコード セットとそのレコード セットと図形間のデータ バインディングを指定します。</span><span class="sxs-lookup"><span data-stu-id="35d8e-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="35d8e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="35d8e-123">Child elements</span></span>

<span data-ttu-id="35d8e-124">なし。</span><span class="sxs-lookup"><span data-stu-id="35d8e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35d8e-125">属性</span><span class="sxs-lookup"><span data-stu-id="35d8e-125">Attributes</span></span>

|<span data-ttu-id="35d8e-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="35d8e-126">**Attribute**</span></span>|<span data-ttu-id="35d8e-127">**型**</span><span class="sxs-lookup"><span data-stu-id="35d8e-127">**Type**</span></span>|<span data-ttu-id="35d8e-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="35d8e-128">**Required**</span></span>|<span data-ttu-id="35d8e-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="35d8e-129">**Description**</span></span>|<span data-ttu-id="35d8e-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="35d8e-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="35d8e-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="35d8e-131">ColumnName</span></span>  <br/> |<span data-ttu-id="35d8e-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="35d8e-132">xsd:string</span></span>  <br/> |<span data-ttu-id="35d8e-133">必須</span><span class="sxs-lookup"><span data-stu-id="35d8e-133">required</span></span>  <br/> |<span data-ttu-id="35d8e-134">ADO レコード セット内の列名に対応します。</span><span class="sxs-lookup"><span data-stu-id="35d8e-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="35d8e-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="35d8e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="35d8e-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="35d8e-136">ContextType</span></span>  <br/> |<span data-ttu-id="35d8e-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="35d8e-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="35d8e-138">必須</span><span class="sxs-lookup"><span data-stu-id="35d8e-138">required</span></span>  <br/> |<span data-ttu-id="35d8e-139">比較に使用するには、グループまたは図形のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="35d8e-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="35d8e-140">使用可能な値は、次の表に表示されます。</span><span class="sxs-lookup"><span data-stu-id="35d8e-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="35d8e-141">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="35d8e-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="35d8e-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="35d8e-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="35d8e-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="35d8e-143">xsd:string</span></span>  <br/> |<span data-ttu-id="35d8e-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="35d8e-144">optional</span></span>  <br/> |<span data-ttu-id="35d8e-145">ContextType の値が 2 または 3 の場合は、比較を定義するのにはこの属性が必要です。</span><span class="sxs-lookup"><span data-stu-id="35d8e-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="35d8e-146">ContextType = 2、ContextTypeLabel は、図形データ アイテムのラベルをして、場合必要があります。 **ContextType** = 3、ContextTypeLabel は、ローカル行の名前をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="35d8e-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="35d8e-147">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="35d8e-147">Values of the xsd:string type.</span></span>  <br/> |
   

