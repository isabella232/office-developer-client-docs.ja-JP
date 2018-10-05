---
title: CellDef_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: bdcfadc36f278fc97b8589b2989d214e5f4b3333
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399985"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="005cc-102">CellDef_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="005cc-102">CellDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="005cc-103">型情報</span><span class="sxs-lookup"><span data-stu-id="005cc-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="005cc-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="005cc-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="005cc-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="005cc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="005cc-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="005cc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="005cc-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="005cc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="005cc-108">なし</span><span class="sxs-lookup"><span data-stu-id="005cc-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="005cc-109">定義</span><span class="sxs-lookup"><span data-stu-id="005cc-109">Definition</span></span>

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="005cc-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="005cc-110">Elements and attributes</span></span>

<span data-ttu-id="005cc-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="005cc-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="005cc-112">子要素</span><span class="sxs-lookup"><span data-stu-id="005cc-112">Child elements</span></span>

<span data-ttu-id="005cc-113">なし。</span><span class="sxs-lookup"><span data-stu-id="005cc-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="005cc-114">属性</span><span class="sxs-lookup"><span data-stu-id="005cc-114">Attributes</span></span>

|<span data-ttu-id="005cc-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="005cc-115">**Attribute**</span></span>|<span data-ttu-id="005cc-116">**型**</span><span class="sxs-lookup"><span data-stu-id="005cc-116">**Type**</span></span>|<span data-ttu-id="005cc-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="005cc-117">**Required**</span></span>|<span data-ttu-id="005cc-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="005cc-118">**Description**</span></span>|<span data-ttu-id="005cc-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="005cc-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="005cc-120">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="005cc-120">F</span></span>  <br/> |<span data-ttu-id="005cc-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="005cc-121">xsd:string</span></span>  <br/> |<span data-ttu-id="005cc-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="005cc-122">optional</span></span>  <br/> ||<span data-ttu-id="005cc-123">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="005cc-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="005cc-124">IX</span><span class="sxs-lookup"><span data-stu-id="005cc-124">IX</span></span>  <br/> |<span data-ttu-id="005cc-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="005cc-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="005cc-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="005cc-126">optional</span></span>  <br/> ||<span data-ttu-id="005cc-127">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="005cc-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="005cc-128">N</span><span class="sxs-lookup"><span data-stu-id="005cc-128">N</span></span>  <br/> |<span data-ttu-id="005cc-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="005cc-129">xsd:string</span></span>  <br/> |<span data-ttu-id="005cc-130">必須</span><span class="sxs-lookup"><span data-stu-id="005cc-130">required</span></span>  <br/> ||<span data-ttu-id="005cc-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="005cc-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="005cc-132">S</span><span class="sxs-lookup"><span data-stu-id="005cc-132">S</span></span>  <br/> |<span data-ttu-id="005cc-133">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="005cc-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="005cc-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="005cc-134">optional</span></span>  <br/> ||<span data-ttu-id="005cc-135">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="005cc-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="005cc-136">SV 要素</span><span class="sxs-lookup"><span data-stu-id="005cc-136">T</span></span>  <br/> |<span data-ttu-id="005cc-137">xsd:token</span><span class="sxs-lookup"><span data-stu-id="005cc-137">xsd:token</span></span>  <br/> |<span data-ttu-id="005cc-138">必須</span><span class="sxs-lookup"><span data-stu-id="005cc-138">required</span></span>  <br/> ||<span data-ttu-id="005cc-139">Xsd:token の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="005cc-139">Values of the xsd:token type.</span></span>  <br/> |
   

