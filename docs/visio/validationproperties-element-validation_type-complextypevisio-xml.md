---
title: validationproperties 要素 (Validation_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: ドキュメントの検証に関連するプロパティをカプセル化します。
ms.openlocfilehash: 9eccb85bd7463411d81c867eda3216d6c9a207f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355959"
---
# <a name="validationproperties-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="1b4c6-103">validationproperties 要素 (Validation_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1b4c6-103">ValidationProperties element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1b4c6-104">ドキュメントの検証に関連するプロパティをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="1b4c6-104">Encapsulates the properties that are related to the document's validation.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b4c6-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="1b4c6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b4c6-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="1b4c6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1b4c6-107">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="1b4c6-107">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1b4c6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1b4c6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1b4c6-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1b4c6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1b4c6-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="1b4c6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1b4c6-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="1b4c6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1b4c6-112">検証 xml</span><span class="sxs-lookup"><span data-stu-id="1b4c6-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1b4c6-113">定義</span><span class="sxs-lookup"><span data-stu-id="1b4c6-113">Definition</span></span>

```XML
< xs:element name="ValidationProperties" type="ValidationProperties_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1b4c6-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1b4c6-114">Elements and attributes</span></span>

<span data-ttu-id="1b4c6-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b4c6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1b4c6-116">親要素</span><span class="sxs-lookup"><span data-stu-id="1b4c6-116">Parent elements</span></span>

|<span data-ttu-id="1b4c6-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="1b4c6-117">**Element**</span></span>|<span data-ttu-id="1b4c6-118">**型**</span><span class="sxs-lookup"><span data-stu-id="1b4c6-118">**Type**</span></span>|<span data-ttu-id="1b4c6-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="1b4c6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1b4c6-120">Validation</span><span class="sxs-lookup"><span data-stu-id="1b4c6-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="1b4c6-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="1b4c6-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1b4c6-122">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="1b4c6-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1b4c6-123">子要素</span><span class="sxs-lookup"><span data-stu-id="1b4c6-123">Child elements</span></span>

<span data-ttu-id="1b4c6-124">なし。</span><span class="sxs-lookup"><span data-stu-id="1b4c6-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b4c6-125">属性</span><span class="sxs-lookup"><span data-stu-id="1b4c6-125">Attributes</span></span>

|<span data-ttu-id="1b4c6-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="1b4c6-126">**Attribute**</span></span>|<span data-ttu-id="1b4c6-127">**型**</span><span class="sxs-lookup"><span data-stu-id="1b4c6-127">**Type**</span></span>|<span data-ttu-id="1b4c6-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="1b4c6-128">**Required**</span></span>|<span data-ttu-id="1b4c6-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="1b4c6-129">**Description**</span></span>|<span data-ttu-id="1b4c6-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="1b4c6-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1b4c6-131">lastvalidated</span><span class="sxs-lookup"><span data-stu-id="1b4c6-131">LastValidated</span></span>  <br/> |<span data-ttu-id="1b4c6-132">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="1b4c6-132">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="1b4c6-133">必須</span><span class="sxs-lookup"><span data-stu-id="1b4c6-133">required</span></span>  <br/> |<span data-ttu-id="1b4c6-134">ドキュメントが最後に検証された日時。</span><span class="sxs-lookup"><span data-stu-id="1b4c6-134">The date and time that the document was last validated.</span></span>  <br/> |<span data-ttu-id="1b4c6-135">xsd: dateTime 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b4c6-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="1b4c6-136">showignored</span><span class="sxs-lookup"><span data-stu-id="1b4c6-136">ShowIgnored</span></span>  <br/> |<span data-ttu-id="1b4c6-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="1b4c6-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1b4c6-138">必須</span><span class="sxs-lookup"><span data-stu-id="1b4c6-138">required</span></span>  <br/> |<span data-ttu-id="1b4c6-139">[問題] ウィンドウに、無視する検証の問題を表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="1b4c6-139">Specifies whether to show ignored validation issues in the Issues window.</span></span>  <br/> |<span data-ttu-id="1b4c6-140">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b4c6-140">Values of the xsd:boolean type.</span></span>  <br/> |
   

