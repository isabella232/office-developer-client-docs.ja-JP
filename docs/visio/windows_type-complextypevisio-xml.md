---
title: Windows_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 33a2acaad76543115c480b5e9a32ddba8fb0d66a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806792"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="d0163-102">Windows_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="d0163-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d0163-103">型情報</span><span class="sxs-lookup"><span data-stu-id="d0163-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0163-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="d0163-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d0163-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d0163-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d0163-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d0163-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d0163-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="d0163-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d0163-108">なし</span><span class="sxs-lookup"><span data-stu-id="d0163-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d0163-109">定義</span><span class="sxs-lookup"><span data-stu-id="d0163-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d0163-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d0163-110">Elements and attributes</span></span>

<span data-ttu-id="d0163-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0163-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d0163-112">子要素</span><span class="sxs-lookup"><span data-stu-id="d0163-112">Child elements</span></span>

|<span data-ttu-id="d0163-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="d0163-113">**Element**</span></span>|<span data-ttu-id="d0163-114">**型**</span><span class="sxs-lookup"><span data-stu-id="d0163-114">**Type**</span></span>|<span data-ttu-id="d0163-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="d0163-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d0163-116">Window</span><span class="sxs-lookup"><span data-stu-id="d0163-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d0163-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="d0163-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d0163-118">属性</span><span class="sxs-lookup"><span data-stu-id="d0163-118">Attributes</span></span>

|<span data-ttu-id="d0163-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="d0163-119">**Attribute**</span></span>|<span data-ttu-id="d0163-120">**型**</span><span class="sxs-lookup"><span data-stu-id="d0163-120">**Type**</span></span>|<span data-ttu-id="d0163-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="d0163-121">**Required**</span></span>|<span data-ttu-id="d0163-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="d0163-122">**Description**</span></span>|<span data-ttu-id="d0163-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="d0163-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d0163-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="d0163-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="d0163-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d0163-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d0163-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="d0163-126">optional</span></span>  <br/> ||<span data-ttu-id="d0163-127">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0163-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d0163-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="d0163-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="d0163-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d0163-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d0163-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="d0163-130">optional</span></span>  <br/> ||<span data-ttu-id="d0163-131">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0163-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

