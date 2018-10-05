---
title: 問題の要素 (Validation_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: ドキュメントのすべての問題の要素が含まれています。
ms.openlocfilehash: da3156e34af1536fab39d3d4949acac1efe67264
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400580"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="71bbd-103">問題の要素 (Validation_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="71bbd-103">Issues element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="71bbd-104">ドキュメントのすべての問題の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71bbd-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="71bbd-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="71bbd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71bbd-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="71bbd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="71bbd-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="71bbd-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="71bbd-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="71bbd-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="71bbd-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="71bbd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="71bbd-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="71bbd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="71bbd-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="71bbd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="71bbd-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="71bbd-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="71bbd-113">定義</span><span class="sxs-lookup"><span data-stu-id="71bbd-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="71bbd-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="71bbd-114">Elements and attributes</span></span>

<span data-ttu-id="71bbd-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="71bbd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="71bbd-116">親要素</span><span class="sxs-lookup"><span data-stu-id="71bbd-116">Parent elements</span></span>

|<span data-ttu-id="71bbd-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="71bbd-117">**Element**</span></span>|<span data-ttu-id="71bbd-118">**型**</span><span class="sxs-lookup"><span data-stu-id="71bbd-118">**Type**</span></span>|<span data-ttu-id="71bbd-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="71bbd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="71bbd-120">検証</span><span class="sxs-lookup"><span data-stu-id="71bbd-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="71bbd-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="71bbd-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="71bbd-122">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="71bbd-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="71bbd-123">子要素</span><span class="sxs-lookup"><span data-stu-id="71bbd-123">Child elements</span></span>

|<span data-ttu-id="71bbd-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="71bbd-124">**Element**</span></span>|<span data-ttu-id="71bbd-125">**型**</span><span class="sxs-lookup"><span data-stu-id="71bbd-125">**Type**</span></span>|<span data-ttu-id="71bbd-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="71bbd-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="71bbd-127">問題</span><span class="sxs-lookup"><span data-stu-id="71bbd-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="71bbd-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="71bbd-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="71bbd-129">文書の 1 つの検証の問題を表します。</span><span class="sxs-lookup"><span data-stu-id="71bbd-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="71bbd-130">属性</span><span class="sxs-lookup"><span data-stu-id="71bbd-130">Attributes</span></span>

<span data-ttu-id="71bbd-131">なし。</span><span class="sxs-lookup"><span data-stu-id="71bbd-131">None.</span></span>
  

