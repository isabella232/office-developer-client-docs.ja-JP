---
title: AuthorEntry_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 39cf47915230b18d22db78f5470fd9c26b9c77ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804773"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="09a15-102">AuthorEntry_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="09a15-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="09a15-103">型情報</span><span class="sxs-lookup"><span data-stu-id="09a15-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09a15-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="09a15-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="09a15-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="09a15-105">**Schema file**</span></span> <br/> |<span data-ttu-id="09a15-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="09a15-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="09a15-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="09a15-107">**Extension base**</span></span> <br/> |<span data-ttu-id="09a15-108">なし</span><span class="sxs-lookup"><span data-stu-id="09a15-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="09a15-109">定義</span><span class="sxs-lookup"><span data-stu-id="09a15-109">Definition</span></span>

```XML
      <xs:complexType name="AuthorEntry_Type">
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="Initials"
  type="xsd:string"
    />
    <xs:attribute name="ResolutionID"
  type="xsd:string"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="09a15-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="09a15-110">Elements and attributes</span></span>

<span data-ttu-id="09a15-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="09a15-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="09a15-112">子要素</span><span class="sxs-lookup"><span data-stu-id="09a15-112">Child elements</span></span>

<span data-ttu-id="09a15-113">なし。</span><span class="sxs-lookup"><span data-stu-id="09a15-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09a15-114">属性</span><span class="sxs-lookup"><span data-stu-id="09a15-114">Attributes</span></span>

|<span data-ttu-id="09a15-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="09a15-115">**Attribute**</span></span>|<span data-ttu-id="09a15-116">**型**</span><span class="sxs-lookup"><span data-stu-id="09a15-116">**Type**</span></span>|<span data-ttu-id="09a15-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="09a15-117">**Required**</span></span>|<span data-ttu-id="09a15-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="09a15-118">**Description**</span></span>|<span data-ttu-id="09a15-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="09a15-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="09a15-120">ID</span><span class="sxs-lookup"><span data-stu-id="09a15-120">ID</span></span>  <br/> |<span data-ttu-id="09a15-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="09a15-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="09a15-122">必須</span><span class="sxs-lookup"><span data-stu-id="09a15-122">required</span></span>  <br/> ||<span data-ttu-id="09a15-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="09a15-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="09a15-124">Initials</span><span class="sxs-lookup"><span data-stu-id="09a15-124">Initials</span></span>  <br/> |<span data-ttu-id="09a15-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="09a15-125">xsd:string</span></span>  <br/> |<span data-ttu-id="09a15-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="09a15-126">optional</span></span>  <br/> ||<span data-ttu-id="09a15-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="09a15-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="09a15-128">名前</span><span class="sxs-lookup"><span data-stu-id="09a15-128">Name</span></span>  <br/> |<span data-ttu-id="09a15-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="09a15-129">xsd:string</span></span>  <br/> |<span data-ttu-id="09a15-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="09a15-130">optional</span></span>  <br/> ||<span data-ttu-id="09a15-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="09a15-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="09a15-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="09a15-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="09a15-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="09a15-133">xsd:string</span></span>  <br/> |<span data-ttu-id="09a15-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="09a15-134">optional</span></span>  <br/> ||<span data-ttu-id="09a15-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="09a15-135">Values of the xsd:string type.</span></span>  <br/> |
   

