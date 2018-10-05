---
title: Issue_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: 1cdc38db93da57969230c280a2df24ac3b20ad0d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399699"
---
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="23a9d-102">Issue_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="23a9d-102">Issue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="23a9d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="23a9d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23a9d-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="23a9d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="23a9d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="23a9d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="23a9d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="23a9d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="23a9d-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="23a9d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="23a9d-108">なし</span><span class="sxs-lookup"><span data-stu-id="23a9d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="23a9d-109">定義</span><span class="sxs-lookup"><span data-stu-id="23a9d-109">Definition</span></span>

```XML
          <xs:complexType name="Issue_Type">
          
          <xs:sequence>
    <xs:element name="IssueTarget"  type="IssueTarget_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleInfo"  type="RuleInfo_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="23a9d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="23a9d-110">Elements and attributes</span></span>

<span data-ttu-id="23a9d-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="23a9d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="23a9d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="23a9d-112">Child elements</span></span>

|<span data-ttu-id="23a9d-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="23a9d-113">**Element**</span></span>|<span data-ttu-id="23a9d-114">**型**</span><span class="sxs-lookup"><span data-stu-id="23a9d-114">**Type**</span></span>|<span data-ttu-id="23a9d-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="23a9d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="23a9d-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="23a9d-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23a9d-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="23a9d-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23a9d-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="23a9d-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23a9d-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="23a9d-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="23a9d-120">属性</span><span class="sxs-lookup"><span data-stu-id="23a9d-120">Attributes</span></span>

|<span data-ttu-id="23a9d-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="23a9d-121">**Attribute**</span></span>|<span data-ttu-id="23a9d-122">**型**</span><span class="sxs-lookup"><span data-stu-id="23a9d-122">**Type**</span></span>|<span data-ttu-id="23a9d-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="23a9d-123">**Required**</span></span>|<span data-ttu-id="23a9d-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="23a9d-124">**Description**</span></span>|<span data-ttu-id="23a9d-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="23a9d-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="23a9d-126">ID</span><span class="sxs-lookup"><span data-stu-id="23a9d-126">ID</span></span>  <br/> |<span data-ttu-id="23a9d-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="23a9d-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="23a9d-128">必須</span><span class="sxs-lookup"><span data-stu-id="23a9d-128">required</span></span>  <br/> ||<span data-ttu-id="23a9d-129">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="23a9d-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="23a9d-130">無視</span><span class="sxs-lookup"><span data-stu-id="23a9d-130">Ignored</span></span>  <br/> |<span data-ttu-id="23a9d-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="23a9d-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="23a9d-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="23a9d-132">optional</span></span>  <br/> ||<span data-ttu-id="23a9d-133">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="23a9d-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

