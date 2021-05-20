---
title: FaceName 要素 (FaceNames_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: フォントに関する情報が含まれる。
ms.openlocfilehash: 773b5f10607cc6d515671d93d7d4abd9e39e72ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541016"
---
# <a name="facename-element-facenames_type-complextype-visio-xml"></a><span data-ttu-id="61163-103">FaceName 要素 (FaceNames_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="61163-103">FaceName element (FaceNames_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="61163-104">フォントに関する情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="61163-104">Contains information about a font.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61163-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="61163-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61163-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="61163-106">**Element type**</span></span> <br/> |[<span data-ttu-id="61163-107">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="61163-107">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="61163-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="61163-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="61163-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="61163-109">**Schema file**</span></span> <br/> |<span data-ttu-id="61163-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="61163-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="61163-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="61163-111">**Document parts**</span></span> <br/> |<span data-ttu-id="61163-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="61163-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="61163-113">定義</span><span class="sxs-lookup"><span data-stu-id="61163-113">Definition</span></span>

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="61163-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="61163-114">Elements and attributes</span></span>

<span data-ttu-id="61163-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="61163-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="61163-116">親要素</span><span class="sxs-lookup"><span data-stu-id="61163-116">Parent elements</span></span>

|<span data-ttu-id="61163-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="61163-117">**Element**</span></span>|<span data-ttu-id="61163-118">**型**</span><span class="sxs-lookup"><span data-stu-id="61163-118">**Type**</span></span>|<span data-ttu-id="61163-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="61163-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61163-120">FaceNames</span><span class="sxs-lookup"><span data-stu-id="61163-120">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61163-121">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="61163-121">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="61163-122">FaceName 要素のコレクション **を含** む。</span><span class="sxs-lookup"><span data-stu-id="61163-122">Contains a collection of **FaceName** elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="61163-123">子要素</span><span class="sxs-lookup"><span data-stu-id="61163-123">Child elements</span></span>

<span data-ttu-id="61163-124">なし。</span><span class="sxs-lookup"><span data-stu-id="61163-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61163-125">属性</span><span class="sxs-lookup"><span data-stu-id="61163-125">Attributes</span></span>

|<span data-ttu-id="61163-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="61163-126">**Attribute**</span></span>|<span data-ttu-id="61163-127">**型**</span><span class="sxs-lookup"><span data-stu-id="61163-127">**Type**</span></span>|<span data-ttu-id="61163-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="61163-128">**Required**</span></span>|<span data-ttu-id="61163-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="61163-129">**Description**</span></span>|<span data-ttu-id="61163-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="61163-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="61163-131">CharSets</span><span class="sxs-lookup"><span data-stu-id="61163-131">CharSets</span></span>  <br/> |<span data-ttu-id="61163-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61163-132">xsd:string</span></span>  <br/> |<span data-ttu-id="61163-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="61163-133">optional</span></span>  <br/> |<span data-ttu-id="61163-134">サポートされているフォントの文字セット。</span><span class="sxs-lookup"><span data-stu-id="61163-134">The supported character sets of the font.</span></span>  <br/> |<span data-ttu-id="61163-135">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="61163-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="61163-136">フラグ</span><span class="sxs-lookup"><span data-stu-id="61163-136">Flags</span></span>  <br/> |<span data-ttu-id="61163-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61163-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61163-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="61163-138">optional</span></span>  <br/> |<span data-ttu-id="61163-139">不足しているフォント、既定のフォント、アジアのフォント、複雑なフォント、垂直フォント、およびフォントの種類を示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="61163-139">Flags that indicate the following: missing font, default font, asian font, complex font, vertical font, and font type.</span></span>  <br/> |<span data-ttu-id="61163-140">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="61163-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61163-141">NameU</span><span class="sxs-lookup"><span data-stu-id="61163-141">NameU</span></span>  <br/> |<span data-ttu-id="61163-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61163-142">xsd:string</span></span>  <br/> |<span data-ttu-id="61163-143">必須</span><span class="sxs-lookup"><span data-stu-id="61163-143">required</span></span>  <br/> |<span data-ttu-id="61163-144">フォントの名前を UTF-16 Unicode 文字列として指定します。</span><span class="sxs-lookup"><span data-stu-id="61163-144">The name of the font as a UTF-16 Unicode string.</span></span>  <br/> ||
|<span data-ttu-id="61163-145">Panos</span><span class="sxs-lookup"><span data-stu-id="61163-145">Panos</span></span>  <br/> |<span data-ttu-id="61163-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61163-146">xsd:string</span></span>  <br/> |<span data-ttu-id="61163-147">省略可能</span><span class="sxs-lookup"><span data-stu-id="61163-147">optional</span></span>  <br/> |<span data-ttu-id="61163-148">フォントのパノセシグニチャ。</span><span class="sxs-lookup"><span data-stu-id="61163-148">The panose signature for the font.</span></span> <span data-ttu-id="61163-149">Panose は、視覚的特性に基づいて分類する書体の分類システムです。</span><span class="sxs-lookup"><span data-stu-id="61163-149">Panose is a classification system for typefaces that categorizes them based upon their visual characteristics.</span></span>  <br/> |<span data-ttu-id="61163-150">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="61163-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="61163-151">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="61163-151">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="61163-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61163-152">xsd:string</span></span>  <br/> |<span data-ttu-id="61163-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="61163-153">optional</span></span>  <br/> |<span data-ttu-id="61163-154">サポートされているフォントの Unicode 範囲。</span><span class="sxs-lookup"><span data-stu-id="61163-154">The supported Unicode ranges of the font.</span></span>  <br/> |<span data-ttu-id="61163-155">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="61163-155">Values of the xsd:string type.</span></span>  <br/> |
   

