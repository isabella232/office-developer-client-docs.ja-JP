---
title: PageSheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 45e3dec8dc97fd3467195102a42227b844f07a98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334651"
---
# <a name="pagesheettype-complextype-visio-xml"></a><span data-ttu-id="f15f6-102">PageSheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f15f6-102">PageSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f15f6-103">型情報</span><span class="sxs-lookup"><span data-stu-id="f15f6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f15f6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f15f6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f15f6-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f15f6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f15f6-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="f15f6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f15f6-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="f15f6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f15f6-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="f15f6-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f15f6-109">定義</span><span class="sxs-lookup"><span data-stu-id="f15f6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f15f6-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f15f6-110">Elements and attributes</span></span>

<span data-ttu-id="f15f6-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f15f6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f15f6-112">子要素</span><span class="sxs-lookup"><span data-stu-id="f15f6-112">Child elements</span></span>

<span data-ttu-id="f15f6-113">なし。</span><span class="sxs-lookup"><span data-stu-id="f15f6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f15f6-114">属性</span><span class="sxs-lookup"><span data-stu-id="f15f6-114">Attributes</span></span>

|<span data-ttu-id="f15f6-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="f15f6-115">**Attribute**</span></span>|<span data-ttu-id="f15f6-116">**型**</span><span class="sxs-lookup"><span data-stu-id="f15f6-116">**Type**</span></span>|<span data-ttu-id="f15f6-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="f15f6-117">**Required**</span></span>|<span data-ttu-id="f15f6-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="f15f6-118">**Description**</span></span>|<span data-ttu-id="f15f6-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="f15f6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f15f6-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="f15f6-120">UniqueID</span></span>  <br/> |<span data-ttu-id="f15f6-121">xsd: string</span><span class="sxs-lookup"><span data-stu-id="f15f6-121">xsd:string</span></span>  <br/> |<span data-ttu-id="f15f6-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="f15f6-122">optional</span></span>  <br/> ||<span data-ttu-id="f15f6-123">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="f15f6-123">Values of the xsd:string type.</span></span>  <br/> |
   

