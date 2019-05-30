---
title: RefBy_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: 7970ae735f4933f05e71f1758912d3ecd382bf89
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538278"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="25b76-102">RefBy_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="25b76-102">RefBy_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="25b76-103">型情報</span><span class="sxs-lookup"><span data-stu-id="25b76-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25b76-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="25b76-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="25b76-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="25b76-105">**Schema file**</span></span> <br/> |<span data-ttu-id="25b76-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="25b76-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="25b76-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="25b76-107">**Extension base**</span></span> <br/> |<span data-ttu-id="25b76-108">None</span><span class="sxs-lookup"><span data-stu-id="25b76-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="25b76-109">定義</span><span class="sxs-lookup"><span data-stu-id="25b76-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="25b76-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="25b76-110">Elements and attributes</span></span>

<span data-ttu-id="25b76-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="25b76-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="25b76-112">子要素</span><span class="sxs-lookup"><span data-stu-id="25b76-112">Child elements</span></span>

<span data-ttu-id="25b76-113">なし。</span><span class="sxs-lookup"><span data-stu-id="25b76-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25b76-114">属性</span><span class="sxs-lookup"><span data-stu-id="25b76-114">Attributes</span></span>

|<span data-ttu-id="25b76-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="25b76-115">**Attribute**</span></span>|<span data-ttu-id="25b76-116">**型**</span><span class="sxs-lookup"><span data-stu-id="25b76-116">**Type**</span></span>|<span data-ttu-id="25b76-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="25b76-117">**Required**</span></span>|<span data-ttu-id="25b76-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="25b76-118">**Description**</span></span>|<span data-ttu-id="25b76-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="25b76-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="25b76-120">ID</span><span class="sxs-lookup"><span data-stu-id="25b76-120">ID</span></span>  <br/> |<span data-ttu-id="25b76-121">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="25b76-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="25b76-122">必須</span><span class="sxs-lookup"><span data-stu-id="25b76-122">required</span></span>  <br/> ||<span data-ttu-id="25b76-123">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="25b76-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="25b76-124">T</span><span class="sxs-lookup"><span data-stu-id="25b76-124">T</span></span>  <br/> |<span data-ttu-id="25b76-125">xsd: string</span><span class="sxs-lookup"><span data-stu-id="25b76-125">xsd:string</span></span>  <br/> |<span data-ttu-id="25b76-126">必須</span><span class="sxs-lookup"><span data-stu-id="25b76-126">required</span></span>  <br/> ||<span data-ttu-id="25b76-127">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="25b76-127">Values of the xsd:string type.</span></span>  <br/> |
   

