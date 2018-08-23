---
title: PageSheet 要素 (Master_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: マスターに関連付けられている図面ページのプロパティを指定します。
ms.openlocfilehash: ab20cfe4561cd5fd0eeb6edad0b3a608428b0e8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806008"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="61b2c-103">PageSheet 要素 (Master_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="61b2c-103">PageSheet element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="61b2c-104">マスターに関連付けられている図面ページのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="61b2c-104">Specifies the properties of the drawing page associated with the master.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61b2c-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="61b2c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61b2c-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="61b2c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="61b2c-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="61b2c-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="61b2c-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="61b2c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="61b2c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="61b2c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="61b2c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="61b2c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="61b2c-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="61b2c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="61b2c-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="61b2c-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="61b2c-113">定義</span><span class="sxs-lookup"><span data-stu-id="61b2c-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="61b2c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="61b2c-114">Elements and attributes</span></span>

<span data-ttu-id="61b2c-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="61b2c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="61b2c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="61b2c-116">Parent elements</span></span>

|<span data-ttu-id="61b2c-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="61b2c-117">**Element**</span></span>|<span data-ttu-id="61b2c-118">**型**</span><span class="sxs-lookup"><span data-stu-id="61b2c-118">**Type**</span></span>|<span data-ttu-id="61b2c-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="61b2c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61b2c-120">Master</span><span class="sxs-lookup"><span data-stu-id="61b2c-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61b2c-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="61b2c-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="61b2c-122">図面のマスター シェイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="61b2c-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="61b2c-123">子要素</span><span class="sxs-lookup"><span data-stu-id="61b2c-123">Child elements</span></span>

<span data-ttu-id="61b2c-124">なし。</span><span class="sxs-lookup"><span data-stu-id="61b2c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61b2c-125">属性</span><span class="sxs-lookup"><span data-stu-id="61b2c-125">Attributes</span></span>

|<span data-ttu-id="61b2c-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="61b2c-126">**Attribute**</span></span>|<span data-ttu-id="61b2c-127">**型**</span><span class="sxs-lookup"><span data-stu-id="61b2c-127">**Type**</span></span>|<span data-ttu-id="61b2c-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="61b2c-128">**Required**</span></span>|<span data-ttu-id="61b2c-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="61b2c-129">**Description**</span></span>|<span data-ttu-id="61b2c-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="61b2c-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="61b2c-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="61b2c-131">FillStyle</span></span>  <br/> |<span data-ttu-id="61b2c-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61b2c-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61b2c-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="61b2c-133">optional</span></span>  <br/> |<span data-ttu-id="61b2c-134">塗りつぶしの書式設定を継承するスタイル シートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="61b2c-134">specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="61b2c-135">図面内の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="61b2c-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="61b2c-136">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61b2c-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61b2c-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="61b2c-137">LineStyle</span></span>  <br/> |<span data-ttu-id="61b2c-138">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61b2c-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61b2c-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="61b2c-139">optional</span></span>  <br/> |<span data-ttu-id="61b2c-140">線の書式設定を継承するスタイル シートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="61b2c-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="61b2c-141">図面内の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="61b2c-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="61b2c-142">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61b2c-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61b2c-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="61b2c-143">TextStyle</span></span>  <br/> |<span data-ttu-id="61b2c-144">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61b2c-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61b2c-145">省略可能</span><span class="sxs-lookup"><span data-stu-id="61b2c-145">optional</span></span>  <br/> |<span data-ttu-id="61b2c-146">テキストの書式設定を継承するスタイル シートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="61b2c-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="61b2c-147">図面内の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="61b2c-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="61b2c-148">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61b2c-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61b2c-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="61b2c-149">UniqueID</span></span>  <br/> |<span data-ttu-id="61b2c-150">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61b2c-150">xsd:string</span></span>  <br/> |<span data-ttu-id="61b2c-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="61b2c-151">optional</span></span>  <br/> |<span data-ttu-id="61b2c-152">その親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="61b2c-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="61b2c-153">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61b2c-153">Values of the xsd:string type.</span></span>  <br/> |
   

