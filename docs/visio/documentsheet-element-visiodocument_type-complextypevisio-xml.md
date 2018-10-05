---
title: DocumentSheet 要素 (VisioDocument_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: DocumentSheet 構造体を指定します。
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383465"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="b245a-103">DocumentSheet 要素 (VisioDocument_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="b245a-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b245a-104">DocumentSheet 構造体を指定します。</span><span class="sxs-lookup"><span data-stu-id="b245a-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b245a-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="b245a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b245a-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="b245a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b245a-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="b245a-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b245a-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="b245a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b245a-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b245a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b245a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b245a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b245a-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="b245a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b245a-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="b245a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b245a-113">定義</span><span class="sxs-lookup"><span data-stu-id="b245a-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b245a-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b245a-114">Elements and attributes</span></span>

<span data-ttu-id="b245a-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b245a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b245a-116">親要素</span><span class="sxs-lookup"><span data-stu-id="b245a-116">Parent elements</span></span>

|<span data-ttu-id="b245a-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="b245a-117">**Element**</span></span>|<span data-ttu-id="b245a-118">**型**</span><span class="sxs-lookup"><span data-stu-id="b245a-118">**Type**</span></span>|<span data-ttu-id="b245a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="b245a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b245a-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="b245a-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="b245a-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="b245a-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b245a-122">Microsoft Visio ドキュメントのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="b245a-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b245a-123">子要素</span><span class="sxs-lookup"><span data-stu-id="b245a-123">Child elements</span></span>

|<span data-ttu-id="b245a-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="b245a-124">**Element**</span></span>|<span data-ttu-id="b245a-125">**型**</span><span class="sxs-lookup"><span data-stu-id="b245a-125">**Type**</span></span>|<span data-ttu-id="b245a-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="b245a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b245a-127">Cell</span><span class="sxs-lookup"><span data-stu-id="b245a-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="b245a-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="b245a-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b245a-129">DocumentSheet でセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="b245a-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b245a-130">属性</span><span class="sxs-lookup"><span data-stu-id="b245a-130">Attributes</span></span>

|<span data-ttu-id="b245a-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="b245a-131">**Attribute**</span></span>|<span data-ttu-id="b245a-132">**型**</span><span class="sxs-lookup"><span data-stu-id="b245a-132">**Type**</span></span>|<span data-ttu-id="b245a-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="b245a-133">**Required**</span></span>|<span data-ttu-id="b245a-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="b245a-134">**Description**</span></span>|<span data-ttu-id="b245a-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="b245a-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b245a-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="b245a-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="b245a-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="b245a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b245a-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="b245a-138">optional</span></span>  <br/> |<span data-ttu-id="b245a-139">名前がユーザーによってカスタマイズされているかどうかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b245a-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="b245a-140">Xsd:Boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b245a-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="b245a-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="b245a-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="b245a-142">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="b245a-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b245a-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="b245a-143">optional</span></span>  <br/> |<span data-ttu-id="b245a-144">汎用名がユーザーによってカスタマイズされているかどうかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b245a-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="b245a-145">Xsd:Boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b245a-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="b245a-146">名前</span><span class="sxs-lookup"><span data-stu-id="b245a-146">Name</span></span>  <br/> |<span data-ttu-id="b245a-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b245a-147">xsd:string</span></span>  <br/> |<span data-ttu-id="b245a-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="b245a-148">optional</span></span>  <br/> |<span data-ttu-id="b245a-149">DocumentSheet の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="b245a-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="b245a-150">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b245a-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b245a-151">NameU</span><span class="sxs-lookup"><span data-stu-id="b245a-151">NameU</span></span>  <br/> |<span data-ttu-id="b245a-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b245a-152">xsd:string</span></span>  <br/> |<span data-ttu-id="b245a-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="b245a-153">optional</span></span>  <br/> |<span data-ttu-id="b245a-154">DocumentSheet の言語に依存しない名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="b245a-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="b245a-155">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b245a-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b245a-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="b245a-156">UniqueID</span></span>  <br/> |<span data-ttu-id="b245a-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b245a-157">xsd:string</span></span>  <br/> |<span data-ttu-id="b245a-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="b245a-158">optional</span></span>  <br/> |<span data-ttu-id="b245a-159">オプションの string。</span><span class="sxs-lookup"><span data-stu-id="b245a-159">Optional string.</span></span> <span data-ttu-id="b245a-160">図形を識別する GUID (グローバルに一意の識別子)。</span><span class="sxs-lookup"><span data-stu-id="b245a-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="b245a-161">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b245a-161">Values of the xsd:string type.</span></span>  <br/> |
   

