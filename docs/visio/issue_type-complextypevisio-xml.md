---
title: Issue_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: b351554fe7919cada99172f721f5dbe2fd8f243a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542962"
---
# <a name="issue_type-complextype-visio-xml"></a><span data-ttu-id="4b6a0-102">Issue_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4b6a0-102">Issue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="4b6a0-103">型情報</span><span class="sxs-lookup"><span data-stu-id="4b6a0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b6a0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4b6a0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4b6a0-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4b6a0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4b6a0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4b6a0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4b6a0-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="4b6a0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4b6a0-108">なし</span><span class="sxs-lookup"><span data-stu-id="4b6a0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4b6a0-109">定義</span><span class="sxs-lookup"><span data-stu-id="4b6a0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4b6a0-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4b6a0-110">Elements and attributes</span></span>

<span data-ttu-id="4b6a0-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b6a0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4b6a0-112">子要素</span><span class="sxs-lookup"><span data-stu-id="4b6a0-112">Child elements</span></span>

|<span data-ttu-id="4b6a0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4b6a0-113">**Element**</span></span>|<span data-ttu-id="4b6a0-114">**型**</span><span class="sxs-lookup"><span data-stu-id="4b6a0-114">**Type**</span></span>|<span data-ttu-id="4b6a0-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="4b6a0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4b6a0-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="4b6a0-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4b6a0-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="4b6a0-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4b6a0-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="4b6a0-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4b6a0-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="4b6a0-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4b6a0-120">属性</span><span class="sxs-lookup"><span data-stu-id="4b6a0-120">Attributes</span></span>

|<span data-ttu-id="4b6a0-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="4b6a0-121">**Attribute**</span></span>|<span data-ttu-id="4b6a0-122">**型**</span><span class="sxs-lookup"><span data-stu-id="4b6a0-122">**Type**</span></span>|<span data-ttu-id="4b6a0-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="4b6a0-123">**Required**</span></span>|<span data-ttu-id="4b6a0-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="4b6a0-124">**Description**</span></span>|<span data-ttu-id="4b6a0-125">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="4b6a0-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4b6a0-126">ID</span><span class="sxs-lookup"><span data-stu-id="4b6a0-126">ID</span></span>  <br/> |<span data-ttu-id="4b6a0-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4b6a0-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4b6a0-128">必須</span><span class="sxs-lookup"><span data-stu-id="4b6a0-128">required</span></span>  <br/> ||<span data-ttu-id="4b6a0-129">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="4b6a0-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4b6a0-130">無視</span><span class="sxs-lookup"><span data-stu-id="4b6a0-130">Ignored</span></span>  <br/> |<span data-ttu-id="4b6a0-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="4b6a0-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4b6a0-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="4b6a0-132">optional</span></span>  <br/> ||<span data-ttu-id="4b6a0-133">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="4b6a0-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

