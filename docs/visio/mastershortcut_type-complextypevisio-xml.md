---
title: MasterShortcut_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: 23d5de92be151b9ab6819296456746087573e7c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341693"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="60794-102">MasterShortcut_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="60794-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="60794-103">型情報</span><span class="sxs-lookup"><span data-stu-id="60794-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60794-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="60794-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="60794-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="60794-105">**Schema file**</span></span> <br/> |<span data-ttu-id="60794-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="60794-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="60794-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="60794-107">**Extension base**</span></span> <br/> |<span data-ttu-id="60794-108">なし</span><span class="sxs-lookup"><span data-stu-id="60794-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="60794-109">定義</span><span class="sxs-lookup"><span data-stu-id="60794-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="60794-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="60794-110">Elements and attributes</span></span>

<span data-ttu-id="60794-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="60794-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="60794-112">子要素</span><span class="sxs-lookup"><span data-stu-id="60794-112">Child elements</span></span>

|<span data-ttu-id="60794-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="60794-113">**Element**</span></span>|<span data-ttu-id="60794-114">**型**</span><span class="sxs-lookup"><span data-stu-id="60794-114">**Type**</span></span>|<span data-ttu-id="60794-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="60794-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="60794-116">Icon</span><span class="sxs-lookup"><span data-stu-id="60794-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="60794-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="60794-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="60794-118">属性</span><span class="sxs-lookup"><span data-stu-id="60794-118">Attributes</span></span>

|<span data-ttu-id="60794-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="60794-119">**Attribute**</span></span>|<span data-ttu-id="60794-120">**型**</span><span class="sxs-lookup"><span data-stu-id="60794-120">**Type**</span></span>|<span data-ttu-id="60794-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="60794-121">**Required**</span></span>|<span data-ttu-id="60794-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="60794-122">**Description**</span></span>|<span data-ttu-id="60794-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="60794-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="60794-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="60794-124">AlignName</span></span>  <br/> |<span data-ttu-id="60794-125">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="60794-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="60794-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="60794-126">optional</span></span>  <br/> ||<span data-ttu-id="60794-127">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="60794-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="60794-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="60794-128">IconSize</span></span>  <br/> |<span data-ttu-id="60794-129">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="60794-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="60794-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="60794-130">optional</span></span>  <br/> ||<span data-ttu-id="60794-131">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="60794-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="60794-132">ID</span><span class="sxs-lookup"><span data-stu-id="60794-132">ID</span></span>  <br/> |<span data-ttu-id="60794-133">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="60794-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="60794-134">必須</span><span class="sxs-lookup"><span data-stu-id="60794-134">required</span></span>  <br/> ||<span data-ttu-id="60794-135">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="60794-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="60794-136">iscustomname</span><span class="sxs-lookup"><span data-stu-id="60794-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="60794-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="60794-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="60794-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="60794-138">optional</span></span>  <br/> ||<span data-ttu-id="60794-139">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="60794-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="60794-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="60794-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="60794-141">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="60794-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="60794-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="60794-142">optional</span></span>  <br/> ||<span data-ttu-id="60794-143">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="60794-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="60794-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="60794-144">MasterType</span></span>  <br/> |<span data-ttu-id="60794-145">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="60794-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="60794-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="60794-146">optional</span></span>  <br/> ||<span data-ttu-id="60794-147">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="60794-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="60794-148">名前</span><span class="sxs-lookup"><span data-stu-id="60794-148">Name</span></span>  <br/> |<span data-ttu-id="60794-149">xsd: string</span><span class="sxs-lookup"><span data-stu-id="60794-149">xsd:string</span></span>  <br/> |<span data-ttu-id="60794-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="60794-150">optional</span></span>  <br/> ||<span data-ttu-id="60794-151">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="60794-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="60794-152">NameU</span><span class="sxs-lookup"><span data-stu-id="60794-152">NameU</span></span>  <br/> |<span data-ttu-id="60794-153">xsd: string</span><span class="sxs-lookup"><span data-stu-id="60794-153">xsd:string</span></span>  <br/> |<span data-ttu-id="60794-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="60794-154">optional</span></span>  <br/> ||<span data-ttu-id="60794-155">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="60794-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="60794-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="60794-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="60794-157">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="60794-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="60794-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="60794-158">optional</span></span>  <br/> ||<span data-ttu-id="60794-159">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="60794-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="60794-160">プロンプト</span><span class="sxs-lookup"><span data-stu-id="60794-160">Prompt</span></span>  <br/> |<span data-ttu-id="60794-161">xsd: string</span><span class="sxs-lookup"><span data-stu-id="60794-161">xsd:string</span></span>  <br/> |<span data-ttu-id="60794-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="60794-162">optional</span></span>  <br/> ||<span data-ttu-id="60794-163">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="60794-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="60794-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="60794-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="60794-165">xsd: string</span><span class="sxs-lookup"><span data-stu-id="60794-165">xsd:string</span></span>  <br/> |<span data-ttu-id="60794-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="60794-166">optional</span></span>  <br/> ||<span data-ttu-id="60794-167">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="60794-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="60794-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="60794-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="60794-169">xsd: string</span><span class="sxs-lookup"><span data-stu-id="60794-169">xsd:string</span></span>  <br/> |<span data-ttu-id="60794-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="60794-170">optional</span></span>  <br/> ||<span data-ttu-id="60794-171">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="60794-171">Values of the xsd:string type.</span></span>  <br/> |
   

