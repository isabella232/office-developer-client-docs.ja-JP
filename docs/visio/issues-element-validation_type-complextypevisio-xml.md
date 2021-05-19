---
title: Issues 要素 (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: ドキュメントのすべての Issue 要素が含まれます。
ms.openlocfilehash: dced8ab94b51535a47415794954b5b3062963ede
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542941"
---
# <a name="issues-element-validation_type-complextype-visio-xml"></a><span data-ttu-id="2ca5b-103">Issues 要素 (Validation_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2ca5b-103">Issues element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="2ca5b-104">ドキュメントのすべての Issue 要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2ca5b-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ca5b-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="2ca5b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ca5b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="2ca5b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2ca5b-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="2ca5b-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2ca5b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2ca5b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2ca5b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="2ca5b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2ca5b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2ca5b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2ca5b-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="2ca5b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2ca5b-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="2ca5b-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2ca5b-113">定義</span><span class="sxs-lookup"><span data-stu-id="2ca5b-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2ca5b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="2ca5b-114">Elements and attributes</span></span>

<span data-ttu-id="2ca5b-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ca5b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2ca5b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="2ca5b-116">Parent elements</span></span>

|<span data-ttu-id="2ca5b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="2ca5b-117">**Element**</span></span>|<span data-ttu-id="2ca5b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="2ca5b-118">**Type**</span></span>|<span data-ttu-id="2ca5b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="2ca5b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2ca5b-120">Validation</span><span class="sxs-lookup"><span data-stu-id="2ca5b-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="2ca5b-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="2ca5b-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2ca5b-122">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="2ca5b-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2ca5b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="2ca5b-123">Child elements</span></span>

|<span data-ttu-id="2ca5b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="2ca5b-124">**Element**</span></span>|<span data-ttu-id="2ca5b-125">**型**</span><span class="sxs-lookup"><span data-stu-id="2ca5b-125">**Type**</span></span>|<span data-ttu-id="2ca5b-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="2ca5b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2ca5b-127">Issue</span><span class="sxs-lookup"><span data-stu-id="2ca5b-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2ca5b-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="2ca5b-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2ca5b-129">文書内の1つの検証問題を表します。</span><span class="sxs-lookup"><span data-stu-id="2ca5b-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2ca5b-130">属性</span><span class="sxs-lookup"><span data-stu-id="2ca5b-130">Attributes</span></span>

<span data-ttu-id="2ca5b-131">なし。</span><span class="sxs-lookup"><span data-stu-id="2ca5b-131">None.</span></span>
  

