---
title: ValidationProperties 要素 (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: ドキュメントの検証に関連するプロパティをカプセル化します。
ms.openlocfilehash: 35e6f3f13eecef826fdef0d664bba35fceb0e069
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538523"
---
# <a name="validationproperties-element-validation_type-complextype-visio-xml"></a><span data-ttu-id="442c2-103">ValidationProperties 要素 (Validation_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="442c2-103">ValidationProperties element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="442c2-104">ドキュメントの検証に関連するプロパティをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="442c2-104">Encapsulates the properties that are related to the document's validation.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="442c2-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="442c2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="442c2-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="442c2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="442c2-107">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="442c2-107">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="442c2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="442c2-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="442c2-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="442c2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="442c2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="442c2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="442c2-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="442c2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="442c2-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="442c2-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="442c2-113">定義</span><span class="sxs-lookup"><span data-stu-id="442c2-113">Definition</span></span>

```XML
< xs:element name="ValidationProperties" type="ValidationProperties_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="442c2-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="442c2-114">Elements and attributes</span></span>

<span data-ttu-id="442c2-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="442c2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="442c2-116">親要素</span><span class="sxs-lookup"><span data-stu-id="442c2-116">Parent elements</span></span>

|<span data-ttu-id="442c2-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="442c2-117">**Element**</span></span>|<span data-ttu-id="442c2-118">**型**</span><span class="sxs-lookup"><span data-stu-id="442c2-118">**Type**</span></span>|<span data-ttu-id="442c2-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="442c2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="442c2-120">Validation</span><span class="sxs-lookup"><span data-stu-id="442c2-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="442c2-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="442c2-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="442c2-122">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="442c2-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="442c2-123">子要素</span><span class="sxs-lookup"><span data-stu-id="442c2-123">Child elements</span></span>

<span data-ttu-id="442c2-124">なし。</span><span class="sxs-lookup"><span data-stu-id="442c2-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="442c2-125">属性</span><span class="sxs-lookup"><span data-stu-id="442c2-125">Attributes</span></span>

|<span data-ttu-id="442c2-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="442c2-126">**Attribute**</span></span>|<span data-ttu-id="442c2-127">**型**</span><span class="sxs-lookup"><span data-stu-id="442c2-127">**Type**</span></span>|<span data-ttu-id="442c2-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="442c2-128">**Required**</span></span>|<span data-ttu-id="442c2-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="442c2-129">**Description**</span></span>|<span data-ttu-id="442c2-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="442c2-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="442c2-131">LastValidated</span><span class="sxs-lookup"><span data-stu-id="442c2-131">LastValidated</span></span>  <br/> |<span data-ttu-id="442c2-132">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="442c2-132">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="442c2-133">必須</span><span class="sxs-lookup"><span data-stu-id="442c2-133">required</span></span>  <br/> |<span data-ttu-id="442c2-134">ドキュメントが最後に検証された日時。</span><span class="sxs-lookup"><span data-stu-id="442c2-134">The date and time that the document was last validated.</span></span>  <br/> |<span data-ttu-id="442c2-135">xsd:dateTime type 型の値。</span><span class="sxs-lookup"><span data-stu-id="442c2-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="442c2-136">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="442c2-136">ShowIgnored</span></span>  <br/> |<span data-ttu-id="442c2-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="442c2-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="442c2-138">必須</span><span class="sxs-lookup"><span data-stu-id="442c2-138">required</span></span>  <br/> |<span data-ttu-id="442c2-139">[問題] ウィンドウに無視された検証の問題を表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="442c2-139">Specifies whether to show ignored validation issues in the Issues window.</span></span>  <br/> |<span data-ttu-id="442c2-140">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="442c2-140">Values of the xsd:boolean type.</span></span>  <br/> |
   

