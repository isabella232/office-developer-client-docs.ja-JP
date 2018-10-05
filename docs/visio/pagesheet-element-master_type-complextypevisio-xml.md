---
title: PageSheet 要素 (Master_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: マスターに関連付けられている図面ページのプロパティを指定します。
ms.openlocfilehash: 579b2b4f02c79a38842a150b8757329e19e7bb3a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399138"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="18dcf-103">PageSheet 要素 (Master_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="18dcf-103">PageSheet element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="18dcf-104">マスターに関連付けられている図面ページのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="18dcf-104">Specifies the properties of the drawing page associated with the master.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18dcf-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="18dcf-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18dcf-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="18dcf-106">**Element type**</span></span> <br/> |[<span data-ttu-id="18dcf-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="18dcf-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="18dcf-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="18dcf-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="18dcf-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="18dcf-109">**Schema file**</span></span> <br/> |<span data-ttu-id="18dcf-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="18dcf-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="18dcf-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="18dcf-111">**Document parts**</span></span> <br/> |<span data-ttu-id="18dcf-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="18dcf-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="18dcf-113">定義</span><span class="sxs-lookup"><span data-stu-id="18dcf-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="18dcf-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="18dcf-114">Elements and attributes</span></span>

<span data-ttu-id="18dcf-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="18dcf-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="18dcf-116">親要素</span><span class="sxs-lookup"><span data-stu-id="18dcf-116">Parent elements</span></span>

|<span data-ttu-id="18dcf-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="18dcf-117">**Element**</span></span>|<span data-ttu-id="18dcf-118">**型**</span><span class="sxs-lookup"><span data-stu-id="18dcf-118">**Type**</span></span>|<span data-ttu-id="18dcf-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="18dcf-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="18dcf-120">Master</span><span class="sxs-lookup"><span data-stu-id="18dcf-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="18dcf-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="18dcf-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="18dcf-122">図面のマスター シェイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="18dcf-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="18dcf-123">子要素</span><span class="sxs-lookup"><span data-stu-id="18dcf-123">Child elements</span></span>

<span data-ttu-id="18dcf-124">なし。</span><span class="sxs-lookup"><span data-stu-id="18dcf-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18dcf-125">属性</span><span class="sxs-lookup"><span data-stu-id="18dcf-125">Attributes</span></span>

|<span data-ttu-id="18dcf-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="18dcf-126">**Attribute**</span></span>|<span data-ttu-id="18dcf-127">**型**</span><span class="sxs-lookup"><span data-stu-id="18dcf-127">**Type**</span></span>|<span data-ttu-id="18dcf-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="18dcf-128">**Required**</span></span>|<span data-ttu-id="18dcf-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="18dcf-129">**Description**</span></span>|<span data-ttu-id="18dcf-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="18dcf-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="18dcf-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="18dcf-131">FillStyle</span></span>  <br/> |<span data-ttu-id="18dcf-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="18dcf-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="18dcf-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="18dcf-133">optional</span></span>  <br/> |<span data-ttu-id="18dcf-134">塗りつぶしの書式設定を継承するスタイル シートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="18dcf-134">specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="18dcf-135">図面内の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="18dcf-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="18dcf-136">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18dcf-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="18dcf-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="18dcf-137">LineStyle</span></span>  <br/> |<span data-ttu-id="18dcf-138">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="18dcf-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="18dcf-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="18dcf-139">optional</span></span>  <br/> |<span data-ttu-id="18dcf-140">線の書式設定を継承するスタイル シートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="18dcf-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="18dcf-141">図面内の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="18dcf-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="18dcf-142">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18dcf-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="18dcf-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="18dcf-143">TextStyle</span></span>  <br/> |<span data-ttu-id="18dcf-144">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="18dcf-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="18dcf-145">省略可能</span><span class="sxs-lookup"><span data-stu-id="18dcf-145">optional</span></span>  <br/> |<span data-ttu-id="18dcf-146">テキストの書式設定を継承するスタイル シートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="18dcf-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="18dcf-147">図面内の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="18dcf-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="18dcf-148">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18dcf-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="18dcf-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="18dcf-149">UniqueID</span></span>  <br/> |<span data-ttu-id="18dcf-150">xsd:string</span><span class="sxs-lookup"><span data-stu-id="18dcf-150">xsd:string</span></span>  <br/> |<span data-ttu-id="18dcf-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="18dcf-151">optional</span></span>  <br/> |<span data-ttu-id="18dcf-152">その親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="18dcf-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="18dcf-153">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18dcf-153">Values of the xsd:string type.</span></span>  <br/> |
   

