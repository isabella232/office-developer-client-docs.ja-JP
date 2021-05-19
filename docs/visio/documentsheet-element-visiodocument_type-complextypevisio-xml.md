---
title: DocumentSheet 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: DocumentSheet 構造体を指定します。
ms.openlocfilehash: 279fca457163d5bcbdda885c11c589bfcde0baa9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540043"
---
# <a name="documentsheet-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="0aeb2-103">DocumentSheet 要素 (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0aeb2-103">DocumentSheet element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="0aeb2-104">DocumentSheet 構造体を指定します。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0aeb2-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="0aeb2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0aeb2-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0aeb2-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="0aeb2-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0aeb2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0aeb2-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0aeb2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0aeb2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0aeb2-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0aeb2-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="0aeb2-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0aeb2-113">定義</span><span class="sxs-lookup"><span data-stu-id="0aeb2-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0aeb2-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0aeb2-114">Elements and attributes</span></span>

<span data-ttu-id="0aeb2-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0aeb2-116">親要素</span><span class="sxs-lookup"><span data-stu-id="0aeb2-116">Parent elements</span></span>

|<span data-ttu-id="0aeb2-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-117">**Element**</span></span>|<span data-ttu-id="0aeb2-118">**型**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-118">**Type**</span></span>|<span data-ttu-id="0aeb2-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0aeb2-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="0aeb2-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="0aeb2-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="0aeb2-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0aeb2-122">Microsoft ドキュメントのルートVisioです。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0aeb2-123">子要素</span><span class="sxs-lookup"><span data-stu-id="0aeb2-123">Child elements</span></span>

|<span data-ttu-id="0aeb2-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-124">**Element**</span></span>|<span data-ttu-id="0aeb2-125">**型**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-125">**Type**</span></span>|<span data-ttu-id="0aeb2-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0aeb2-127">Cell</span><span class="sxs-lookup"><span data-stu-id="0aeb2-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="0aeb2-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0aeb2-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0aeb2-129">DocumentSheet のセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0aeb2-130">属性</span><span class="sxs-lookup"><span data-stu-id="0aeb2-130">Attributes</span></span>

|<span data-ttu-id="0aeb2-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-131">**Attribute**</span></span>|<span data-ttu-id="0aeb2-132">**型**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-132">**Type**</span></span>|<span data-ttu-id="0aeb2-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-133">**Required**</span></span>|<span data-ttu-id="0aeb2-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-134">**Description**</span></span>|<span data-ttu-id="0aeb2-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="0aeb2-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0aeb2-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="0aeb2-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="0aeb2-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="0aeb2-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0aeb2-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="0aeb2-138">optional</span></span>  <br/> |<span data-ttu-id="0aeb2-139">名前がユーザーによってカスタマイズされたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="0aeb2-140">xsd:Boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="0aeb2-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="0aeb2-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="0aeb2-142">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="0aeb2-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0aeb2-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="0aeb2-143">optional</span></span>  <br/> |<span data-ttu-id="0aeb2-144">ユニバーサル名がユーザーによってカスタマイズされたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="0aeb2-145">xsd:Boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="0aeb2-146">名前</span><span class="sxs-lookup"><span data-stu-id="0aeb2-146">Name</span></span>  <br/> |<span data-ttu-id="0aeb2-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0aeb2-147">xsd:string</span></span>  <br/> |<span data-ttu-id="0aeb2-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="0aeb2-148">optional</span></span>  <br/> |<span data-ttu-id="0aeb2-149">DocumentSheet の言語依存の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="0aeb2-150">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0aeb2-151">NameU</span><span class="sxs-lookup"><span data-stu-id="0aeb2-151">NameU</span></span>  <br/> |<span data-ttu-id="0aeb2-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0aeb2-152">xsd:string</span></span>  <br/> |<span data-ttu-id="0aeb2-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="0aeb2-153">optional</span></span>  <br/> |<span data-ttu-id="0aeb2-154">DocumentSheet の言語に依存しない名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="0aeb2-155">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0aeb2-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="0aeb2-156">UniqueID</span></span>  <br/> |<span data-ttu-id="0aeb2-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0aeb2-157">xsd:string</span></span>  <br/> |<span data-ttu-id="0aeb2-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="0aeb2-158">optional</span></span>  <br/> |<span data-ttu-id="0aeb2-159">オプションの string。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-159">Optional string.</span></span> <span data-ttu-id="0aeb2-160">図形を識別する GUID (グローバル一意識別子)。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="0aeb2-161">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0aeb2-161">Values of the xsd:string type.</span></span>  <br/> |
   

