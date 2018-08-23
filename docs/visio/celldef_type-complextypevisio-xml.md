---
title: CellDef_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: 6471158df8c89e8d7b0202f9bdbce196e24b93b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804977"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="43a71-102">CellDef_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="43a71-102">CellDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="43a71-103">型情報</span><span class="sxs-lookup"><span data-stu-id="43a71-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43a71-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="43a71-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="43a71-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="43a71-105">**Schema file**</span></span> <br/> |<span data-ttu-id="43a71-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="43a71-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="43a71-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="43a71-107">**Extension base**</span></span> <br/> |<span data-ttu-id="43a71-108">なし</span><span class="sxs-lookup"><span data-stu-id="43a71-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="43a71-109">定義</span><span class="sxs-lookup"><span data-stu-id="43a71-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="43a71-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="43a71-110">Elements and attributes</span></span>

<span data-ttu-id="43a71-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="43a71-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="43a71-112">子要素</span><span class="sxs-lookup"><span data-stu-id="43a71-112">Child elements</span></span>

<span data-ttu-id="43a71-113">なし。</span><span class="sxs-lookup"><span data-stu-id="43a71-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43a71-114">属性</span><span class="sxs-lookup"><span data-stu-id="43a71-114">Attributes</span></span>

|<span data-ttu-id="43a71-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="43a71-115">**Attribute**</span></span>|<span data-ttu-id="43a71-116">**型**</span><span class="sxs-lookup"><span data-stu-id="43a71-116">**Type**</span></span>|<span data-ttu-id="43a71-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="43a71-117">**Required**</span></span>|<span data-ttu-id="43a71-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="43a71-118">**Description**</span></span>|<span data-ttu-id="43a71-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="43a71-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="43a71-120">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="43a71-120">F</span></span>  <br/> |<span data-ttu-id="43a71-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="43a71-121">xsd:string</span></span>  <br/> |<span data-ttu-id="43a71-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="43a71-122">optional</span></span>  <br/> ||<span data-ttu-id="43a71-123">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43a71-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="43a71-124">IX</span><span class="sxs-lookup"><span data-stu-id="43a71-124">IX</span></span>  <br/> |<span data-ttu-id="43a71-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="43a71-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="43a71-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="43a71-126">optional</span></span>  <br/> ||<span data-ttu-id="43a71-127">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43a71-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="43a71-128">N</span><span class="sxs-lookup"><span data-stu-id="43a71-128">N</span></span>  <br/> |<span data-ttu-id="43a71-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="43a71-129">xsd:string</span></span>  <br/> |<span data-ttu-id="43a71-130">必須</span><span class="sxs-lookup"><span data-stu-id="43a71-130">required</span></span>  <br/> ||<span data-ttu-id="43a71-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43a71-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="43a71-132">S</span><span class="sxs-lookup"><span data-stu-id="43a71-132">S</span></span>  <br/> |<span data-ttu-id="43a71-133">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="43a71-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="43a71-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="43a71-134">optional</span></span>  <br/> ||<span data-ttu-id="43a71-135">Xsd:unsignedByte の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43a71-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="43a71-136">SV 要素</span><span class="sxs-lookup"><span data-stu-id="43a71-136">T</span></span>  <br/> |<span data-ttu-id="43a71-137">xsd:token</span><span class="sxs-lookup"><span data-stu-id="43a71-137">xsd:token</span></span>  <br/> |<span data-ttu-id="43a71-138">必須</span><span class="sxs-lookup"><span data-stu-id="43a71-138">required</span></span>  <br/> ||<span data-ttu-id="43a71-139">Xsd:token の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43a71-139">Values of the xsd:token type.</span></span>  <br/> |
   

