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
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="cb92d-102">MasterShortcut_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="cb92d-102">MasterShortcut_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="cb92d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="cb92d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb92d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cb92d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cb92d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="cb92d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cb92d-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="cb92d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cb92d-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="cb92d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cb92d-108">None</span><span class="sxs-lookup"><span data-stu-id="cb92d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cb92d-109">定義</span><span class="sxs-lookup"><span data-stu-id="cb92d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cb92d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="cb92d-110">Elements and attributes</span></span>

<span data-ttu-id="cb92d-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb92d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cb92d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="cb92d-112">Child elements</span></span>

|<span data-ttu-id="cb92d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cb92d-113">**Element**</span></span>|<span data-ttu-id="cb92d-114">**型**</span><span class="sxs-lookup"><span data-stu-id="cb92d-114">**Type**</span></span>|<span data-ttu-id="cb92d-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb92d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cb92d-116">Icon</span><span class="sxs-lookup"><span data-stu-id="cb92d-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb92d-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="cb92d-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cb92d-118">属性</span><span class="sxs-lookup"><span data-stu-id="cb92d-118">Attributes</span></span>

|<span data-ttu-id="cb92d-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="cb92d-119">**Attribute**</span></span>|<span data-ttu-id="cb92d-120">**型**</span><span class="sxs-lookup"><span data-stu-id="cb92d-120">**Type**</span></span>|<span data-ttu-id="cb92d-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="cb92d-121">**Required**</span></span>|<span data-ttu-id="cb92d-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb92d-122">**Description**</span></span>|<span data-ttu-id="cb92d-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="cb92d-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cb92d-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="cb92d-124">AlignName</span></span>  <br/> |<span data-ttu-id="cb92d-125">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="cb92d-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cb92d-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb92d-126">optional</span></span>  <br/> ||<span data-ttu-id="cb92d-127">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb92d-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cb92d-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="cb92d-128">IconSize</span></span>  <br/> |<span data-ttu-id="cb92d-129">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="cb92d-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cb92d-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb92d-130">optional</span></span>  <br/> ||<span data-ttu-id="cb92d-131">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb92d-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cb92d-132">ID</span><span class="sxs-lookup"><span data-stu-id="cb92d-132">ID</span></span>  <br/> |<span data-ttu-id="cb92d-133">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="cb92d-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cb92d-134">必須</span><span class="sxs-lookup"><span data-stu-id="cb92d-134">required</span></span>  <br/> ||<span data-ttu-id="cb92d-135">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb92d-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cb92d-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="cb92d-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="cb92d-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="cb92d-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cb92d-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb92d-138">optional</span></span>  <br/> ||<span data-ttu-id="cb92d-139">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb92d-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cb92d-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="cb92d-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="cb92d-141">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="cb92d-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cb92d-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb92d-142">optional</span></span>  <br/> ||<span data-ttu-id="cb92d-143">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb92d-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cb92d-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="cb92d-144">MasterType</span></span>  <br/> |<span data-ttu-id="cb92d-145">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="cb92d-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cb92d-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb92d-146">optional</span></span>  <br/> ||<span data-ttu-id="cb92d-147">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb92d-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cb92d-148">名前</span><span class="sxs-lookup"><span data-stu-id="cb92d-148">Name</span></span>  <br/> |<span data-ttu-id="cb92d-149">xsd: string</span><span class="sxs-lookup"><span data-stu-id="cb92d-149">xsd:string</span></span>  <br/> |<span data-ttu-id="cb92d-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb92d-150">optional</span></span>  <br/> ||<span data-ttu-id="cb92d-151">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb92d-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb92d-152">NameU</span><span class="sxs-lookup"><span data-stu-id="cb92d-152">NameU</span></span>  <br/> |<span data-ttu-id="cb92d-153">xsd: string</span><span class="sxs-lookup"><span data-stu-id="cb92d-153">xsd:string</span></span>  <br/> |<span data-ttu-id="cb92d-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb92d-154">optional</span></span>  <br/> ||<span data-ttu-id="cb92d-155">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb92d-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb92d-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="cb92d-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="cb92d-157">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="cb92d-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cb92d-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb92d-158">optional</span></span>  <br/> ||<span data-ttu-id="cb92d-159">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb92d-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cb92d-160">プロンプト</span><span class="sxs-lookup"><span data-stu-id="cb92d-160">Prompt</span></span>  <br/> |<span data-ttu-id="cb92d-161">xsd: string</span><span class="sxs-lookup"><span data-stu-id="cb92d-161">xsd:string</span></span>  <br/> |<span data-ttu-id="cb92d-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb92d-162">optional</span></span>  <br/> ||<span data-ttu-id="cb92d-163">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb92d-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb92d-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="cb92d-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="cb92d-165">xsd: string</span><span class="sxs-lookup"><span data-stu-id="cb92d-165">xsd:string</span></span>  <br/> |<span data-ttu-id="cb92d-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb92d-166">optional</span></span>  <br/> ||<span data-ttu-id="cb92d-167">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb92d-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb92d-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="cb92d-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="cb92d-169">xsd: string</span><span class="sxs-lookup"><span data-stu-id="cb92d-169">xsd:string</span></span>  <br/> |<span data-ttu-id="cb92d-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb92d-170">optional</span></span>  <br/> ||<span data-ttu-id="cb92d-171">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="cb92d-171">Values of the xsd:string type.</span></span>  <br/> |
   

