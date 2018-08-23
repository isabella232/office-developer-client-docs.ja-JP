---
title: AutoLinkComparison 要素 (DataRecordSet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: 前回成功した自動リンクで実行されたアクション ユーザー インターフェイスからの図形データ項目の親データ レコード セットの要素内の列を比較するルールを定義します。
ms.openlocfilehash: 38970a84676f769c36c9bdc3f8334652f7d9ec21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804800"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="18684-103">AutoLinkComparison 要素 (DataRecordSet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="18684-103">AutoLinkComparison element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="18684-104">前回成功した自動リンクで実行されたアクション ユーザー インターフェイスからの図形データ項目の親**データ レコード セット**の要素内の列を比較するルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="18684-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="18684-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="18684-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18684-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="18684-106">**Element type**</span></span> <br/> |[<span data-ttu-id="18684-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="18684-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="18684-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="18684-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="18684-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="18684-109">**Schema file**</span></span> <br/> |<span data-ttu-id="18684-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="18684-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="18684-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="18684-111">**Document parts**</span></span> <br/> |<span data-ttu-id="18684-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="18684-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="18684-113">定義</span><span class="sxs-lookup"><span data-stu-id="18684-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="18684-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="18684-114">Elements and attributes</span></span>

<span data-ttu-id="18684-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="18684-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="18684-116">親要素</span><span class="sxs-lookup"><span data-stu-id="18684-116">Parent elements</span></span>

|<span data-ttu-id="18684-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="18684-117">**Element**</span></span>|<span data-ttu-id="18684-118">**型**</span><span class="sxs-lookup"><span data-stu-id="18684-118">**Type**</span></span>|<span data-ttu-id="18684-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="18684-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="18684-120">データ レコード セット</span><span class="sxs-lookup"><span data-stu-id="18684-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="18684-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="18684-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="18684-122">図面ページで、レコード セットとそのレコード セットと図形間のデータ バインディングを指定します。</span><span class="sxs-lookup"><span data-stu-id="18684-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="18684-123">子要素</span><span class="sxs-lookup"><span data-stu-id="18684-123">Child elements</span></span>

<span data-ttu-id="18684-124">なし。</span><span class="sxs-lookup"><span data-stu-id="18684-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18684-125">属性</span><span class="sxs-lookup"><span data-stu-id="18684-125">Attributes</span></span>

|<span data-ttu-id="18684-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="18684-126">**Attribute**</span></span>|<span data-ttu-id="18684-127">**型**</span><span class="sxs-lookup"><span data-stu-id="18684-127">**Type**</span></span>|<span data-ttu-id="18684-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="18684-128">**Required**</span></span>|<span data-ttu-id="18684-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="18684-129">**Description**</span></span>|<span data-ttu-id="18684-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="18684-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="18684-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="18684-131">ColumnName</span></span>  <br/> |<span data-ttu-id="18684-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="18684-132">xsd:string</span></span>  <br/> |<span data-ttu-id="18684-133">必須</span><span class="sxs-lookup"><span data-stu-id="18684-133">required</span></span>  <br/> |<span data-ttu-id="18684-134">ADO レコード セット内の列名に対応します。</span><span class="sxs-lookup"><span data-stu-id="18684-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="18684-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18684-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="18684-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="18684-136">ContextType</span></span>  <br/> |<span data-ttu-id="18684-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="18684-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="18684-138">必須</span><span class="sxs-lookup"><span data-stu-id="18684-138">required</span></span>  <br/> |<span data-ttu-id="18684-139">比較に使用するには、グループまたは図形のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="18684-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="18684-140">使用可能な値は、次の表に表示されます。</span><span class="sxs-lookup"><span data-stu-id="18684-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="18684-141">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18684-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="18684-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="18684-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="18684-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="18684-143">xsd:string</span></span>  <br/> |<span data-ttu-id="18684-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="18684-144">optional</span></span>  <br/> |<span data-ttu-id="18684-145">ContextType の値が 2 または 3 の場合は、比較を定義するのにはこの属性が必要です。</span><span class="sxs-lookup"><span data-stu-id="18684-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="18684-146">ContextType = 2、ContextTypeLabel は、図形データ アイテムのラベルをして、場合必要があります。 **ContextType** = 3、ContextTypeLabel は、ローカル行の名前をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="18684-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="18684-147">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18684-147">Values of the xsd:string type.</span></span>  <br/> |
   

