---
title: cp_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e69b0db-f705-61f0-e6ab-811b2acc358e
ms.openlocfilehash: 9419882f8f61293f0160b8e645f0f76bb443d46f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282916"
---
# <a name="cptype-complextype-visio-xml"></a><span data-ttu-id="e6183-102">cp_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="e6183-102">cp_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e6183-103">型情報</span><span class="sxs-lookup"><span data-stu-id="e6183-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6183-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e6183-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e6183-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e6183-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e6183-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="e6183-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e6183-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="e6183-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e6183-108">なし</span><span class="sxs-lookup"><span data-stu-id="e6183-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e6183-109">定義</span><span class="sxs-lookup"><span data-stu-id="e6183-109">Definition</span></span>

```XML
      <xs:complexType name="cp_Type">
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e6183-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e6183-110">Elements and attributes</span></span>

<span data-ttu-id="e6183-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e6183-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e6183-112">子要素</span><span class="sxs-lookup"><span data-stu-id="e6183-112">Child elements</span></span>

<span data-ttu-id="e6183-113">なし。</span><span class="sxs-lookup"><span data-stu-id="e6183-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6183-114">属性</span><span class="sxs-lookup"><span data-stu-id="e6183-114">Attributes</span></span>

|<span data-ttu-id="e6183-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="e6183-115">**Attribute**</span></span>|<span data-ttu-id="e6183-116">**型**</span><span class="sxs-lookup"><span data-stu-id="e6183-116">**Type**</span></span>|<span data-ttu-id="e6183-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="e6183-117">**Required**</span></span>|<span data-ttu-id="e6183-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="e6183-118">**Description**</span></span>|<span data-ttu-id="e6183-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="e6183-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e6183-120">IX</span><span class="sxs-lookup"><span data-stu-id="e6183-120">IX</span></span>  <br/> |<span data-ttu-id="e6183-121">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="e6183-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e6183-122">必須</span><span class="sxs-lookup"><span data-stu-id="e6183-122">required</span></span>  <br/> ||<span data-ttu-id="e6183-123">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="e6183-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

