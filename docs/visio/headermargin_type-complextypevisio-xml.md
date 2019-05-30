---
title: HeaderMargin_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 2d4a1fb15172d86a7843616679df4177d6f8292b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539090"
---
# <a name="headermargintype-complextype-visio-xml"></a><span data-ttu-id="9701d-102">HeaderMargin_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9701d-102">HeaderMargin_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9701d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="9701d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9701d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9701d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9701d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9701d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9701d-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="9701d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9701d-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="9701d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9701d-108">xsd: double</span><span class="sxs-lookup"><span data-stu-id="9701d-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9701d-109">定義</span><span class="sxs-lookup"><span data-stu-id="9701d-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9701d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9701d-110">Elements and attributes</span></span>

<span data-ttu-id="9701d-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9701d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9701d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="9701d-112">Child elements</span></span>

<span data-ttu-id="9701d-113">なし。</span><span class="sxs-lookup"><span data-stu-id="9701d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9701d-114">属性</span><span class="sxs-lookup"><span data-stu-id="9701d-114">Attributes</span></span>

|<span data-ttu-id="9701d-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="9701d-115">**Attribute**</span></span>|<span data-ttu-id="9701d-116">**型**</span><span class="sxs-lookup"><span data-stu-id="9701d-116">**Type**</span></span>|<span data-ttu-id="9701d-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="9701d-117">**Required**</span></span>|<span data-ttu-id="9701d-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="9701d-118">**Description**</span></span>|<span data-ttu-id="9701d-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="9701d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9701d-120">単位</span><span class="sxs-lookup"><span data-stu-id="9701d-120">Unit</span></span>  <br/> |<span data-ttu-id="9701d-121">xsd: string</span><span class="sxs-lookup"><span data-stu-id="9701d-121">xsd:string</span></span>  <br/> |<span data-ttu-id="9701d-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="9701d-122">optional</span></span>  <br/> ||<span data-ttu-id="9701d-123">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="9701d-123">Values of the xsd:string type.</span></span>  <br/> |
   

