---
title: ColorEntry_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: c5f2cafba60cd8157f80dc548cea328d179e74db
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394910"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="04532-102">ColorEntry_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="04532-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="04532-103">型情報</span><span class="sxs-lookup"><span data-stu-id="04532-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04532-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="04532-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="04532-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="04532-105">**Schema file**</span></span> <br/> |<span data-ttu-id="04532-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="04532-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="04532-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="04532-107">**Extension base**</span></span> <br/> |<span data-ttu-id="04532-108">なし</span><span class="sxs-lookup"><span data-stu-id="04532-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="04532-109">定義</span><span class="sxs-lookup"><span data-stu-id="04532-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="04532-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="04532-110">Elements and attributes</span></span>

<span data-ttu-id="04532-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="04532-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="04532-112">子要素</span><span class="sxs-lookup"><span data-stu-id="04532-112">Child elements</span></span>

<span data-ttu-id="04532-113">なし。</span><span class="sxs-lookup"><span data-stu-id="04532-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04532-114">属性</span><span class="sxs-lookup"><span data-stu-id="04532-114">Attributes</span></span>

|<span data-ttu-id="04532-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="04532-115">**Attribute**</span></span>|<span data-ttu-id="04532-116">**型**</span><span class="sxs-lookup"><span data-stu-id="04532-116">**Type**</span></span>|<span data-ttu-id="04532-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="04532-117">**Required**</span></span>|<span data-ttu-id="04532-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="04532-118">**Description**</span></span>|<span data-ttu-id="04532-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="04532-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="04532-120">IX</span><span class="sxs-lookup"><span data-stu-id="04532-120">IX</span></span>  <br/> |<span data-ttu-id="04532-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="04532-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="04532-122">必須</span><span class="sxs-lookup"><span data-stu-id="04532-122">required</span></span>  <br/> ||<span data-ttu-id="04532-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04532-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="04532-124">RGB</span><span class="sxs-lookup"><span data-stu-id="04532-124">RGB</span></span>  <br/> |<span data-ttu-id="04532-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="04532-125">xsd:string</span></span>  <br/> |<span data-ttu-id="04532-126">必須</span><span class="sxs-lookup"><span data-stu-id="04532-126">required</span></span>  <br/> ||<span data-ttu-id="04532-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04532-127">Values of the xsd:string type.</span></span>  <br/> |
   

