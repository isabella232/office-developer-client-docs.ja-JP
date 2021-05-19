---
title: Connect要素 (Connects_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: 組織図の線やボックスなど、図面内の 2 つの図形の接続を表します。
ms.openlocfilehash: 3450a07e042fc633b9cd4952d9b3ad6b8190ed1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541996"
---
# <a name="connect-element-connects_type-complextype-visio-xml"></a><span data-ttu-id="70d03-103">Connect要素 (Connects_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="70d03-103">Connect element (Connects_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="70d03-104">組織図の線やボックスなど、図面内の 2 つの図形の接続を表します。</span><span class="sxs-lookup"><span data-stu-id="70d03-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70d03-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="70d03-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70d03-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="70d03-106">**Element type**</span></span> <br/> |[<span data-ttu-id="70d03-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="70d03-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="70d03-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="70d03-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="70d03-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="70d03-109">**Schema file**</span></span> <br/> |<span data-ttu-id="70d03-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="70d03-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="70d03-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="70d03-111">**Document parts**</span></span> <br/> |<span data-ttu-id="70d03-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="70d03-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="70d03-113">定義</span><span class="sxs-lookup"><span data-stu-id="70d03-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="70d03-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="70d03-114">Elements and attributes</span></span>

<span data-ttu-id="70d03-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="70d03-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="70d03-116">親要素</span><span class="sxs-lookup"><span data-stu-id="70d03-116">Parent elements</span></span>

|<span data-ttu-id="70d03-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="70d03-117">**Element**</span></span>|<span data-ttu-id="70d03-118">**型**</span><span class="sxs-lookup"><span data-stu-id="70d03-118">**Type**</span></span>|<span data-ttu-id="70d03-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="70d03-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="70d03-120">Connects</span><span class="sxs-lookup"><span data-stu-id="70d03-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70d03-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="70d03-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="70d03-122">図面内の **2 Connect** 間の接続ごとに 1 つの要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="70d03-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="70d03-123">子要素</span><span class="sxs-lookup"><span data-stu-id="70d03-123">Child elements</span></span>

<span data-ttu-id="70d03-124">なし。</span><span class="sxs-lookup"><span data-stu-id="70d03-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70d03-125">属性</span><span class="sxs-lookup"><span data-stu-id="70d03-125">Attributes</span></span>

|<span data-ttu-id="70d03-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="70d03-126">**Attribute**</span></span>|<span data-ttu-id="70d03-127">**型**</span><span class="sxs-lookup"><span data-stu-id="70d03-127">**Type**</span></span>|<span data-ttu-id="70d03-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="70d03-128">**Required**</span></span>|<span data-ttu-id="70d03-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="70d03-129">**Description**</span></span>|<span data-ttu-id="70d03-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="70d03-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="70d03-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="70d03-131">FromCell</span></span>  <br/> |<span data-ttu-id="70d03-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="70d03-132">xsd:string</span></span>  <br/> |<span data-ttu-id="70d03-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="70d03-133">optional</span></span>  <br/> |<span data-ttu-id="70d03-134">接続の開始元のセル。</span><span class="sxs-lookup"><span data-stu-id="70d03-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="70d03-135">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="70d03-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="70d03-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="70d03-136">FromPart</span></span>  <br/> |<span data-ttu-id="70d03-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="70d03-137">xsd:int</span></span>  <br/> |<span data-ttu-id="70d03-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="70d03-138">optional</span></span>  <br/> |<span data-ttu-id="70d03-139">接続の発生元となる図形の部分。</span><span class="sxs-lookup"><span data-stu-id="70d03-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="70d03-140">xsd:int 型の値。</span><span class="sxs-lookup"><span data-stu-id="70d03-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="70d03-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="70d03-141">FromSheet</span></span>  <br/> |<span data-ttu-id="70d03-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70d03-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70d03-143">必須</span><span class="sxs-lookup"><span data-stu-id="70d03-143">required</span></span>  <br/> |<span data-ttu-id="70d03-144">接続または接続の発生元となる図形の ID。</span><span class="sxs-lookup"><span data-stu-id="70d03-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="70d03-145">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="70d03-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="70d03-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="70d03-146">ToCell</span></span>  <br/> |<span data-ttu-id="70d03-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="70d03-147">xsd:string</span></span>  <br/> |<span data-ttu-id="70d03-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="70d03-148">optional</span></span>  <br/> |<span data-ttu-id="70d03-149">接続が行われたセル。</span><span class="sxs-lookup"><span data-stu-id="70d03-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="70d03-150">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="70d03-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="70d03-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="70d03-151">ToPart</span></span>  <br/> |<span data-ttu-id="70d03-152">xsd:int</span><span class="sxs-lookup"><span data-stu-id="70d03-152">xsd:int</span></span>  <br/> |<span data-ttu-id="70d03-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="70d03-153">optional</span></span>  <br/> |<span data-ttu-id="70d03-154">接続が行われた図形の部分。</span><span class="sxs-lookup"><span data-stu-id="70d03-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="70d03-155">xsd:Int 型の値。</span><span class="sxs-lookup"><span data-stu-id="70d03-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="70d03-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="70d03-156">ToSheet</span></span>  <br/> |<span data-ttu-id="70d03-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70d03-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70d03-158">必須</span><span class="sxs-lookup"><span data-stu-id="70d03-158">required</span></span>  <br/> |<span data-ttu-id="70d03-159">1 つ以上の接続が作成される図形の ID。</span><span class="sxs-lookup"><span data-stu-id="70d03-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="70d03-160">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="70d03-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

