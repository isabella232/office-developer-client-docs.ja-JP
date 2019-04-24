---
title: HeaderMargin_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 9bb32471f1384c89e02e9ffdbcceebfc48d2b22e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330052"
---
# <a name="headermargintype-complextype-visio-xml"></a><span data-ttu-id="ec595-102">HeaderMargin_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ec595-102">HeaderMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ec595-103">型情報</span><span class="sxs-lookup"><span data-stu-id="ec595-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec595-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ec595-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ec595-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ec595-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ec595-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="ec595-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ec595-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="ec595-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ec595-108">xsd: double</span><span class="sxs-lookup"><span data-stu-id="ec595-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ec595-109">定義</span><span class="sxs-lookup"><span data-stu-id="ec595-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ec595-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ec595-110">Elements and attributes</span></span>

<span data-ttu-id="ec595-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec595-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ec595-112">子要素</span><span class="sxs-lookup"><span data-stu-id="ec595-112">Child elements</span></span>

<span data-ttu-id="ec595-113">なし。</span><span class="sxs-lookup"><span data-stu-id="ec595-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec595-114">属性</span><span class="sxs-lookup"><span data-stu-id="ec595-114">Attributes</span></span>

|<span data-ttu-id="ec595-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="ec595-115">**Attribute**</span></span>|<span data-ttu-id="ec595-116">**型**</span><span class="sxs-lookup"><span data-stu-id="ec595-116">**Type**</span></span>|<span data-ttu-id="ec595-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="ec595-117">**Required**</span></span>|<span data-ttu-id="ec595-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="ec595-118">**Description**</span></span>|<span data-ttu-id="ec595-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="ec595-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ec595-120">単位</span><span class="sxs-lookup"><span data-stu-id="ec595-120">Unit</span></span>  <br/> |<span data-ttu-id="ec595-121">xsd: string</span><span class="sxs-lookup"><span data-stu-id="ec595-121">xsd:string</span></span>  <br/> |<span data-ttu-id="ec595-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="ec595-122">optional</span></span>  <br/> ||<span data-ttu-id="ec595-123">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="ec595-123">Values of the xsd:string type.</span></span>  <br/> |
   

