---
title: DocumentSheet 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: DocumentSheet 構造を指定します。
ms.openlocfilehash: 279fca457163d5bcbdda885c11c589bfcde0baa9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540043"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="87a57-103">DocumentSheet 要素 (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="87a57-103">DocumentSheet element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="87a57-104">DocumentSheet 構造を指定します。</span><span class="sxs-lookup"><span data-stu-id="87a57-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87a57-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="87a57-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87a57-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="87a57-106">**Element type**</span></span> <br/> |[<span data-ttu-id="87a57-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="87a57-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="87a57-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="87a57-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="87a57-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="87a57-109">**Schema file**</span></span> <br/> |<span data-ttu-id="87a57-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="87a57-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="87a57-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="87a57-111">**Document parts**</span></span> <br/> |<span data-ttu-id="87a57-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="87a57-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="87a57-113">定義</span><span class="sxs-lookup"><span data-stu-id="87a57-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="87a57-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="87a57-114">Elements and attributes</span></span>

<span data-ttu-id="87a57-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="87a57-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="87a57-116">親要素</span><span class="sxs-lookup"><span data-stu-id="87a57-116">Parent elements</span></span>

|<span data-ttu-id="87a57-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="87a57-117">**Element**</span></span>|<span data-ttu-id="87a57-118">**型**</span><span class="sxs-lookup"><span data-stu-id="87a57-118">**Type**</span></span>|<span data-ttu-id="87a57-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="87a57-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="87a57-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="87a57-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="87a57-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="87a57-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="87a57-122">Microsoft Visio 図面のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="87a57-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="87a57-123">子要素</span><span class="sxs-lookup"><span data-stu-id="87a57-123">Child elements</span></span>

|<span data-ttu-id="87a57-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="87a57-124">**Element**</span></span>|<span data-ttu-id="87a57-125">**型**</span><span class="sxs-lookup"><span data-stu-id="87a57-125">**Type**</span></span>|<span data-ttu-id="87a57-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="87a57-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="87a57-127">Cell</span><span class="sxs-lookup"><span data-stu-id="87a57-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="87a57-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="87a57-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="87a57-129">DocumentSheet のセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="87a57-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="87a57-130">属性</span><span class="sxs-lookup"><span data-stu-id="87a57-130">Attributes</span></span>

|<span data-ttu-id="87a57-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="87a57-131">**Attribute**</span></span>|<span data-ttu-id="87a57-132">**型**</span><span class="sxs-lookup"><span data-stu-id="87a57-132">**Type**</span></span>|<span data-ttu-id="87a57-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="87a57-133">**Required**</span></span>|<span data-ttu-id="87a57-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="87a57-134">**Description**</span></span>|<span data-ttu-id="87a57-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="87a57-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="87a57-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="87a57-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="87a57-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="87a57-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="87a57-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="87a57-138">optional</span></span>  <br/> |<span data-ttu-id="87a57-139">ユーザーによって名前がカスタマイズされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="87a57-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="87a57-140">Xsd: Boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="87a57-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="87a57-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="87a57-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="87a57-142">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="87a57-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="87a57-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="87a57-143">optional</span></span>  <br/> |<span data-ttu-id="87a57-144">ユーザーが汎用名をカスタマイズしたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="87a57-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="87a57-145">Xsd: Boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="87a57-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="87a57-146">名前</span><span class="sxs-lookup"><span data-stu-id="87a57-146">Name</span></span>  <br/> |<span data-ttu-id="87a57-147">xsd: string</span><span class="sxs-lookup"><span data-stu-id="87a57-147">xsd:string</span></span>  <br/> |<span data-ttu-id="87a57-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="87a57-148">optional</span></span>  <br/> |<span data-ttu-id="87a57-149">DocumentSheet の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="87a57-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="87a57-150">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="87a57-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="87a57-151">NameU</span><span class="sxs-lookup"><span data-stu-id="87a57-151">NameU</span></span>  <br/> |<span data-ttu-id="87a57-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="87a57-152">xsd:string</span></span>  <br/> |<span data-ttu-id="87a57-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="87a57-153">optional</span></span>  <br/> |<span data-ttu-id="87a57-154">DocumentSheet の言語に依存しない名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="87a57-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="87a57-155">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="87a57-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="87a57-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="87a57-156">UniqueID</span></span>  <br/> |<span data-ttu-id="87a57-157">xsd: string</span><span class="sxs-lookup"><span data-stu-id="87a57-157">xsd:string</span></span>  <br/> |<span data-ttu-id="87a57-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="87a57-158">optional</span></span>  <br/> |<span data-ttu-id="87a57-159">オプションの string。</span><span class="sxs-lookup"><span data-stu-id="87a57-159">Optional string.</span></span> <span data-ttu-id="87a57-160">図形を識別する GUID (グローバル一意識別子)。</span><span class="sxs-lookup"><span data-stu-id="87a57-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="87a57-161">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="87a57-161">Values of the xsd:string type.</span></span>  <br/> |
   

