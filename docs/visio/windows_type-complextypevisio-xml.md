---
title: Windows_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: b8d8ed39637bdd692b2ba113525f40a3f91ffc9c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538439"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="58a63-102">Windows_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="58a63-102">Windows_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="58a63-103">型情報</span><span class="sxs-lookup"><span data-stu-id="58a63-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58a63-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="58a63-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="58a63-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="58a63-105">**Schema file**</span></span> <br/> |<span data-ttu-id="58a63-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="58a63-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="58a63-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="58a63-107">**Extension base**</span></span> <br/> |<span data-ttu-id="58a63-108">None</span><span class="sxs-lookup"><span data-stu-id="58a63-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="58a63-109">定義</span><span class="sxs-lookup"><span data-stu-id="58a63-109">Definition</span></span>

```XML
          <xs:complexType name="Windows_Type">
          
          <xs:sequence>
    <xs:element name="Window"  type="Window_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ClientWidth"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ClientHeight"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="58a63-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="58a63-110">Elements and attributes</span></span>

<span data-ttu-id="58a63-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="58a63-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="58a63-112">子要素</span><span class="sxs-lookup"><span data-stu-id="58a63-112">Child elements</span></span>

|<span data-ttu-id="58a63-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="58a63-113">**Element**</span></span>|<span data-ttu-id="58a63-114">**型**</span><span class="sxs-lookup"><span data-stu-id="58a63-114">**Type**</span></span>|<span data-ttu-id="58a63-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="58a63-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="58a63-116">Window</span><span class="sxs-lookup"><span data-stu-id="58a63-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="58a63-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="58a63-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="58a63-118">属性</span><span class="sxs-lookup"><span data-stu-id="58a63-118">Attributes</span></span>

|<span data-ttu-id="58a63-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="58a63-119">**Attribute**</span></span>|<span data-ttu-id="58a63-120">**型**</span><span class="sxs-lookup"><span data-stu-id="58a63-120">**Type**</span></span>|<span data-ttu-id="58a63-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="58a63-121">**Required**</span></span>|<span data-ttu-id="58a63-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="58a63-122">**Description**</span></span>|<span data-ttu-id="58a63-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="58a63-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="58a63-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="58a63-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="58a63-125">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="58a63-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="58a63-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="58a63-126">optional</span></span>  <br/> ||<span data-ttu-id="58a63-127">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="58a63-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="58a63-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="58a63-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="58a63-129">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="58a63-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="58a63-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="58a63-130">optional</span></span>  <br/> ||<span data-ttu-id="58a63-131">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="58a63-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

