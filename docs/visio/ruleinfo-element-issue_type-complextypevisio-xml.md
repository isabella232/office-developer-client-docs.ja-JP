---
title: RuleInfo 要素 (Issue_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: 親の検証の問題に関連する入力規則に関する情報を指定します。
ms.openlocfilehash: f0cf726f0c5d6943ef72669aa92f361a7367459c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394749"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="c3675-103">RuleInfo 要素 (Issue_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="c3675-103">RuleInfo element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c3675-104">親の検証の問題に関連する入力規則に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="c3675-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c3675-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="c3675-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3675-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="c3675-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c3675-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="c3675-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c3675-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="c3675-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c3675-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c3675-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c3675-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c3675-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c3675-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="c3675-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c3675-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="c3675-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c3675-113">定義</span><span class="sxs-lookup"><span data-stu-id="c3675-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c3675-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c3675-114">Elements and attributes</span></span>

<span data-ttu-id="c3675-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3675-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c3675-116">親要素</span><span class="sxs-lookup"><span data-stu-id="c3675-116">Parent elements</span></span>

|<span data-ttu-id="c3675-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="c3675-117">**Element**</span></span>|<span data-ttu-id="c3675-118">**型**</span><span class="sxs-lookup"><span data-stu-id="c3675-118">**Type**</span></span>|<span data-ttu-id="c3675-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="c3675-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c3675-120">問題</span><span class="sxs-lookup"><span data-stu-id="c3675-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3675-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="c3675-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c3675-122">文書の 1 つの検証の問題を表します。</span><span class="sxs-lookup"><span data-stu-id="c3675-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c3675-123">子要素</span><span class="sxs-lookup"><span data-stu-id="c3675-123">Child elements</span></span>

<span data-ttu-id="c3675-124">なし。</span><span class="sxs-lookup"><span data-stu-id="c3675-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3675-125">属性</span><span class="sxs-lookup"><span data-stu-id="c3675-125">Attributes</span></span>

|<span data-ttu-id="c3675-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="c3675-126">**Attribute**</span></span>|<span data-ttu-id="c3675-127">**型**</span><span class="sxs-lookup"><span data-stu-id="c3675-127">**Type**</span></span>|<span data-ttu-id="c3675-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="c3675-128">**Required**</span></span>|<span data-ttu-id="c3675-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="c3675-129">**Description**</span></span>|<span data-ttu-id="c3675-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="c3675-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c3675-131">規則 Id</span><span class="sxs-lookup"><span data-stu-id="c3675-131">RuleID</span></span>  <br/> |<span data-ttu-id="c3675-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3675-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3675-133">必須</span><span class="sxs-lookup"><span data-stu-id="c3675-133">required</span></span>  <br/> |<span data-ttu-id="c3675-134">親の問題が関連する入力規則の一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="c3675-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="c3675-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3675-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3675-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="c3675-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="c3675-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3675-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3675-138">必須</span><span class="sxs-lookup"><span data-stu-id="c3675-138">required</span></span>  <br/> |<span data-ttu-id="c3675-139">親の問題が関連する検証規則のセットの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="c3675-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="c3675-140">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3675-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

