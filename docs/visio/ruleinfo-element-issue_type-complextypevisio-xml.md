---
title: RuleInfo 要素 (Issue_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: 親の検証の問題に関連する入力規則に関する情報を指定します。
ms.openlocfilehash: ff5a7e4e8918d5ae151a0d4582d1a393509e1b64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806314"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="6c063-103">RuleInfo 要素 (Issue_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="6c063-103">RuleInfo element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6c063-104">親の検証の問題に関連する入力規則に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="6c063-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c063-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="6c063-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c063-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="6c063-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6c063-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="6c063-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6c063-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="6c063-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6c063-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6c063-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6c063-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6c063-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6c063-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="6c063-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6c063-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="6c063-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6c063-113">定義</span><span class="sxs-lookup"><span data-stu-id="6c063-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6c063-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6c063-114">Elements and attributes</span></span>

<span data-ttu-id="6c063-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c063-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6c063-116">親要素</span><span class="sxs-lookup"><span data-stu-id="6c063-116">Parent elements</span></span>

|<span data-ttu-id="6c063-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="6c063-117">**Element**</span></span>|<span data-ttu-id="6c063-118">**型**</span><span class="sxs-lookup"><span data-stu-id="6c063-118">**Type**</span></span>|<span data-ttu-id="6c063-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="6c063-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6c063-120">問題</span><span class="sxs-lookup"><span data-stu-id="6c063-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6c063-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="6c063-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6c063-122">文書の 1 つの検証の問題を表します。</span><span class="sxs-lookup"><span data-stu-id="6c063-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6c063-123">子要素</span><span class="sxs-lookup"><span data-stu-id="6c063-123">Child elements</span></span>

<span data-ttu-id="6c063-124">なし。</span><span class="sxs-lookup"><span data-stu-id="6c063-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c063-125">属性</span><span class="sxs-lookup"><span data-stu-id="6c063-125">Attributes</span></span>

|<span data-ttu-id="6c063-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="6c063-126">**Attribute**</span></span>|<span data-ttu-id="6c063-127">**型**</span><span class="sxs-lookup"><span data-stu-id="6c063-127">**Type**</span></span>|<span data-ttu-id="6c063-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="6c063-128">**Required**</span></span>|<span data-ttu-id="6c063-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="6c063-129">**Description**</span></span>|<span data-ttu-id="6c063-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="6c063-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6c063-131">規則 Id</span><span class="sxs-lookup"><span data-stu-id="6c063-131">RuleID</span></span>  <br/> |<span data-ttu-id="6c063-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6c063-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6c063-133">必須</span><span class="sxs-lookup"><span data-stu-id="6c063-133">required</span></span>  <br/> |<span data-ttu-id="6c063-134">親の問題が関連する入力規則の一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="6c063-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="6c063-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6c063-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6c063-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="6c063-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="6c063-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6c063-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6c063-138">必須</span><span class="sxs-lookup"><span data-stu-id="6c063-138">required</span></span>  <br/> |<span data-ttu-id="6c063-139">親の問題が関連する検証規則のセットの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="6c063-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="6c063-140">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6c063-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

