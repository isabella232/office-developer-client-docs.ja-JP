---
title: MasterShortcut_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: df1e10ff11470cd87fc16efbaba6ad968df6d1b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805836"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="7b313-102">MasterShortcut_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="7b313-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7b313-103">型情報</span><span class="sxs-lookup"><span data-stu-id="7b313-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b313-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="7b313-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7b313-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="7b313-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7b313-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7b313-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7b313-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="7b313-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7b313-108">なし</span><span class="sxs-lookup"><span data-stu-id="7b313-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7b313-109">定義</span><span class="sxs-lookup"><span data-stu-id="7b313-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7b313-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="7b313-110">Elements and attributes</span></span>

<span data-ttu-id="7b313-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b313-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7b313-112">子要素</span><span class="sxs-lookup"><span data-stu-id="7b313-112">Child elements</span></span>

|<span data-ttu-id="7b313-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="7b313-113">**Element**</span></span>|<span data-ttu-id="7b313-114">**型**</span><span class="sxs-lookup"><span data-stu-id="7b313-114">**Type**</span></span>|<span data-ttu-id="7b313-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="7b313-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7b313-116">Icon</span><span class="sxs-lookup"><span data-stu-id="7b313-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b313-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="7b313-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7b313-118">属性</span><span class="sxs-lookup"><span data-stu-id="7b313-118">Attributes</span></span>

|<span data-ttu-id="7b313-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="7b313-119">**Attribute**</span></span>|<span data-ttu-id="7b313-120">**型**</span><span class="sxs-lookup"><span data-stu-id="7b313-120">**Type**</span></span>|<span data-ttu-id="7b313-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="7b313-121">**Required**</span></span>|<span data-ttu-id="7b313-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="7b313-122">**Description**</span></span>|<span data-ttu-id="7b313-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="7b313-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7b313-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="7b313-124">AlignName</span></span>  <br/> |<span data-ttu-id="7b313-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="7b313-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7b313-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="7b313-126">optional</span></span>  <br/> ||<span data-ttu-id="7b313-127">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b313-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7b313-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="7b313-128">IconSize</span></span>  <br/> |<span data-ttu-id="7b313-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="7b313-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7b313-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="7b313-130">optional</span></span>  <br/> ||<span data-ttu-id="7b313-131">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b313-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7b313-132">ID</span><span class="sxs-lookup"><span data-stu-id="7b313-132">ID</span></span>  <br/> |<span data-ttu-id="7b313-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7b313-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7b313-134">必須</span><span class="sxs-lookup"><span data-stu-id="7b313-134">required</span></span>  <br/> ||<span data-ttu-id="7b313-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b313-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7b313-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="7b313-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="7b313-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="7b313-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7b313-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="7b313-138">optional</span></span>  <br/> ||<span data-ttu-id="7b313-139">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b313-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7b313-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="7b313-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="7b313-141">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="7b313-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7b313-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="7b313-142">optional</span></span>  <br/> ||<span data-ttu-id="7b313-143">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b313-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7b313-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="7b313-144">MasterType</span></span>  <br/> |<span data-ttu-id="7b313-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="7b313-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7b313-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="7b313-146">optional</span></span>  <br/> ||<span data-ttu-id="7b313-147">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b313-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7b313-148">名前</span><span class="sxs-lookup"><span data-stu-id="7b313-148">Name</span></span>  <br/> |<span data-ttu-id="7b313-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7b313-149">xsd:string</span></span>  <br/> |<span data-ttu-id="7b313-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="7b313-150">optional</span></span>  <br/> ||<span data-ttu-id="7b313-151">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b313-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7b313-152">NameU</span><span class="sxs-lookup"><span data-stu-id="7b313-152">NameU</span></span>  <br/> |<span data-ttu-id="7b313-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7b313-153">xsd:string</span></span>  <br/> |<span data-ttu-id="7b313-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="7b313-154">optional</span></span>  <br/> ||<span data-ttu-id="7b313-155">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b313-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7b313-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="7b313-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="7b313-157">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="7b313-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7b313-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="7b313-158">optional</span></span>  <br/> ||<span data-ttu-id="7b313-159">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b313-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7b313-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="7b313-160">Prompt</span></span>  <br/> |<span data-ttu-id="7b313-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7b313-161">xsd:string</span></span>  <br/> |<span data-ttu-id="7b313-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="7b313-162">optional</span></span>  <br/> ||<span data-ttu-id="7b313-163">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b313-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7b313-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="7b313-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="7b313-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7b313-165">xsd:string</span></span>  <br/> |<span data-ttu-id="7b313-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="7b313-166">optional</span></span>  <br/> ||<span data-ttu-id="7b313-167">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b313-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7b313-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="7b313-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="7b313-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7b313-169">xsd:string</span></span>  <br/> |<span data-ttu-id="7b313-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="7b313-170">optional</span></span>  <br/> ||<span data-ttu-id="7b313-171">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b313-171">Values of the xsd:string type.</span></span>  <br/> |
   

