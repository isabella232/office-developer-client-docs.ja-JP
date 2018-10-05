---
title: Section_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 35cd638d36f4ddd1d90e0c312e65626f7d8b0bff
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384298"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="18f60-102">Section_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="18f60-102">Section_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="18f60-103">型情報</span><span class="sxs-lookup"><span data-stu-id="18f60-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18f60-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="18f60-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="18f60-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="18f60-105">**Schema file**</span></span> <br/> |<span data-ttu-id="18f60-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="18f60-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="18f60-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="18f60-107">**Extension base**</span></span> <br/> |<span data-ttu-id="18f60-108">なし</span><span class="sxs-lookup"><span data-stu-id="18f60-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="18f60-109">定義</span><span class="sxs-lookup"><span data-stu-id="18f60-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="18f60-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="18f60-110">Elements and attributes</span></span>

<span data-ttu-id="18f60-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="18f60-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="18f60-112">子要素</span><span class="sxs-lookup"><span data-stu-id="18f60-112">Child elements</span></span>

|<span data-ttu-id="18f60-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="18f60-113">**Element**</span></span>|<span data-ttu-id="18f60-114">**型**</span><span class="sxs-lookup"><span data-stu-id="18f60-114">**Type**</span></span>|<span data-ttu-id="18f60-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="18f60-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="18f60-116">Cell</span><span class="sxs-lookup"><span data-stu-id="18f60-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="18f60-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="18f60-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="18f60-118">Row</span><span class="sxs-lookup"><span data-stu-id="18f60-118">Row</span></span>](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="18f60-119">Row_Type</span><span class="sxs-lookup"><span data-stu-id="18f60-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="18f60-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="18f60-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="18f60-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="18f60-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="18f60-122">属性</span><span class="sxs-lookup"><span data-stu-id="18f60-122">Attributes</span></span>

|<span data-ttu-id="18f60-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="18f60-123">**Attribute**</span></span>|<span data-ttu-id="18f60-124">**型**</span><span class="sxs-lookup"><span data-stu-id="18f60-124">**Type**</span></span>|<span data-ttu-id="18f60-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="18f60-125">**Required**</span></span>|<span data-ttu-id="18f60-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="18f60-126">**Description**</span></span>|<span data-ttu-id="18f60-127">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="18f60-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="18f60-128">Del</span><span class="sxs-lookup"><span data-stu-id="18f60-128">Del</span></span>  <br/> |<span data-ttu-id="18f60-129">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="18f60-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="18f60-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="18f60-130">optional</span></span>  <br/> ||<span data-ttu-id="18f60-131">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18f60-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="18f60-132">IX</span><span class="sxs-lookup"><span data-stu-id="18f60-132">IX</span></span>  <br/> |<span data-ttu-id="18f60-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="18f60-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="18f60-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="18f60-134">optional</span></span>  <br/> ||<span data-ttu-id="18f60-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18f60-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="18f60-136">N</span><span class="sxs-lookup"><span data-stu-id="18f60-136">N</span></span>  <br/> |<span data-ttu-id="18f60-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="18f60-137">xsd:string</span></span>  <br/> |<span data-ttu-id="18f60-138">必須</span><span class="sxs-lookup"><span data-stu-id="18f60-138">required</span></span>  <br/> ||<span data-ttu-id="18f60-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18f60-139">Values of the xsd:string type.</span></span>  <br/> |
   

