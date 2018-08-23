---
title: ColorEntry_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: 58a0abdd4f7f8c2014ec8c6763441840a07b93db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805017"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="95690-102">ColorEntry_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="95690-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="95690-103">型情報</span><span class="sxs-lookup"><span data-stu-id="95690-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95690-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="95690-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="95690-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="95690-105">**Schema file**</span></span> <br/> |<span data-ttu-id="95690-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="95690-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="95690-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="95690-107">**Extension base**</span></span> <br/> |<span data-ttu-id="95690-108">なし</span><span class="sxs-lookup"><span data-stu-id="95690-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95690-109">定義</span><span class="sxs-lookup"><span data-stu-id="95690-109">Definition</span></span>

```XML
      <xs:complexType name="ColorEntry_Type">
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RGB"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="95690-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="95690-110">Elements and attributes</span></span>

<span data-ttu-id="95690-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="95690-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="95690-112">子要素</span><span class="sxs-lookup"><span data-stu-id="95690-112">Child elements</span></span>

<span data-ttu-id="95690-113">なし。</span><span class="sxs-lookup"><span data-stu-id="95690-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95690-114">属性</span><span class="sxs-lookup"><span data-stu-id="95690-114">Attributes</span></span>

|<span data-ttu-id="95690-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="95690-115">**Attribute**</span></span>|<span data-ttu-id="95690-116">**型**</span><span class="sxs-lookup"><span data-stu-id="95690-116">**Type**</span></span>|<span data-ttu-id="95690-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="95690-117">**Required**</span></span>|<span data-ttu-id="95690-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="95690-118">**Description**</span></span>|<span data-ttu-id="95690-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="95690-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="95690-120">IX</span><span class="sxs-lookup"><span data-stu-id="95690-120">IX</span></span>  <br/> |<span data-ttu-id="95690-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="95690-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="95690-122">必須</span><span class="sxs-lookup"><span data-stu-id="95690-122">required</span></span>  <br/> ||<span data-ttu-id="95690-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95690-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="95690-124">RGB</span><span class="sxs-lookup"><span data-stu-id="95690-124">RGB</span></span>  <br/> |<span data-ttu-id="95690-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="95690-125">xsd:string</span></span>  <br/> |<span data-ttu-id="95690-126">必須</span><span class="sxs-lookup"><span data-stu-id="95690-126">required</span></span>  <br/> ||<span data-ttu-id="95690-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="95690-127">Values of the xsd:string type.</span></span>  <br/> |
   

