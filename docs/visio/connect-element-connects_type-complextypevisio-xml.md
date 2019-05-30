---
title: Connect 要素 (Connects_Type complexType) (Visio XML)
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
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="3c1a9-103">Connect 要素 (Connects_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="3c1a9-103">Connect element (Connects_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="3c1a9-104">組織図の線やボックスなど、図面内の 2 つの図形の接続を表します。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c1a9-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="3c1a9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c1a9-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="3c1a9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3c1a9-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="3c1a9-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3c1a9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3c1a9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3c1a9-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="3c1a9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3c1a9-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="3c1a9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3c1a9-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="3c1a9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3c1a9-112">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="3c1a9-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3c1a9-113">定義</span><span class="sxs-lookup"><span data-stu-id="3c1a9-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3c1a9-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="3c1a9-114">Elements and attributes</span></span>

<span data-ttu-id="3c1a9-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3c1a9-116">親要素</span><span class="sxs-lookup"><span data-stu-id="3c1a9-116">Parent elements</span></span>

|<span data-ttu-id="3c1a9-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="3c1a9-117">**Element**</span></span>|<span data-ttu-id="3c1a9-118">**型**</span><span class="sxs-lookup"><span data-stu-id="3c1a9-118">**Type**</span></span>|<span data-ttu-id="3c1a9-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="3c1a9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3c1a9-120">Connects</span><span class="sxs-lookup"><span data-stu-id="3c1a9-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c1a9-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="3c1a9-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3c1a9-122">図面内の2つの図形を接続するための**Connect**要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3c1a9-123">子要素</span><span class="sxs-lookup"><span data-stu-id="3c1a9-123">Child elements</span></span>

<span data-ttu-id="3c1a9-124">なし。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c1a9-125">属性</span><span class="sxs-lookup"><span data-stu-id="3c1a9-125">Attributes</span></span>

|<span data-ttu-id="3c1a9-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="3c1a9-126">**Attribute**</span></span>|<span data-ttu-id="3c1a9-127">**型**</span><span class="sxs-lookup"><span data-stu-id="3c1a9-127">**Type**</span></span>|<span data-ttu-id="3c1a9-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="3c1a9-128">**Required**</span></span>|<span data-ttu-id="3c1a9-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="3c1a9-129">**Description**</span></span>|<span data-ttu-id="3c1a9-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="3c1a9-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3c1a9-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="3c1a9-131">FromCell</span></span>  <br/> |<span data-ttu-id="3c1a9-132">xsd: string</span><span class="sxs-lookup"><span data-stu-id="3c1a9-132">xsd:string</span></span>  <br/> |<span data-ttu-id="3c1a9-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="3c1a9-133">optional</span></span>  <br/> |<span data-ttu-id="3c1a9-134">接続元のセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="3c1a9-135">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c1a9-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="3c1a9-136">FromPart</span></span>  <br/> |<span data-ttu-id="3c1a9-137">xsd: int</span><span class="sxs-lookup"><span data-stu-id="3c1a9-137">xsd:int</span></span>  <br/> |<span data-ttu-id="3c1a9-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="3c1a9-138">optional</span></span>  <br/> |<span data-ttu-id="3c1a9-139">接続元の図形の部分を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="3c1a9-140">Xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="3c1a9-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="3c1a9-141">FromSheet</span></span>  <br/> |<span data-ttu-id="3c1a9-142">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="3c1a9-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3c1a9-143">必須</span><span class="sxs-lookup"><span data-stu-id="3c1a9-143">required</span></span>  <br/> |<span data-ttu-id="3c1a9-144">1つまたは複数の接続を開始する図形の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="3c1a9-145">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3c1a9-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="3c1a9-146">ToCell</span></span>  <br/> |<span data-ttu-id="3c1a9-147">xsd: string</span><span class="sxs-lookup"><span data-stu-id="3c1a9-147">xsd:string</span></span>  <br/> |<span data-ttu-id="3c1a9-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="3c1a9-148">optional</span></span>  <br/> |<span data-ttu-id="3c1a9-149">接続を確立するセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="3c1a9-150">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c1a9-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="3c1a9-151">ToPart</span></span>  <br/> |<span data-ttu-id="3c1a9-152">xsd: int</span><span class="sxs-lookup"><span data-stu-id="3c1a9-152">xsd:int</span></span>  <br/> |<span data-ttu-id="3c1a9-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="3c1a9-153">optional</span></span>  <br/> |<span data-ttu-id="3c1a9-154">図形の接続先となる部分を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="3c1a9-155">Xsd: Int 型の値。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="3c1a9-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="3c1a9-156">ToSheet</span></span>  <br/> |<span data-ttu-id="3c1a9-157">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="3c1a9-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3c1a9-158">必須</span><span class="sxs-lookup"><span data-stu-id="3c1a9-158">required</span></span>  <br/> |<span data-ttu-id="3c1a9-159">1つまたは複数の接続を確立する図形の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="3c1a9-160">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="3c1a9-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

