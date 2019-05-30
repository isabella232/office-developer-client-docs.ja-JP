---
title: PageSheet 要素 (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: マスターシェイプに関連付けられている図面ページのプロパティを指定します。
ms.openlocfilehash: 94fde64b130c2a05c4bd70c97552fe4218171ce7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540617"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="cb966-103">PageSheet 要素 (Master_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="cb966-103">PageSheet element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="cb966-104">マスターシェイプに関連付けられている図面ページのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="cb966-104">Specifies the properties of the drawing page associated with the master.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb966-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="cb966-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb966-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="cb966-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cb966-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="cb966-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cb966-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cb966-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cb966-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="cb966-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cb966-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="cb966-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cb966-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="cb966-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cb966-112">masters</span><span class="sxs-lookup"><span data-stu-id="cb966-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cb966-113">定義</span><span class="sxs-lookup"><span data-stu-id="cb966-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cb966-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="cb966-114">Elements and attributes</span></span>

<span data-ttu-id="cb966-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb966-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cb966-116">親要素</span><span class="sxs-lookup"><span data-stu-id="cb966-116">Parent elements</span></span>

|<span data-ttu-id="cb966-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="cb966-117">**Element**</span></span>|<span data-ttu-id="cb966-118">**型**</span><span class="sxs-lookup"><span data-stu-id="cb966-118">**Type**</span></span>|<span data-ttu-id="cb966-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb966-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cb966-120">Master</span><span class="sxs-lookup"><span data-stu-id="cb966-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb966-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="cb966-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb966-122">図面のマスターシェイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="cb966-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cb966-123">子要素</span><span class="sxs-lookup"><span data-stu-id="cb966-123">Child elements</span></span>

<span data-ttu-id="cb966-124">なし。</span><span class="sxs-lookup"><span data-stu-id="cb966-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb966-125">属性</span><span class="sxs-lookup"><span data-stu-id="cb966-125">Attributes</span></span>

|<span data-ttu-id="cb966-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="cb966-126">**Attribute**</span></span>|<span data-ttu-id="cb966-127">**型**</span><span class="sxs-lookup"><span data-stu-id="cb966-127">**Type**</span></span>|<span data-ttu-id="cb966-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="cb966-128">**Required**</span></span>|<span data-ttu-id="cb966-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb966-129">**Description**</span></span>|<span data-ttu-id="cb966-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="cb966-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cb966-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="cb966-131">FillStyle</span></span>  <br/> |<span data-ttu-id="cb966-132">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="cb966-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cb966-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb966-133">optional</span></span>  <br/> |<span data-ttu-id="cb966-134">塗りつぶしの書式設定を継承するスタイルシートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="cb966-134">specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="cb966-135">図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb966-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="cb966-136">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb966-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cb966-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="cb966-137">LineStyle</span></span>  <br/> |<span data-ttu-id="cb966-138">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="cb966-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cb966-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb966-139">optional</span></span>  <br/> |<span data-ttu-id="cb966-140">線の書式設定を継承するスタイルシートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="cb966-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="cb966-141">図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb966-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="cb966-142">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb966-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cb966-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="cb966-143">TextStyle</span></span>  <br/> |<span data-ttu-id="cb966-144">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="cb966-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cb966-145">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb966-145">optional</span></span>  <br/> |<span data-ttu-id="cb966-146">テキストの書式設定を継承するスタイルシートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="cb966-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="cb966-147">図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb966-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="cb966-148">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb966-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cb966-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="cb966-149">UniqueID</span></span>  <br/> |<span data-ttu-id="cb966-150">xsd: string</span><span class="sxs-lookup"><span data-stu-id="cb966-150">xsd:string</span></span>  <br/> |<span data-ttu-id="cb966-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb966-151">optional</span></span>  <br/> |<span data-ttu-id="cb966-152">親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="cb966-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="cb966-153">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb966-153">Values of the xsd:string type.</span></span>  <br/> |
   

