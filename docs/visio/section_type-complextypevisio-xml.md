---
title: Section_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 8eb9362f84849ad22a20662b327ae33cd795cc5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806356"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="1dbed-102">Section_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="1dbed-102">Section_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1dbed-103">型情報</span><span class="sxs-lookup"><span data-stu-id="1dbed-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1dbed-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="1dbed-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1dbed-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1dbed-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1dbed-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1dbed-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1dbed-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="1dbed-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1dbed-108">なし</span><span class="sxs-lookup"><span data-stu-id="1dbed-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1dbed-109">定義</span><span class="sxs-lookup"><span data-stu-id="1dbed-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1dbed-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1dbed-110">Elements and attributes</span></span>

<span data-ttu-id="1dbed-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1dbed-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1dbed-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1dbed-112">Child elements</span></span>

|<span data-ttu-id="1dbed-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="1dbed-113">**Element**</span></span>|<span data-ttu-id="1dbed-114">**型**</span><span class="sxs-lookup"><span data-stu-id="1dbed-114">**Type**</span></span>|<span data-ttu-id="1dbed-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="1dbed-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1dbed-116">Cell</span><span class="sxs-lookup"><span data-stu-id="1dbed-116">Cell</span></span>](http://msdn.microsoft.com/library/70a9d6d6-a4ff-2b0d-febc-789a04a2f5b0%28Office.15%29.aspx) <br/> |[<span data-ttu-id="1dbed-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1dbed-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1dbed-118">Row</span><span class="sxs-lookup"><span data-stu-id="1dbed-118">Row</span></span>](http://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="1dbed-119">Row_Type</span><span class="sxs-lookup"><span data-stu-id="1dbed-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1dbed-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="1dbed-120">Trigger</span></span>](http://msdn.microsoft.com/library/e4eeb238-f6d0-fb23-db1c-01d55b0a8d88%28Office.15%29.aspx) <br/> |[<span data-ttu-id="1dbed-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="1dbed-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1dbed-122">属性</span><span class="sxs-lookup"><span data-stu-id="1dbed-122">Attributes</span></span>

|<span data-ttu-id="1dbed-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="1dbed-123">**Attribute**</span></span>|<span data-ttu-id="1dbed-124">**型**</span><span class="sxs-lookup"><span data-stu-id="1dbed-124">**Type**</span></span>|<span data-ttu-id="1dbed-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="1dbed-125">**Required**</span></span>|<span data-ttu-id="1dbed-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="1dbed-126">**Description**</span></span>|<span data-ttu-id="1dbed-127">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="1dbed-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1dbed-128">Del</span><span class="sxs-lookup"><span data-stu-id="1dbed-128">Del</span></span>  <br/> |<span data-ttu-id="1dbed-129">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="1dbed-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1dbed-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="1dbed-130">optional</span></span>  <br/> ||<span data-ttu-id="1dbed-131">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1dbed-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1dbed-132">IX</span><span class="sxs-lookup"><span data-stu-id="1dbed-132">IX</span></span>  <br/> |<span data-ttu-id="1dbed-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1dbed-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1dbed-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="1dbed-134">optional</span></span>  <br/> ||<span data-ttu-id="1dbed-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1dbed-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1dbed-136">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="1dbed-136">N</span></span>  <br/> |<span data-ttu-id="1dbed-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1dbed-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1dbed-138">必須</span><span class="sxs-lookup"><span data-stu-id="1dbed-138">required</span></span>  <br/> ||<span data-ttu-id="1dbed-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1dbed-139">Values of the xsd:string type.</span></span>  <br/> |
   

