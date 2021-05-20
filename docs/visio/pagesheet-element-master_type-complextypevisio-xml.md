---
title: PageSheet 要素 (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: マスターに関連付けられた図面ページのプロパティを指定します。
ms.openlocfilehash: 94fde64b130c2a05c4bd70c97552fe4218171ce7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540617"
---
# <a name="pagesheet-element-master_type-complextype-visio-xml"></a><span data-ttu-id="bd472-103">PageSheet 要素 (Master_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bd472-103">PageSheet element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="bd472-104">マスターに関連付けられた図面ページのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="bd472-104">Specifies the properties of the drawing page associated with the master.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bd472-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="bd472-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd472-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="bd472-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bd472-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="bd472-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bd472-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bd472-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bd472-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="bd472-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bd472-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="bd472-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bd472-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="bd472-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bd472-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="bd472-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bd472-113">定義</span><span class="sxs-lookup"><span data-stu-id="bd472-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bd472-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="bd472-114">Elements and attributes</span></span>

<span data-ttu-id="bd472-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bd472-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bd472-116">親要素</span><span class="sxs-lookup"><span data-stu-id="bd472-116">Parent elements</span></span>

|<span data-ttu-id="bd472-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="bd472-117">**Element**</span></span>|<span data-ttu-id="bd472-118">**型**</span><span class="sxs-lookup"><span data-stu-id="bd472-118">**Type**</span></span>|<span data-ttu-id="bd472-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="bd472-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bd472-120">Master</span><span class="sxs-lookup"><span data-stu-id="bd472-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bd472-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="bd472-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bd472-122">図面のマスターを指定します。</span><span class="sxs-lookup"><span data-stu-id="bd472-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bd472-123">子要素</span><span class="sxs-lookup"><span data-stu-id="bd472-123">Child elements</span></span>

<span data-ttu-id="bd472-124">なし。</span><span class="sxs-lookup"><span data-stu-id="bd472-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd472-125">属性</span><span class="sxs-lookup"><span data-stu-id="bd472-125">Attributes</span></span>

|<span data-ttu-id="bd472-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="bd472-126">**Attribute**</span></span>|<span data-ttu-id="bd472-127">**型**</span><span class="sxs-lookup"><span data-stu-id="bd472-127">**Type**</span></span>|<span data-ttu-id="bd472-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="bd472-128">**Required**</span></span>|<span data-ttu-id="bd472-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="bd472-129">**Description**</span></span>|<span data-ttu-id="bd472-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="bd472-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bd472-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="bd472-131">FillStyle</span></span>  <br/> |<span data-ttu-id="bd472-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bd472-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bd472-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="bd472-133">optional</span></span>  <br/> |<span data-ttu-id="bd472-134">塗りつぶしの書式を継承するスタイル シートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd472-134">specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="bd472-135">図面内のオブジェクトに関連付けられている **ID** 属性 **StyleSheet_Typeする必要** があります。</span><span class="sxs-lookup"><span data-stu-id="bd472-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="bd472-136">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="bd472-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bd472-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="bd472-137">LineStyle</span></span>  <br/> |<span data-ttu-id="bd472-138">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bd472-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bd472-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="bd472-139">optional</span></span>  <br/> |<span data-ttu-id="bd472-140">線の書式設定を継承するスタイル シートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd472-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="bd472-141">図面内のオブジェクトに関連付けられている **ID** 属性 **StyleSheet_Typeする必要** があります。</span><span class="sxs-lookup"><span data-stu-id="bd472-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="bd472-142">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="bd472-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bd472-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="bd472-143">TextStyle</span></span>  <br/> |<span data-ttu-id="bd472-144">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bd472-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bd472-145">省略可能</span><span class="sxs-lookup"><span data-stu-id="bd472-145">optional</span></span>  <br/> |<span data-ttu-id="bd472-146">テキストの書式設定を継承するスタイル シートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd472-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="bd472-147">図面内のオブジェクトに関連付けられている **ID** 属性 **StyleSheet_Typeする必要** があります。</span><span class="sxs-lookup"><span data-stu-id="bd472-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="bd472-148">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="bd472-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bd472-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="bd472-149">UniqueID</span></span>  <br/> |<span data-ttu-id="bd472-150">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bd472-150">xsd:string</span></span>  <br/> |<span data-ttu-id="bd472-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="bd472-151">optional</span></span>  <br/> |<span data-ttu-id="bd472-152">親要素内の要素の一意の ID です。</span><span class="sxs-lookup"><span data-stu-id="bd472-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="bd472-153">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="bd472-153">Values of the xsd:string type.</span></span>  <br/> |
   

