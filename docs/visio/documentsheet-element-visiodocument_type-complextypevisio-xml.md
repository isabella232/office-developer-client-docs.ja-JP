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
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="14763-103">DocumentSheet 要素 (VisioDocument_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="14763-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="14763-104">DocumentSheet 構造体を指定します。</span><span class="sxs-lookup"><span data-stu-id="14763-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14763-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="14763-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14763-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="14763-106">**Element type**</span></span> <br/> |[<span data-ttu-id="14763-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="14763-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="14763-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="14763-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="14763-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="14763-109">**Schema file**</span></span> <br/> |<span data-ttu-id="14763-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="14763-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="14763-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="14763-111">**Document parts**</span></span> <br/> |<span data-ttu-id="14763-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="14763-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="14763-113">定義</span><span class="sxs-lookup"><span data-stu-id="14763-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="14763-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="14763-114">Elements and attributes</span></span>

<span data-ttu-id="14763-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="14763-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="14763-116">親要素</span><span class="sxs-lookup"><span data-stu-id="14763-116">Parent elements</span></span>

|<span data-ttu-id="14763-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="14763-117">**Element**</span></span>|<span data-ttu-id="14763-118">**型**</span><span class="sxs-lookup"><span data-stu-id="14763-118">**Type**</span></span>|<span data-ttu-id="14763-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="14763-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="14763-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="14763-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="14763-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="14763-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="14763-122">Microsoft Visio ドキュメントのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="14763-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="14763-123">子要素</span><span class="sxs-lookup"><span data-stu-id="14763-123">Child elements</span></span>

|<span data-ttu-id="14763-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="14763-124">**Element**</span></span>|<span data-ttu-id="14763-125">**型**</span><span class="sxs-lookup"><span data-stu-id="14763-125">**Type**</span></span>|<span data-ttu-id="14763-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="14763-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="14763-127">Cell</span><span class="sxs-lookup"><span data-stu-id="14763-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="14763-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="14763-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="14763-129">DocumentSheet でセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="14763-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="14763-130">属性</span><span class="sxs-lookup"><span data-stu-id="14763-130">Attributes</span></span>

|<span data-ttu-id="14763-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="14763-131">**Attribute**</span></span>|<span data-ttu-id="14763-132">**型**</span><span class="sxs-lookup"><span data-stu-id="14763-132">**Type**</span></span>|<span data-ttu-id="14763-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="14763-133">**Required**</span></span>|<span data-ttu-id="14763-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="14763-134">**Description**</span></span>|<span data-ttu-id="14763-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="14763-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="14763-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="14763-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="14763-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="14763-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="14763-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="14763-138">optional</span></span>  <br/> |<span data-ttu-id="14763-139">名前がユーザーによってカスタマイズされているかどうかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="14763-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="14763-140">Xsd:Boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="14763-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="14763-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="14763-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="14763-142">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="14763-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="14763-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="14763-143">optional</span></span>  <br/> |<span data-ttu-id="14763-144">汎用名がユーザーによってカスタマイズされているかどうかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="14763-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="14763-145">Xsd:Boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="14763-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="14763-146">名前</span><span class="sxs-lookup"><span data-stu-id="14763-146">Name</span></span>  <br/> |<span data-ttu-id="14763-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="14763-147">xsd:string</span></span>  <br/> |<span data-ttu-id="14763-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="14763-148">optional</span></span>  <br/> |<span data-ttu-id="14763-149">DocumentSheet の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="14763-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="14763-150">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="14763-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="14763-151">NameU</span><span class="sxs-lookup"><span data-stu-id="14763-151">NameU</span></span>  <br/> |<span data-ttu-id="14763-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="14763-152">xsd:string</span></span>  <br/> |<span data-ttu-id="14763-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="14763-153">optional</span></span>  <br/> |<span data-ttu-id="14763-154">DocumentSheet の言語に依存しない名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="14763-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="14763-155">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="14763-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="14763-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="14763-156">UniqueID</span></span>  <br/> |<span data-ttu-id="14763-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="14763-157">xsd:string</span></span>  <br/> |<span data-ttu-id="14763-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="14763-158">optional</span></span>  <br/> |<span data-ttu-id="14763-159">オプションの string。</span><span class="sxs-lookup"><span data-stu-id="14763-159">Optional string.</span></span> <span data-ttu-id="14763-160">図形を識別する GUID (グローバルに一意の識別子)。</span><span class="sxs-lookup"><span data-stu-id="14763-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="14763-161">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="14763-161">Values of the xsd:string type.</span></span>  <br/> |
   

