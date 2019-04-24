---
title: PageSheet 要素 (Master_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: マスターシェイプに関連付けられている図面ページのプロパティを指定します。
ms.openlocfilehash: 579b2b4f02c79a38842a150b8757329e19e7bb3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361125"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="9b2ef-103">PageSheet 要素 (Master_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9b2ef-103">PageSheet element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9b2ef-104">マスターシェイプに関連付けられている図面ページのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-104">Specifies the properties of the drawing page associated with the master.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b2ef-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="9b2ef-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b2ef-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="9b2ef-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9b2ef-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="9b2ef-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9b2ef-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9b2ef-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9b2ef-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9b2ef-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9b2ef-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="9b2ef-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9b2ef-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="9b2ef-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9b2ef-112">masters</span><span class="sxs-lookup"><span data-stu-id="9b2ef-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9b2ef-113">定義</span><span class="sxs-lookup"><span data-stu-id="9b2ef-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9b2ef-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9b2ef-114">Elements and attributes</span></span>

<span data-ttu-id="9b2ef-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9b2ef-116">親要素</span><span class="sxs-lookup"><span data-stu-id="9b2ef-116">Parent elements</span></span>

|<span data-ttu-id="9b2ef-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="9b2ef-117">**Element**</span></span>|<span data-ttu-id="9b2ef-118">**型**</span><span class="sxs-lookup"><span data-stu-id="9b2ef-118">**Type**</span></span>|<span data-ttu-id="9b2ef-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="9b2ef-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9b2ef-120">Master</span><span class="sxs-lookup"><span data-stu-id="9b2ef-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9b2ef-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="9b2ef-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9b2ef-122">図面のマスターシェイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9b2ef-123">子要素</span><span class="sxs-lookup"><span data-stu-id="9b2ef-123">Child elements</span></span>

<span data-ttu-id="9b2ef-124">なし。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b2ef-125">属性</span><span class="sxs-lookup"><span data-stu-id="9b2ef-125">Attributes</span></span>

|<span data-ttu-id="9b2ef-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="9b2ef-126">**Attribute**</span></span>|<span data-ttu-id="9b2ef-127">**型**</span><span class="sxs-lookup"><span data-stu-id="9b2ef-127">**Type**</span></span>|<span data-ttu-id="9b2ef-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="9b2ef-128">**Required**</span></span>|<span data-ttu-id="9b2ef-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="9b2ef-129">**Description**</span></span>|<span data-ttu-id="9b2ef-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="9b2ef-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9b2ef-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="9b2ef-131">FillStyle</span></span>  <br/> |<span data-ttu-id="9b2ef-132">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="9b2ef-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9b2ef-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="9b2ef-133">optional</span></span>  <br/> |<span data-ttu-id="9b2ef-134">塗りつぶしの書式設定を継承するスタイルシートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-134">specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="9b2ef-135">図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="9b2ef-136">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9b2ef-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="9b2ef-137">LineStyle</span></span>  <br/> |<span data-ttu-id="9b2ef-138">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="9b2ef-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9b2ef-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="9b2ef-139">optional</span></span>  <br/> |<span data-ttu-id="9b2ef-140">線の書式設定を継承するスタイルシートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="9b2ef-141">図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="9b2ef-142">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9b2ef-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="9b2ef-143">TextStyle</span></span>  <br/> |<span data-ttu-id="9b2ef-144">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="9b2ef-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9b2ef-145">省略可能</span><span class="sxs-lookup"><span data-stu-id="9b2ef-145">optional</span></span>  <br/> |<span data-ttu-id="9b2ef-146">テキストの書式設定を継承するスタイルシートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="9b2ef-147">図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="9b2ef-148">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9b2ef-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="9b2ef-149">UniqueID</span></span>  <br/> |<span data-ttu-id="9b2ef-150">xsd: string</span><span class="sxs-lookup"><span data-stu-id="9b2ef-150">xsd:string</span></span>  <br/> |<span data-ttu-id="9b2ef-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="9b2ef-151">optional</span></span>  <br/> |<span data-ttu-id="9b2ef-152">親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="9b2ef-153">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="9b2ef-153">Values of the xsd:string type.</span></span>  <br/> |
   

