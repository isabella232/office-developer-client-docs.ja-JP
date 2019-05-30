---
title: PageSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 01112db1465eece9ecf5faf200a1d866ce6e332d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540589"
---
# <a name="pagesheettype-complextype-visio-xml"></a><span data-ttu-id="6969e-102">PageSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6969e-102">PageSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6969e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="6969e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6969e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6969e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6969e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6969e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6969e-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="6969e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6969e-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="6969e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6969e-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="6969e-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6969e-109">定義</span><span class="sxs-lookup"><span data-stu-id="6969e-109">Definition</span></span>

```XML
      <xs:complexType name="PageSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6969e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6969e-110">Elements and attributes</span></span>

<span data-ttu-id="6969e-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6969e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6969e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="6969e-112">Child elements</span></span>

<span data-ttu-id="6969e-113">なし。</span><span class="sxs-lookup"><span data-stu-id="6969e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6969e-114">属性</span><span class="sxs-lookup"><span data-stu-id="6969e-114">Attributes</span></span>

|<span data-ttu-id="6969e-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="6969e-115">**Attribute**</span></span>|<span data-ttu-id="6969e-116">**型**</span><span class="sxs-lookup"><span data-stu-id="6969e-116">**Type**</span></span>|<span data-ttu-id="6969e-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="6969e-117">**Required**</span></span>|<span data-ttu-id="6969e-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="6969e-118">**Description**</span></span>|<span data-ttu-id="6969e-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="6969e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6969e-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="6969e-120">UniqueID</span></span>  <br/> |<span data-ttu-id="6969e-121">xsd: string</span><span class="sxs-lookup"><span data-stu-id="6969e-121">xsd:string</span></span>  <br/> |<span data-ttu-id="6969e-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="6969e-122">optional</span></span>  <br/> ||<span data-ttu-id="6969e-123">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="6969e-123">Values of the xsd:string type.</span></span>  <br/> |
   

