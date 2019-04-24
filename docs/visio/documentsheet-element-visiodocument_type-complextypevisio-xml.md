---
title: documentsheet 要素 (VisioDocument_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: documentsheet 構造を指定します。
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356365"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="4042f-103">documentsheet 要素 (VisioDocument_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="4042f-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4042f-104">documentsheet 構造を指定します。</span><span class="sxs-lookup"><span data-stu-id="4042f-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4042f-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="4042f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4042f-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4042f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4042f-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="4042f-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4042f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4042f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4042f-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4042f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4042f-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="4042f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4042f-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="4042f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4042f-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="4042f-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4042f-113">定義</span><span class="sxs-lookup"><span data-stu-id="4042f-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4042f-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4042f-114">Elements and attributes</span></span>

<span data-ttu-id="4042f-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4042f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4042f-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4042f-116">Parent elements</span></span>

|<span data-ttu-id="4042f-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="4042f-117">**Element**</span></span>|<span data-ttu-id="4042f-118">**型**</span><span class="sxs-lookup"><span data-stu-id="4042f-118">**Type**</span></span>|<span data-ttu-id="4042f-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="4042f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4042f-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="4042f-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="4042f-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="4042f-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4042f-122">Microsoft Visio 図面のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="4042f-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4042f-123">子要素</span><span class="sxs-lookup"><span data-stu-id="4042f-123">Child elements</span></span>

|<span data-ttu-id="4042f-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="4042f-124">**Element**</span></span>|<span data-ttu-id="4042f-125">**型**</span><span class="sxs-lookup"><span data-stu-id="4042f-125">**Type**</span></span>|<span data-ttu-id="4042f-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="4042f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4042f-127">Cell</span><span class="sxs-lookup"><span data-stu-id="4042f-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="4042f-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4042f-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4042f-129">documentsheet のセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="4042f-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4042f-130">属性</span><span class="sxs-lookup"><span data-stu-id="4042f-130">Attributes</span></span>

|<span data-ttu-id="4042f-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="4042f-131">**Attribute**</span></span>|<span data-ttu-id="4042f-132">**型**</span><span class="sxs-lookup"><span data-stu-id="4042f-132">**Type**</span></span>|<span data-ttu-id="4042f-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="4042f-133">**Required**</span></span>|<span data-ttu-id="4042f-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="4042f-134">**Description**</span></span>|<span data-ttu-id="4042f-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="4042f-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4042f-136">iscustomname</span><span class="sxs-lookup"><span data-stu-id="4042f-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="4042f-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="4042f-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4042f-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="4042f-138">optional</span></span>  <br/> |<span data-ttu-id="4042f-139">ユーザーによって名前がカスタマイズされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4042f-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="4042f-140">xsd: Boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="4042f-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="4042f-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="4042f-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="4042f-142">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="4042f-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4042f-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="4042f-143">optional</span></span>  <br/> |<span data-ttu-id="4042f-144">ユーザーが汎用名をカスタマイズしたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4042f-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="4042f-145">xsd: Boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="4042f-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="4042f-146">名前</span><span class="sxs-lookup"><span data-stu-id="4042f-146">Name</span></span>  <br/> |<span data-ttu-id="4042f-147">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4042f-147">xsd:string</span></span>  <br/> |<span data-ttu-id="4042f-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="4042f-148">optional</span></span>  <br/> |<span data-ttu-id="4042f-149">documentsheet の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="4042f-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="4042f-150">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="4042f-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4042f-151">NameU</span><span class="sxs-lookup"><span data-stu-id="4042f-151">NameU</span></span>  <br/> |<span data-ttu-id="4042f-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4042f-152">xsd:string</span></span>  <br/> |<span data-ttu-id="4042f-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="4042f-153">optional</span></span>  <br/> |<span data-ttu-id="4042f-154">documentsheet の言語に依存しない名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="4042f-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="4042f-155">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="4042f-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4042f-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="4042f-156">UniqueID</span></span>  <br/> |<span data-ttu-id="4042f-157">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4042f-157">xsd:string</span></span>  <br/> |<span data-ttu-id="4042f-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="4042f-158">optional</span></span>  <br/> |<span data-ttu-id="4042f-159">オプションの string。</span><span class="sxs-lookup"><span data-stu-id="4042f-159">Optional string.</span></span> <span data-ttu-id="4042f-160">図形を識別する GUID (グローバル一意識別子)。</span><span class="sxs-lookup"><span data-stu-id="4042f-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="4042f-161">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="4042f-161">Values of the xsd:string type.</span></span>  <br/> |
   

