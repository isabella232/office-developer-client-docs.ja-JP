---
title: MasterShortcut_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: ed8dd8ef985c814e41017526144bd7ec8cb63424
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538061"
---
# <a name="mastershortcut_type-complextype-visio-xml"></a><span data-ttu-id="ffee8-102">MasterShortcut_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ffee8-102">MasterShortcut_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ffee8-103">型情報</span><span class="sxs-lookup"><span data-stu-id="ffee8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffee8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ffee8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ffee8-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ffee8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ffee8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ffee8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ffee8-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="ffee8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ffee8-108">なし</span><span class="sxs-lookup"><span data-stu-id="ffee8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ffee8-109">定義</span><span class="sxs-lookup"><span data-stu-id="ffee8-109">Definition</span></span>

```XML
          <xs:complexType name="MasterShortcut_Type">
          
          <xs:all>
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutURL"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutHelp"
  type="xsd:string"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ffee8-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ffee8-110">Elements and attributes</span></span>

<span data-ttu-id="ffee8-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffee8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ffee8-112">子要素</span><span class="sxs-lookup"><span data-stu-id="ffee8-112">Child elements</span></span>

|<span data-ttu-id="ffee8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ffee8-113">**Element**</span></span>|<span data-ttu-id="ffee8-114">**型**</span><span class="sxs-lookup"><span data-stu-id="ffee8-114">**Type**</span></span>|<span data-ttu-id="ffee8-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="ffee8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ffee8-116">Icon</span><span class="sxs-lookup"><span data-stu-id="ffee8-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ffee8-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="ffee8-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ffee8-118">属性</span><span class="sxs-lookup"><span data-stu-id="ffee8-118">Attributes</span></span>

|<span data-ttu-id="ffee8-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="ffee8-119">**Attribute**</span></span>|<span data-ttu-id="ffee8-120">**型**</span><span class="sxs-lookup"><span data-stu-id="ffee8-120">**Type**</span></span>|<span data-ttu-id="ffee8-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="ffee8-121">**Required**</span></span>|<span data-ttu-id="ffee8-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="ffee8-122">**Description**</span></span>|<span data-ttu-id="ffee8-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="ffee8-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ffee8-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="ffee8-124">AlignName</span></span>  <br/> |<span data-ttu-id="ffee8-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ffee8-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ffee8-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="ffee8-126">optional</span></span>  <br/> ||<span data-ttu-id="ffee8-127">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="ffee8-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ffee8-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="ffee8-128">IconSize</span></span>  <br/> |<span data-ttu-id="ffee8-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ffee8-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ffee8-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="ffee8-130">optional</span></span>  <br/> ||<span data-ttu-id="ffee8-131">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="ffee8-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ffee8-132">ID</span><span class="sxs-lookup"><span data-stu-id="ffee8-132">ID</span></span>  <br/> |<span data-ttu-id="ffee8-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ffee8-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ffee8-134">必須</span><span class="sxs-lookup"><span data-stu-id="ffee8-134">required</span></span>  <br/> ||<span data-ttu-id="ffee8-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="ffee8-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ffee8-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="ffee8-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="ffee8-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ffee8-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ffee8-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="ffee8-138">optional</span></span>  <br/> ||<span data-ttu-id="ffee8-139">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="ffee8-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ffee8-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="ffee8-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="ffee8-141">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ffee8-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ffee8-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="ffee8-142">optional</span></span>  <br/> ||<span data-ttu-id="ffee8-143">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="ffee8-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ffee8-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="ffee8-144">MasterType</span></span>  <br/> |<span data-ttu-id="ffee8-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ffee8-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ffee8-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="ffee8-146">optional</span></span>  <br/> ||<span data-ttu-id="ffee8-147">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="ffee8-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ffee8-148">名前</span><span class="sxs-lookup"><span data-stu-id="ffee8-148">Name</span></span>  <br/> |<span data-ttu-id="ffee8-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ffee8-149">xsd:string</span></span>  <br/> |<span data-ttu-id="ffee8-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="ffee8-150">optional</span></span>  <br/> ||<span data-ttu-id="ffee8-151">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="ffee8-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ffee8-152">NameU</span><span class="sxs-lookup"><span data-stu-id="ffee8-152">NameU</span></span>  <br/> |<span data-ttu-id="ffee8-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ffee8-153">xsd:string</span></span>  <br/> |<span data-ttu-id="ffee8-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="ffee8-154">optional</span></span>  <br/> ||<span data-ttu-id="ffee8-155">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="ffee8-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ffee8-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="ffee8-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="ffee8-157">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ffee8-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ffee8-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="ffee8-158">optional</span></span>  <br/> ||<span data-ttu-id="ffee8-159">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="ffee8-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ffee8-160">プロンプト</span><span class="sxs-lookup"><span data-stu-id="ffee8-160">Prompt</span></span>  <br/> |<span data-ttu-id="ffee8-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ffee8-161">xsd:string</span></span>  <br/> |<span data-ttu-id="ffee8-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="ffee8-162">optional</span></span>  <br/> ||<span data-ttu-id="ffee8-163">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="ffee8-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ffee8-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="ffee8-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="ffee8-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ffee8-165">xsd:string</span></span>  <br/> |<span data-ttu-id="ffee8-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="ffee8-166">optional</span></span>  <br/> ||<span data-ttu-id="ffee8-167">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="ffee8-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ffee8-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="ffee8-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="ffee8-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ffee8-169">xsd:string</span></span>  <br/> |<span data-ttu-id="ffee8-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="ffee8-170">optional</span></span>  <br/> ||<span data-ttu-id="ffee8-171">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="ffee8-171">Values of the xsd:string type.</span></span>  <br/> |
   

