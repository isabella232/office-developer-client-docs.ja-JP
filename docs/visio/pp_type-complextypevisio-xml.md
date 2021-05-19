---
title: pp_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9259b546-4a4d-81d9-4e0d-cff693d28a56
ms.openlocfilehash: 4e86d95459e7df7c8a145459c268b647e79c6a4c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539006"
---
# <a name="pp_type-complextype-visio-xml"></a><span data-ttu-id="84bdf-102">pp_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="84bdf-102">pp_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="84bdf-103">型情報</span><span class="sxs-lookup"><span data-stu-id="84bdf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84bdf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="84bdf-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="84bdf-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="84bdf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="84bdf-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="84bdf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="84bdf-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="84bdf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="84bdf-108">なし</span><span class="sxs-lookup"><span data-stu-id="84bdf-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="84bdf-109">定義</span><span class="sxs-lookup"><span data-stu-id="84bdf-109">Definition</span></span>

```XML
      <xs:complexType name="pp_Type">
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="84bdf-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="84bdf-110">Elements and attributes</span></span>

<span data-ttu-id="84bdf-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="84bdf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="84bdf-112">子要素</span><span class="sxs-lookup"><span data-stu-id="84bdf-112">Child elements</span></span>

<span data-ttu-id="84bdf-113">なし。</span><span class="sxs-lookup"><span data-stu-id="84bdf-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84bdf-114">属性</span><span class="sxs-lookup"><span data-stu-id="84bdf-114">Attributes</span></span>

|<span data-ttu-id="84bdf-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="84bdf-115">**Attribute**</span></span>|<span data-ttu-id="84bdf-116">**型**</span><span class="sxs-lookup"><span data-stu-id="84bdf-116">**Type**</span></span>|<span data-ttu-id="84bdf-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="84bdf-117">**Required**</span></span>|<span data-ttu-id="84bdf-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="84bdf-118">**Description**</span></span>|<span data-ttu-id="84bdf-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="84bdf-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="84bdf-120">IX</span><span class="sxs-lookup"><span data-stu-id="84bdf-120">IX</span></span>  <br/> |<span data-ttu-id="84bdf-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="84bdf-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="84bdf-122">必須</span><span class="sxs-lookup"><span data-stu-id="84bdf-122">required</span></span>  <br/> ||<span data-ttu-id="84bdf-123">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="84bdf-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

