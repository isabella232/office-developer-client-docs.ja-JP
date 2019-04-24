---
title: Windows_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 5aeffa7b78c4c402d03b6a2774a2df8b339e03e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346446"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="5f989-102">Windows_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="5f989-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5f989-103">型情報</span><span class="sxs-lookup"><span data-stu-id="5f989-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f989-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5f989-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5f989-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5f989-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5f989-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="5f989-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5f989-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="5f989-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5f989-108">なし</span><span class="sxs-lookup"><span data-stu-id="5f989-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5f989-109">定義</span><span class="sxs-lookup"><span data-stu-id="5f989-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5f989-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5f989-110">Elements and attributes</span></span>

<span data-ttu-id="5f989-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f989-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5f989-112">子要素</span><span class="sxs-lookup"><span data-stu-id="5f989-112">Child elements</span></span>

|<span data-ttu-id="5f989-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f989-113">**Element**</span></span>|<span data-ttu-id="5f989-114">**型**</span><span class="sxs-lookup"><span data-stu-id="5f989-114">**Type**</span></span>|<span data-ttu-id="5f989-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="5f989-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5f989-116">Window</span><span class="sxs-lookup"><span data-stu-id="5f989-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5f989-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="5f989-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5f989-118">属性</span><span class="sxs-lookup"><span data-stu-id="5f989-118">Attributes</span></span>

|<span data-ttu-id="5f989-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="5f989-119">**Attribute**</span></span>|<span data-ttu-id="5f989-120">**型**</span><span class="sxs-lookup"><span data-stu-id="5f989-120">**Type**</span></span>|<span data-ttu-id="5f989-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="5f989-121">**Required**</span></span>|<span data-ttu-id="5f989-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="5f989-122">**Description**</span></span>|<span data-ttu-id="5f989-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="5f989-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5f989-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="5f989-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="5f989-125">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="5f989-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="5f989-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="5f989-126">optional</span></span>  <br/> ||<span data-ttu-id="5f989-127">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="5f989-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="5f989-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="5f989-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="5f989-129">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="5f989-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="5f989-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="5f989-130">optional</span></span>  <br/> ||<span data-ttu-id="5f989-131">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="5f989-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

