---
title: フォント名の要素 (FaceNames_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: フォントに関する情報が含まれています。
ms.openlocfilehash: 4c8f047d655be167dc058b3e29ac62161887ce99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389779"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a><span data-ttu-id="4d4a2-103">フォント名の要素 (FaceNames_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="4d4a2-103">FaceName element (FaceNames_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4d4a2-104">フォントに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-104">Contains information about a font.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d4a2-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="4d4a2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d4a2-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4d4a2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4d4a2-107">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="4d4a2-107">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4d4a2-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="4d4a2-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4d4a2-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4d4a2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4d4a2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4d4a2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4d4a2-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="4d4a2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4d4a2-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="4d4a2-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4d4a2-113">定義</span><span class="sxs-lookup"><span data-stu-id="4d4a2-113">Definition</span></span>

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4d4a2-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4d4a2-114">Elements and attributes</span></span>

<span data-ttu-id="4d4a2-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4d4a2-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4d4a2-116">Parent elements</span></span>

|<span data-ttu-id="4d4a2-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="4d4a2-117">**Element**</span></span>|<span data-ttu-id="4d4a2-118">**型**</span><span class="sxs-lookup"><span data-stu-id="4d4a2-118">**Type**</span></span>|<span data-ttu-id="4d4a2-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="4d4a2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4d4a2-120">FaceNames</span><span class="sxs-lookup"><span data-stu-id="4d4a2-120">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4d4a2-121">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="4d4a2-121">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4d4a2-122">**フォント名**の要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-122">Contains a collection of **FaceName** elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4d4a2-123">子要素</span><span class="sxs-lookup"><span data-stu-id="4d4a2-123">Child elements</span></span>

<span data-ttu-id="4d4a2-124">なし。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d4a2-125">属性</span><span class="sxs-lookup"><span data-stu-id="4d4a2-125">Attributes</span></span>

|<span data-ttu-id="4d4a2-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="4d4a2-126">**Attribute**</span></span>|<span data-ttu-id="4d4a2-127">**型**</span><span class="sxs-lookup"><span data-stu-id="4d4a2-127">**Type**</span></span>|<span data-ttu-id="4d4a2-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="4d4a2-128">**Required**</span></span>|<span data-ttu-id="4d4a2-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="4d4a2-129">**Description**</span></span>|<span data-ttu-id="4d4a2-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="4d4a2-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4d4a2-131">文字集合</span><span class="sxs-lookup"><span data-stu-id="4d4a2-131">CharSets</span></span>  <br/> |<span data-ttu-id="4d4a2-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4d4a2-132">xsd:string</span></span>  <br/> |<span data-ttu-id="4d4a2-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="4d4a2-133">optional</span></span>  <br/> |<span data-ttu-id="4d4a2-134">サポートされている文字のフォントを設定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-134">The supported character sets of the font.</span></span>  <br/> |<span data-ttu-id="4d4a2-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4d4a2-136">Flags</span><span class="sxs-lookup"><span data-stu-id="4d4a2-136">Flags</span></span>  <br/> |<span data-ttu-id="4d4a2-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4d4a2-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4d4a2-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="4d4a2-138">optional</span></span>  <br/> |<span data-ttu-id="4d4a2-139">次に示すフラグ: フォント、デフォルトのフォント、アジア言語のフォント、複雑なフォント、縦書きフォント、およびフォントの種類がありません。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-139">Flags that indicate the following: missing font, default font, asian font, complex font, vertical font, and font type.</span></span>  <br/> |<span data-ttu-id="4d4a2-140">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4d4a2-141">NameU</span><span class="sxs-lookup"><span data-stu-id="4d4a2-141">NameU</span></span>  <br/> |<span data-ttu-id="4d4a2-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4d4a2-142">xsd:string</span></span>  <br/> |<span data-ttu-id="4d4a2-143">必須</span><span class="sxs-lookup"><span data-stu-id="4d4a2-143">required</span></span>  <br/> |<span data-ttu-id="4d4a2-144">Utf-16 Unicode 文字列のフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-144">The name of the font as a UTF-16 Unicode string.</span></span>  <br/> ||
|<span data-ttu-id="4d4a2-145">Panos</span><span class="sxs-lookup"><span data-stu-id="4d4a2-145">Panos</span></span>  <br/> |<span data-ttu-id="4d4a2-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4d4a2-146">xsd:string</span></span>  <br/> |<span data-ttu-id="4d4a2-147">省略可能</span><span class="sxs-lookup"><span data-stu-id="4d4a2-147">optional</span></span>  <br/> |<span data-ttu-id="4d4a2-148">フォントの panose 署名します。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-148">The panose signature for the font.</span></span> <span data-ttu-id="4d4a2-149">Panose は、その視覚的特性に基づくに分類されている書体の分類システムです。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-149">Panose is a classification system for typefaces that categorizes them based upon their visual characteristics.</span></span>  <br/> |<span data-ttu-id="4d4a2-150">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4d4a2-151">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="4d4a2-151">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="4d4a2-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4d4a2-152">xsd:string</span></span>  <br/> |<span data-ttu-id="4d4a2-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="4d4a2-153">optional</span></span>  <br/> |<span data-ttu-id="4d4a2-154">フォントのサポートされている Unicode の範囲です。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-154">The supported Unicode ranges of the font.</span></span>  <br/> |<span data-ttu-id="4d4a2-155">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d4a2-155">Values of the xsd:string type.</span></span>  <br/> |
   

