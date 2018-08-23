---
title: RefBy_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: 5042a618420a72284e0ef75c5d624c6f5464e162
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806151"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="a3a7a-102">RefBy_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a3a7a-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a3a7a-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a3a7a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3a7a-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a3a7a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a3a7a-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a3a7a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a3a7a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a3a7a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a3a7a-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a3a7a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a3a7a-108">なし</span><span class="sxs-lookup"><span data-stu-id="a3a7a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a3a7a-109">定義</span><span class="sxs-lookup"><span data-stu-id="a3a7a-109">Definition</span></span>

```XML
      <xs:complexType name="RefBy_Type">
    <xs:attribute name="T"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a3a7a-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a3a7a-110">Elements and attributes</span></span>

<span data-ttu-id="a3a7a-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3a7a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a3a7a-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a3a7a-112">Child elements</span></span>

<span data-ttu-id="a3a7a-113">なし。</span><span class="sxs-lookup"><span data-stu-id="a3a7a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3a7a-114">属性</span><span class="sxs-lookup"><span data-stu-id="a3a7a-114">Attributes</span></span>

|<span data-ttu-id="a3a7a-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="a3a7a-115">**Attribute**</span></span>|<span data-ttu-id="a3a7a-116">**型**</span><span class="sxs-lookup"><span data-stu-id="a3a7a-116">**Type**</span></span>|<span data-ttu-id="a3a7a-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="a3a7a-117">**Required**</span></span>|<span data-ttu-id="a3a7a-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="a3a7a-118">**Description**</span></span>|<span data-ttu-id="a3a7a-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="a3a7a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a3a7a-120">ID</span><span class="sxs-lookup"><span data-stu-id="a3a7a-120">ID</span></span>  <br/> |<span data-ttu-id="a3a7a-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a3a7a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a3a7a-122">必須</span><span class="sxs-lookup"><span data-stu-id="a3a7a-122">required</span></span>  <br/> ||<span data-ttu-id="a3a7a-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a3a7a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a3a7a-124">SV 要素</span><span class="sxs-lookup"><span data-stu-id="a3a7a-124">T</span></span>  <br/> |<span data-ttu-id="a3a7a-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a3a7a-125">xsd:string</span></span>  <br/> |<span data-ttu-id="a3a7a-126">必須</span><span class="sxs-lookup"><span data-stu-id="a3a7a-126">required</span></span>  <br/> ||<span data-ttu-id="a3a7a-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a3a7a-127">Values of the xsd:string type.</span></span>  <br/> |
   

