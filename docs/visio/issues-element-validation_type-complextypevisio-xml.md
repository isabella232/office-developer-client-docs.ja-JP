---
title: 問題要素 (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: 文書のすべての Issue 要素を含みます。
ms.openlocfilehash: dced8ab94b51535a47415794954b5b3062963ede
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542941"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="f6298-103">問題要素 (Validation_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f6298-103">Issues element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f6298-104">文書のすべての Issue 要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="f6298-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f6298-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="f6298-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6298-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="f6298-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f6298-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="f6298-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f6298-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f6298-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f6298-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f6298-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f6298-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="f6298-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f6298-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="f6298-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f6298-112">検証 xml</span><span class="sxs-lookup"><span data-stu-id="f6298-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f6298-113">定義</span><span class="sxs-lookup"><span data-stu-id="f6298-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f6298-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f6298-114">Elements and attributes</span></span>

<span data-ttu-id="f6298-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6298-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f6298-116">親要素</span><span class="sxs-lookup"><span data-stu-id="f6298-116">Parent elements</span></span>

|<span data-ttu-id="f6298-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="f6298-117">**Element**</span></span>|<span data-ttu-id="f6298-118">**型**</span><span class="sxs-lookup"><span data-stu-id="f6298-118">**Type**</span></span>|<span data-ttu-id="f6298-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="f6298-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f6298-120">Validation</span><span class="sxs-lookup"><span data-stu-id="f6298-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="f6298-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="f6298-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f6298-122">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="f6298-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f6298-123">子要素</span><span class="sxs-lookup"><span data-stu-id="f6298-123">Child elements</span></span>

|<span data-ttu-id="f6298-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="f6298-124">**Element**</span></span>|<span data-ttu-id="f6298-125">**型**</span><span class="sxs-lookup"><span data-stu-id="f6298-125">**Type**</span></span>|<span data-ttu-id="f6298-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="f6298-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f6298-127">問題</span><span class="sxs-lookup"><span data-stu-id="f6298-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f6298-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="f6298-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f6298-129">文書内の1つの検証問題を表します。</span><span class="sxs-lookup"><span data-stu-id="f6298-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f6298-130">属性</span><span class="sxs-lookup"><span data-stu-id="f6298-130">Attributes</span></span>

<span data-ttu-id="f6298-131">なし。</span><span class="sxs-lookup"><span data-stu-id="f6298-131">None.</span></span>
  

