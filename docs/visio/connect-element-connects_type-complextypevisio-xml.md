---
title: 要素 (Connects_Type の複合型) を接続 ' Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: "\n			組織図の線やボックスなど、図面内の 2 つの図形の接続を表します。\n"
ms.openlocfilehash: 82413f44f05f2ec6140e2b3981b7a1e8435becb0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399320"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="6d381-103">要素 (Connects_Type の複合型) を接続 ' Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="6d381-103">Connect element (Connects_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6d381-104">
			組織図の線やボックスなど、図面内の 2 つの図形の接続を表します。
</span><span class="sxs-lookup"><span data-stu-id="6d381-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d381-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="6d381-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d381-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="6d381-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6d381-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="6d381-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6d381-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="6d381-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6d381-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6d381-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6d381-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6d381-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6d381-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="6d381-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6d381-112"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="6d381-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6d381-113">定義</span><span class="sxs-lookup"><span data-stu-id="6d381-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6d381-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6d381-114">Elements and attributes</span></span>

<span data-ttu-id="6d381-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d381-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6d381-116">親要素</span><span class="sxs-lookup"><span data-stu-id="6d381-116">Parent elements</span></span>

|<span data-ttu-id="6d381-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="6d381-117">**Element**</span></span>|<span data-ttu-id="6d381-118">**型**</span><span class="sxs-lookup"><span data-stu-id="6d381-118">**Type**</span></span>|<span data-ttu-id="6d381-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="6d381-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6d381-120">Connects</span><span class="sxs-lookup"><span data-stu-id="6d381-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6d381-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="6d381-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6d381-122">図面内の 2 つの図形間の各接続の**接続**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6d381-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6d381-123">子要素</span><span class="sxs-lookup"><span data-stu-id="6d381-123">Child elements</span></span>

<span data-ttu-id="6d381-124">なし。</span><span class="sxs-lookup"><span data-stu-id="6d381-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d381-125">属性</span><span class="sxs-lookup"><span data-stu-id="6d381-125">Attributes</span></span>

|<span data-ttu-id="6d381-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="6d381-126">**Attribute**</span></span>|<span data-ttu-id="6d381-127">**型**</span><span class="sxs-lookup"><span data-stu-id="6d381-127">**Type**</span></span>|<span data-ttu-id="6d381-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="6d381-128">**Required**</span></span>|<span data-ttu-id="6d381-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="6d381-129">**Description**</span></span>|<span data-ttu-id="6d381-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="6d381-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6d381-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="6d381-131">FromCell</span></span>  <br/> |<span data-ttu-id="6d381-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6d381-132">xsd:string</span></span>  <br/> |<span data-ttu-id="6d381-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="6d381-133">optional</span></span>  <br/> |<span data-ttu-id="6d381-134">接続元のセルです。</span><span class="sxs-lookup"><span data-stu-id="6d381-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="6d381-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d381-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6d381-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="6d381-136">FromPart</span></span>  <br/> |<span data-ttu-id="6d381-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="6d381-137">xsd:int</span></span>  <br/> |<span data-ttu-id="6d381-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="6d381-138">optional</span></span>  <br/> |<span data-ttu-id="6d381-139">接続元の図形の一部です。</span><span class="sxs-lookup"><span data-stu-id="6d381-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="6d381-140">Xsd:int 型の値です。</span><span class="sxs-lookup"><span data-stu-id="6d381-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="6d381-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="6d381-141">FromSheet</span></span>  <br/> |<span data-ttu-id="6d381-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6d381-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6d381-143">必須</span><span class="sxs-lookup"><span data-stu-id="6d381-143">required</span></span>  <br/> |<span data-ttu-id="6d381-144">接続または接続の送信元の図形の ID です。</span><span class="sxs-lookup"><span data-stu-id="6d381-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="6d381-145">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d381-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6d381-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="6d381-146">ToCell</span></span>  <br/> |<span data-ttu-id="6d381-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6d381-147">xsd:string</span></span>  <br/> |<span data-ttu-id="6d381-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="6d381-148">optional</span></span>  <br/> |<span data-ttu-id="6d381-149">接続を作成するセルです。</span><span class="sxs-lookup"><span data-stu-id="6d381-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="6d381-150">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d381-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6d381-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="6d381-151">ToPart</span></span>  <br/> |<span data-ttu-id="6d381-152">xsd:int</span><span class="sxs-lookup"><span data-stu-id="6d381-152">xsd:int</span></span>  <br/> |<span data-ttu-id="6d381-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="6d381-153">optional</span></span>  <br/> |<span data-ttu-id="6d381-154">接続を作成する図形の一部です。</span><span class="sxs-lookup"><span data-stu-id="6d381-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="6d381-155">Xsd:Int 型の値です。</span><span class="sxs-lookup"><span data-stu-id="6d381-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="6d381-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="6d381-156">ToSheet</span></span>  <br/> |<span data-ttu-id="6d381-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6d381-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6d381-158">必須</span><span class="sxs-lookup"><span data-stu-id="6d381-158">required</span></span>  <br/> |<span data-ttu-id="6d381-159">1 つまたは複数の接続を作成する図形の ID です。</span><span class="sxs-lookup"><span data-stu-id="6d381-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="6d381-160">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d381-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

