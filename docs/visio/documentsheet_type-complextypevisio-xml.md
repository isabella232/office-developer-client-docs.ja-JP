---
title: DocumentSheet_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: 47378b039d11294dcb566f61cf20b0ed1ed7fed8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805263"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="04791-102">DocumentSheet_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="04791-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="04791-103">型情報</span><span class="sxs-lookup"><span data-stu-id="04791-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04791-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="04791-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="04791-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="04791-105">**Schema file**</span></span> <br/> |<span data-ttu-id="04791-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="04791-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="04791-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="04791-107">**Extension base**</span></span> <br/> |<span data-ttu-id="04791-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="04791-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="04791-109">定義</span><span class="sxs-lookup"><span data-stu-id="04791-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
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
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="04791-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="04791-110">Elements and attributes</span></span>

<span data-ttu-id="04791-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="04791-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="04791-112">子要素</span><span class="sxs-lookup"><span data-stu-id="04791-112">Child elements</span></span>

<span data-ttu-id="04791-113">なし。</span><span class="sxs-lookup"><span data-stu-id="04791-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04791-114">属性</span><span class="sxs-lookup"><span data-stu-id="04791-114">Attributes</span></span>

|<span data-ttu-id="04791-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="04791-115">**Attribute**</span></span>|<span data-ttu-id="04791-116">**型**</span><span class="sxs-lookup"><span data-stu-id="04791-116">**Type**</span></span>|<span data-ttu-id="04791-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="04791-117">**Required**</span></span>|<span data-ttu-id="04791-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="04791-118">**Description**</span></span>|<span data-ttu-id="04791-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="04791-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="04791-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="04791-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="04791-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="04791-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="04791-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="04791-122">optional</span></span>  <br/> ||<span data-ttu-id="04791-123">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04791-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="04791-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="04791-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="04791-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="04791-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="04791-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="04791-126">optional</span></span>  <br/> ||<span data-ttu-id="04791-127">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04791-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="04791-128">名前</span><span class="sxs-lookup"><span data-stu-id="04791-128">Name</span></span>  <br/> |<span data-ttu-id="04791-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="04791-129">xsd:string</span></span>  <br/> |<span data-ttu-id="04791-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="04791-130">optional</span></span>  <br/> ||<span data-ttu-id="04791-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04791-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="04791-132">NameU</span><span class="sxs-lookup"><span data-stu-id="04791-132">NameU</span></span>  <br/> |<span data-ttu-id="04791-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="04791-133">xsd:string</span></span>  <br/> |<span data-ttu-id="04791-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="04791-134">optional</span></span>  <br/> ||<span data-ttu-id="04791-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04791-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="04791-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="04791-136">UniqueID</span></span>  <br/> |<span data-ttu-id="04791-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="04791-137">xsd:string</span></span>  <br/> |<span data-ttu-id="04791-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="04791-138">optional</span></span>  <br/> ||<span data-ttu-id="04791-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04791-139">Values of the xsd:string type.</span></span>  <br/> |
   

