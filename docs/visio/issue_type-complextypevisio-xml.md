---
title: Issue_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: f0346c20e4a290819e3f23a0384a59b308a5e907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805654"
---
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="90697-102">Issue_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="90697-102">Issue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="90697-103">型情報</span><span class="sxs-lookup"><span data-stu-id="90697-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90697-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="90697-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="90697-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="90697-105">**Schema file**</span></span> <br/> |<span data-ttu-id="90697-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="90697-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="90697-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="90697-107">**Extension base**</span></span> <br/> |<span data-ttu-id="90697-108">なし</span><span class="sxs-lookup"><span data-stu-id="90697-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="90697-109">定義</span><span class="sxs-lookup"><span data-stu-id="90697-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="90697-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="90697-110">Elements and attributes</span></span>

<span data-ttu-id="90697-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="90697-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="90697-112">子要素</span><span class="sxs-lookup"><span data-stu-id="90697-112">Child elements</span></span>

|<span data-ttu-id="90697-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="90697-113">**Element**</span></span>|<span data-ttu-id="90697-114">**型**</span><span class="sxs-lookup"><span data-stu-id="90697-114">**Type**</span></span>|<span data-ttu-id="90697-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="90697-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="90697-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="90697-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90697-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="90697-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="90697-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="90697-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90697-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="90697-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="90697-120">属性</span><span class="sxs-lookup"><span data-stu-id="90697-120">Attributes</span></span>

|<span data-ttu-id="90697-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="90697-121">**Attribute**</span></span>|<span data-ttu-id="90697-122">**型**</span><span class="sxs-lookup"><span data-stu-id="90697-122">**Type**</span></span>|<span data-ttu-id="90697-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="90697-123">**Required**</span></span>|<span data-ttu-id="90697-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="90697-124">**Description**</span></span>|<span data-ttu-id="90697-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="90697-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="90697-126">ID</span><span class="sxs-lookup"><span data-stu-id="90697-126">ID</span></span>  <br/> |<span data-ttu-id="90697-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="90697-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="90697-128">必須</span><span class="sxs-lookup"><span data-stu-id="90697-128">required</span></span>  <br/> ||<span data-ttu-id="90697-129">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="90697-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="90697-130">無視</span><span class="sxs-lookup"><span data-stu-id="90697-130">Ignored</span></span>  <br/> |<span data-ttu-id="90697-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="90697-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="90697-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="90697-132">optional</span></span>  <br/> ||<span data-ttu-id="90697-133">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="90697-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

