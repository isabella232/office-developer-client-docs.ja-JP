---
title: 問題の要素 (Validation_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: ドキュメントのすべての問題の要素が含まれています。
ms.openlocfilehash: 9205bf014c81aa699b8bc4a2a7412c5ce59c5fd0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805622"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="ea00b-103">問題の要素 (Validation_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="ea00b-103">Issues element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ea00b-104">ドキュメントのすべての問題の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ea00b-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ea00b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="ea00b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea00b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="ea00b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ea00b-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="ea00b-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ea00b-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="ea00b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ea00b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ea00b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ea00b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ea00b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ea00b-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="ea00b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ea00b-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="ea00b-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ea00b-113">定義</span><span class="sxs-lookup"><span data-stu-id="ea00b-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ea00b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ea00b-114">Elements and attributes</span></span>

<span data-ttu-id="ea00b-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea00b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ea00b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ea00b-116">Parent elements</span></span>

|<span data-ttu-id="ea00b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="ea00b-117">**Element**</span></span>|<span data-ttu-id="ea00b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="ea00b-118">**Type**</span></span>|<span data-ttu-id="ea00b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="ea00b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ea00b-120">検証</span><span class="sxs-lookup"><span data-stu-id="ea00b-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="ea00b-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="ea00b-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ea00b-122">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="ea00b-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ea00b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="ea00b-123">Child elements</span></span>

|<span data-ttu-id="ea00b-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="ea00b-124">**Element**</span></span>|<span data-ttu-id="ea00b-125">**型**</span><span class="sxs-lookup"><span data-stu-id="ea00b-125">**Type**</span></span>|<span data-ttu-id="ea00b-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="ea00b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ea00b-127">問題</span><span class="sxs-lookup"><span data-stu-id="ea00b-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ea00b-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="ea00b-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ea00b-129">文書の 1 つの検証の問題を表します。</span><span class="sxs-lookup"><span data-stu-id="ea00b-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ea00b-130">属性</span><span class="sxs-lookup"><span data-stu-id="ea00b-130">Attributes</span></span>

<span data-ttu-id="ea00b-131">なし。</span><span class="sxs-lookup"><span data-stu-id="ea00b-131">None.</span></span>
  

