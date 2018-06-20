---
title: DocumentSheet 要素 (VisioDocument_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: DocumentSheet 構造体を指定します。
ms.openlocfilehash: 50332759ff3bbe94887371d48c4a2e729243fb32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805275"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="a33dc-103">DocumentSheet 要素 (VisioDocument_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a33dc-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a33dc-104">DocumentSheet 構造体を指定します。</span><span class="sxs-lookup"><span data-stu-id="a33dc-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a33dc-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="a33dc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a33dc-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="a33dc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a33dc-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="a33dc-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a33dc-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a33dc-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a33dc-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a33dc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a33dc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a33dc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a33dc-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="a33dc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a33dc-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="a33dc-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a33dc-113">定義</span><span class="sxs-lookup"><span data-stu-id="a33dc-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a33dc-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a33dc-114">Elements and attributes</span></span>

<span data-ttu-id="a33dc-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a33dc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a33dc-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a33dc-116">Parent elements</span></span>

|<span data-ttu-id="a33dc-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a33dc-117">**Element**</span></span>|<span data-ttu-id="a33dc-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a33dc-118">**Type**</span></span>|<span data-ttu-id="a33dc-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a33dc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a33dc-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="a33dc-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="a33dc-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="a33dc-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a33dc-122">Microsoft Visio ドキュメントのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="a33dc-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a33dc-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a33dc-123">Child elements</span></span>

|<span data-ttu-id="a33dc-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="a33dc-124">**Element**</span></span>|<span data-ttu-id="a33dc-125">**型**</span><span class="sxs-lookup"><span data-stu-id="a33dc-125">**Type**</span></span>|<span data-ttu-id="a33dc-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="a33dc-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a33dc-127">Cell</span><span class="sxs-lookup"><span data-stu-id="a33dc-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="a33dc-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a33dc-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a33dc-129">DocumentSheet でセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="a33dc-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a33dc-130">属性</span><span class="sxs-lookup"><span data-stu-id="a33dc-130">Attributes</span></span>

|<span data-ttu-id="a33dc-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="a33dc-131">**Attribute**</span></span>|<span data-ttu-id="a33dc-132">**型**</span><span class="sxs-lookup"><span data-stu-id="a33dc-132">**Type**</span></span>|<span data-ttu-id="a33dc-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="a33dc-133">**Required**</span></span>|<span data-ttu-id="a33dc-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="a33dc-134">**Description**</span></span>|<span data-ttu-id="a33dc-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="a33dc-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a33dc-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="a33dc-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="a33dc-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a33dc-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a33dc-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="a33dc-138">optional</span></span>  <br/> |<span data-ttu-id="a33dc-139">名前がユーザーによってカスタマイズされているかどうかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a33dc-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="a33dc-140">Xsd:Boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a33dc-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="a33dc-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="a33dc-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="a33dc-142">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a33dc-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a33dc-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="a33dc-143">optional</span></span>  <br/> |<span data-ttu-id="a33dc-144">汎用名がユーザーによってカスタマイズされているかどうかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a33dc-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="a33dc-145">Xsd:Boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a33dc-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="a33dc-146">名前</span><span class="sxs-lookup"><span data-stu-id="a33dc-146">Name</span></span>  <br/> |<span data-ttu-id="a33dc-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a33dc-147">xsd:string</span></span>  <br/> |<span data-ttu-id="a33dc-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="a33dc-148">optional</span></span>  <br/> |<span data-ttu-id="a33dc-149">DocumentSheet の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="a33dc-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="a33dc-150">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a33dc-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a33dc-151">NameU</span><span class="sxs-lookup"><span data-stu-id="a33dc-151">NameU</span></span>  <br/> |<span data-ttu-id="a33dc-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a33dc-152">xsd:string</span></span>  <br/> |<span data-ttu-id="a33dc-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="a33dc-153">optional</span></span>  <br/> |<span data-ttu-id="a33dc-154">DocumentSheet の言語に依存しない名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="a33dc-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="a33dc-155">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a33dc-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a33dc-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="a33dc-156">UniqueID</span></span>  <br/> |<span data-ttu-id="a33dc-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a33dc-157">xsd:string</span></span>  <br/> |<span data-ttu-id="a33dc-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="a33dc-158">optional</span></span>  <br/> |<span data-ttu-id="a33dc-159">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="a33dc-159">Optional string.</span></span> <span data-ttu-id="a33dc-160">図形を識別する GUID (グローバルに一意の識別子)。</span><span class="sxs-lookup"><span data-stu-id="a33dc-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="a33dc-161">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a33dc-161">Values of the xsd:string type.</span></span>  <br/> |
   

