---
title: FooterMargin_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: 69f5ce201bd1859aa716e0967939f0c1e5a5a2c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346047"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="c7d6f-102">FooterMargin_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c7d6f-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c7d6f-103">型情報</span><span class="sxs-lookup"><span data-stu-id="c7d6f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7d6f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c7d6f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c7d6f-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c7d6f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c7d6f-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="c7d6f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c7d6f-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="c7d6f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c7d6f-108">xsd: double</span><span class="sxs-lookup"><span data-stu-id="c7d6f-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c7d6f-109">定義</span><span class="sxs-lookup"><span data-stu-id="c7d6f-109">Definition</span></span>

```XML
      <xs:complexType name="FooterMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c7d6f-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c7d6f-110">Elements and attributes</span></span>

<span data-ttu-id="c7d6f-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7d6f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c7d6f-112">子要素</span><span class="sxs-lookup"><span data-stu-id="c7d6f-112">Child elements</span></span>

<span data-ttu-id="c7d6f-113">なし。</span><span class="sxs-lookup"><span data-stu-id="c7d6f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7d6f-114">属性</span><span class="sxs-lookup"><span data-stu-id="c7d6f-114">Attributes</span></span>

|<span data-ttu-id="c7d6f-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="c7d6f-115">**Attribute**</span></span>|<span data-ttu-id="c7d6f-116">**型**</span><span class="sxs-lookup"><span data-stu-id="c7d6f-116">**Type**</span></span>|<span data-ttu-id="c7d6f-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="c7d6f-117">**Required**</span></span>|<span data-ttu-id="c7d6f-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="c7d6f-118">**Description**</span></span>|<span data-ttu-id="c7d6f-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="c7d6f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c7d6f-120">単位</span><span class="sxs-lookup"><span data-stu-id="c7d6f-120">Unit</span></span>  <br/> |<span data-ttu-id="c7d6f-121">xsd: string</span><span class="sxs-lookup"><span data-stu-id="c7d6f-121">xsd:string</span></span>  <br/> |<span data-ttu-id="c7d6f-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="c7d6f-122">optional</span></span>  <br/> ||<span data-ttu-id="c7d6f-123">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c7d6f-123">Values of the xsd:string type.</span></span>  <br/> |
   

