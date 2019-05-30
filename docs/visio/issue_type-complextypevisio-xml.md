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
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="00429-102">Issue_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="00429-102">Issue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="00429-103">型情報</span><span class="sxs-lookup"><span data-stu-id="00429-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00429-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="00429-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="00429-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="00429-105">**Schema file**</span></span> <br/> |<span data-ttu-id="00429-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="00429-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="00429-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="00429-107">**Extension base**</span></span> <br/> |<span data-ttu-id="00429-108">None</span><span class="sxs-lookup"><span data-stu-id="00429-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="00429-109">定義</span><span class="sxs-lookup"><span data-stu-id="00429-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="00429-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="00429-110">Elements and attributes</span></span>

<span data-ttu-id="00429-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="00429-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="00429-112">子要素</span><span class="sxs-lookup"><span data-stu-id="00429-112">Child elements</span></span>

|<span data-ttu-id="00429-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="00429-113">**Element**</span></span>|<span data-ttu-id="00429-114">**型**</span><span class="sxs-lookup"><span data-stu-id="00429-114">**Type**</span></span>|<span data-ttu-id="00429-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="00429-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="00429-116">"発信先"</span><span class="sxs-lookup"><span data-stu-id="00429-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="00429-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="00429-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="00429-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="00429-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="00429-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="00429-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="00429-120">属性</span><span class="sxs-lookup"><span data-stu-id="00429-120">Attributes</span></span>

|<span data-ttu-id="00429-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="00429-121">**Attribute**</span></span>|<span data-ttu-id="00429-122">**型**</span><span class="sxs-lookup"><span data-stu-id="00429-122">**Type**</span></span>|<span data-ttu-id="00429-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="00429-123">**Required**</span></span>|<span data-ttu-id="00429-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="00429-124">**Description**</span></span>|<span data-ttu-id="00429-125">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="00429-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="00429-126">ID</span><span class="sxs-lookup"><span data-stu-id="00429-126">ID</span></span>  <br/> |<span data-ttu-id="00429-127">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="00429-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="00429-128">必須</span><span class="sxs-lookup"><span data-stu-id="00429-128">required</span></span>  <br/> ||<span data-ttu-id="00429-129">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="00429-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="00429-130">Ignored</span><span class="sxs-lookup"><span data-stu-id="00429-130">Ignored</span></span>  <br/> |<span data-ttu-id="00429-131">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="00429-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="00429-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="00429-132">optional</span></span>  <br/> ||<span data-ttu-id="00429-133">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="00429-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

