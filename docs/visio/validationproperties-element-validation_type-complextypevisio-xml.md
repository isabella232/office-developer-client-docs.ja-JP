---
title: ValidationProperties 要素 (Validation_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: ドキュメントの検証に関連するプロパティをカプセル化します。
ms.openlocfilehash: 4f91160969cfb162f18440019ced23ea62061879
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806747"
---
# <a name="validationproperties-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="9ca99-103">ValidationProperties 要素 (Validation_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="9ca99-103">ValidationProperties element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9ca99-104">ドキュメントの検証に関連するプロパティをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="9ca99-104">Encapsulates the properties that are related to the document's validation.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9ca99-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="9ca99-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ca99-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="9ca99-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9ca99-107">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="9ca99-107">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9ca99-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="9ca99-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9ca99-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9ca99-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9ca99-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9ca99-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9ca99-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="9ca99-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9ca99-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="9ca99-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9ca99-113">定義</span><span class="sxs-lookup"><span data-stu-id="9ca99-113">Definition</span></span>

```XML
< xs:element name="ValidationProperties" type="ValidationProperties_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9ca99-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9ca99-114">Elements and attributes</span></span>

<span data-ttu-id="9ca99-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ca99-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9ca99-116">親要素</span><span class="sxs-lookup"><span data-stu-id="9ca99-116">Parent elements</span></span>

|<span data-ttu-id="9ca99-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="9ca99-117">**Element**</span></span>|<span data-ttu-id="9ca99-118">**型**</span><span class="sxs-lookup"><span data-stu-id="9ca99-118">**Type**</span></span>|<span data-ttu-id="9ca99-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="9ca99-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9ca99-120">検証</span><span class="sxs-lookup"><span data-stu-id="9ca99-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="9ca99-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="9ca99-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9ca99-122">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="9ca99-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9ca99-123">子要素</span><span class="sxs-lookup"><span data-stu-id="9ca99-123">Child elements</span></span>

<span data-ttu-id="9ca99-124">なし。</span><span class="sxs-lookup"><span data-stu-id="9ca99-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ca99-125">属性</span><span class="sxs-lookup"><span data-stu-id="9ca99-125">Attributes</span></span>

|<span data-ttu-id="9ca99-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="9ca99-126">**Attribute**</span></span>|<span data-ttu-id="9ca99-127">**型**</span><span class="sxs-lookup"><span data-stu-id="9ca99-127">**Type**</span></span>|<span data-ttu-id="9ca99-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="9ca99-128">**Required**</span></span>|<span data-ttu-id="9ca99-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="9ca99-129">**Description**</span></span>|<span data-ttu-id="9ca99-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="9ca99-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9ca99-131">LastValidated</span><span class="sxs-lookup"><span data-stu-id="9ca99-131">LastValidated</span></span>  <br/> |<span data-ttu-id="9ca99-132">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="9ca99-132">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="9ca99-133">必須</span><span class="sxs-lookup"><span data-stu-id="9ca99-133">required</span></span>  <br/> |<span data-ttu-id="9ca99-134">日付と時刻をドキュメントが最後に検証されました。</span><span class="sxs-lookup"><span data-stu-id="9ca99-134">The date and time that the document was last validated.</span></span>  <br/> |<span data-ttu-id="9ca99-135">Xsd:dateTime の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ca99-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="9ca99-136">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="9ca99-136">ShowIgnored</span></span>  <br/> |<span data-ttu-id="9ca99-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9ca99-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9ca99-138">必須</span><span class="sxs-lookup"><span data-stu-id="9ca99-138">required</span></span>  <br/> |<span data-ttu-id="9ca99-139">問題ウィンドウで無視される検証の問題を表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9ca99-139">Specifies whether to show ignored validation issues in the Issues window.</span></span>  <br/> |<span data-ttu-id="9ca99-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ca99-140">Values of the xsd:boolean type.</span></span>  <br/> |
   

