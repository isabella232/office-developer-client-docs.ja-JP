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
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="91cc0-102">MasterShortcut_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="91cc0-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="91cc0-103">型情報</span><span class="sxs-lookup"><span data-stu-id="91cc0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91cc0-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="91cc0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="91cc0-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="91cc0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="91cc0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="91cc0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="91cc0-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="91cc0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="91cc0-108">なし</span><span class="sxs-lookup"><span data-stu-id="91cc0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="91cc0-109">定義</span><span class="sxs-lookup"><span data-stu-id="91cc0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="91cc0-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="91cc0-110">Elements and attributes</span></span>

<span data-ttu-id="91cc0-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="91cc0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="91cc0-112">子要素</span><span class="sxs-lookup"><span data-stu-id="91cc0-112">Child elements</span></span>

|<span data-ttu-id="91cc0-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="91cc0-113">**Element**</span></span>|<span data-ttu-id="91cc0-114">**型**</span><span class="sxs-lookup"><span data-stu-id="91cc0-114">**Type**</span></span>|<span data-ttu-id="91cc0-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="91cc0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="91cc0-116">Icon</span><span class="sxs-lookup"><span data-stu-id="91cc0-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="91cc0-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="91cc0-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="91cc0-118">属性</span><span class="sxs-lookup"><span data-stu-id="91cc0-118">Attributes</span></span>

|<span data-ttu-id="91cc0-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="91cc0-119">**Attribute**</span></span>|<span data-ttu-id="91cc0-120">**型**</span><span class="sxs-lookup"><span data-stu-id="91cc0-120">**Type**</span></span>|<span data-ttu-id="91cc0-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="91cc0-121">**Required**</span></span>|<span data-ttu-id="91cc0-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="91cc0-122">**Description**</span></span>|<span data-ttu-id="91cc0-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="91cc0-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="91cc0-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="91cc0-124">AlignName</span></span>  <br/> |<span data-ttu-id="91cc0-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="91cc0-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="91cc0-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="91cc0-126">optional</span></span>  <br/> ||<span data-ttu-id="91cc0-127">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="91cc0-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="91cc0-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="91cc0-128">IconSize</span></span>  <br/> |<span data-ttu-id="91cc0-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="91cc0-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="91cc0-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="91cc0-130">optional</span></span>  <br/> ||<span data-ttu-id="91cc0-131">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="91cc0-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="91cc0-132">ID</span><span class="sxs-lookup"><span data-stu-id="91cc0-132">ID</span></span>  <br/> |<span data-ttu-id="91cc0-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="91cc0-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="91cc0-134">必須</span><span class="sxs-lookup"><span data-stu-id="91cc0-134">required</span></span>  <br/> ||<span data-ttu-id="91cc0-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="91cc0-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="91cc0-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="91cc0-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="91cc0-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="91cc0-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="91cc0-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="91cc0-138">optional</span></span>  <br/> ||<span data-ttu-id="91cc0-139">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="91cc0-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="91cc0-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="91cc0-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="91cc0-141">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="91cc0-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="91cc0-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="91cc0-142">optional</span></span>  <br/> ||<span data-ttu-id="91cc0-143">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="91cc0-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="91cc0-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="91cc0-144">MasterType</span></span>  <br/> |<span data-ttu-id="91cc0-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="91cc0-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="91cc0-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="91cc0-146">optional</span></span>  <br/> ||<span data-ttu-id="91cc0-147">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="91cc0-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="91cc0-148">名前</span><span class="sxs-lookup"><span data-stu-id="91cc0-148">Name</span></span>  <br/> |<span data-ttu-id="91cc0-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="91cc0-149">xsd:string</span></span>  <br/> |<span data-ttu-id="91cc0-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="91cc0-150">optional</span></span>  <br/> ||<span data-ttu-id="91cc0-151">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="91cc0-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="91cc0-152">NameU</span><span class="sxs-lookup"><span data-stu-id="91cc0-152">NameU</span></span>  <br/> |<span data-ttu-id="91cc0-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="91cc0-153">xsd:string</span></span>  <br/> |<span data-ttu-id="91cc0-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="91cc0-154">optional</span></span>  <br/> ||<span data-ttu-id="91cc0-155">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="91cc0-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="91cc0-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="91cc0-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="91cc0-157">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="91cc0-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="91cc0-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="91cc0-158">optional</span></span>  <br/> ||<span data-ttu-id="91cc0-159">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="91cc0-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="91cc0-160">プロンプト</span><span class="sxs-lookup"><span data-stu-id="91cc0-160">Prompt</span></span>  <br/> |<span data-ttu-id="91cc0-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="91cc0-161">xsd:string</span></span>  <br/> |<span data-ttu-id="91cc0-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="91cc0-162">optional</span></span>  <br/> ||<span data-ttu-id="91cc0-163">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="91cc0-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="91cc0-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="91cc0-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="91cc0-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="91cc0-165">xsd:string</span></span>  <br/> |<span data-ttu-id="91cc0-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="91cc0-166">optional</span></span>  <br/> ||<span data-ttu-id="91cc0-167">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="91cc0-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="91cc0-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="91cc0-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="91cc0-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="91cc0-169">xsd:string</span></span>  <br/> |<span data-ttu-id="91cc0-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="91cc0-170">optional</span></span>  <br/> ||<span data-ttu-id="91cc0-171">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="91cc0-171">Values of the xsd:string type.</span></span>  <br/> |
   

