---
title: Section_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 48dd7a0ffc487b4a7a4200505f08d0aca42fd3c6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542129"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="1c810-102">Section_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1c810-102">Section_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1c810-103">型情報</span><span class="sxs-lookup"><span data-stu-id="1c810-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c810-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1c810-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1c810-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1c810-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1c810-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="1c810-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1c810-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="1c810-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1c810-108">None</span><span class="sxs-lookup"><span data-stu-id="1c810-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1c810-109">定義</span><span class="sxs-lookup"><span data-stu-id="1c810-109">Definition</span></span>

```XML
          <xs:complexType name="Section_Type">
          
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Row"  type="Row_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1c810-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1c810-110">Elements and attributes</span></span>

<span data-ttu-id="1c810-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c810-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1c810-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1c810-112">Child elements</span></span>

|<span data-ttu-id="1c810-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c810-113">**Element**</span></span>|<span data-ttu-id="1c810-114">**型**</span><span class="sxs-lookup"><span data-stu-id="1c810-114">**Type**</span></span>|<span data-ttu-id="1c810-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="1c810-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1c810-116">Cell</span><span class="sxs-lookup"><span data-stu-id="1c810-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="1c810-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1c810-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1c810-118">行</span><span class="sxs-lookup"><span data-stu-id="1c810-118">Row</span></span>](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="1c810-119">Row_Type</span><span class="sxs-lookup"><span data-stu-id="1c810-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1c810-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="1c810-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="1c810-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="1c810-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1c810-122">属性</span><span class="sxs-lookup"><span data-stu-id="1c810-122">Attributes</span></span>

|<span data-ttu-id="1c810-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="1c810-123">**Attribute**</span></span>|<span data-ttu-id="1c810-124">**型**</span><span class="sxs-lookup"><span data-stu-id="1c810-124">**Type**</span></span>|<span data-ttu-id="1c810-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="1c810-125">**Required**</span></span>|<span data-ttu-id="1c810-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="1c810-126">**Description**</span></span>|<span data-ttu-id="1c810-127">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="1c810-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1c810-128">Del</span><span class="sxs-lookup"><span data-stu-id="1c810-128">Del</span></span>  <br/> |<span data-ttu-id="1c810-129">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="1c810-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1c810-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="1c810-130">optional</span></span>  <br/> ||<span data-ttu-id="1c810-131">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="1c810-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1c810-132">IX</span><span class="sxs-lookup"><span data-stu-id="1c810-132">IX</span></span>  <br/> |<span data-ttu-id="1c810-133">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="1c810-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1c810-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="1c810-134">optional</span></span>  <br/> ||<span data-ttu-id="1c810-135">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="1c810-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1c810-136">N</span><span class="sxs-lookup"><span data-stu-id="1c810-136">N</span></span>  <br/> |<span data-ttu-id="1c810-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="1c810-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1c810-138">必須</span><span class="sxs-lookup"><span data-stu-id="1c810-138">required</span></span>  <br/> ||<span data-ttu-id="1c810-139">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1c810-139">Values of the xsd:string type.</span></span>  <br/> |
   

