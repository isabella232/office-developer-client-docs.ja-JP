---
title: Trigger_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: e34ef122a6f0a08168f838fdaeb130d68349ecb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280858"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="b3413-102">Trigger_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b3413-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b3413-103">型情報</span><span class="sxs-lookup"><span data-stu-id="b3413-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3413-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b3413-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b3413-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b3413-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b3413-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="b3413-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b3413-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="b3413-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b3413-108">なし</span><span class="sxs-lookup"><span data-stu-id="b3413-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b3413-109">定義</span><span class="sxs-lookup"><span data-stu-id="b3413-109">Definition</span></span>

```XML
          <xs:complexType name="Trigger_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b3413-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b3413-110">Elements and attributes</span></span>

<span data-ttu-id="b3413-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3413-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b3413-112">子要素</span><span class="sxs-lookup"><span data-stu-id="b3413-112">Child elements</span></span>

|<span data-ttu-id="b3413-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3413-113">**Element**</span></span>|<span data-ttu-id="b3413-114">**型**</span><span class="sxs-lookup"><span data-stu-id="b3413-114">**Type**</span></span>|<span data-ttu-id="b3413-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="b3413-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b3413-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="b3413-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b3413-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="b3413-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b3413-118">属性</span><span class="sxs-lookup"><span data-stu-id="b3413-118">Attributes</span></span>

|<span data-ttu-id="b3413-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="b3413-119">**Attribute**</span></span>|<span data-ttu-id="b3413-120">**型**</span><span class="sxs-lookup"><span data-stu-id="b3413-120">**Type**</span></span>|<span data-ttu-id="b3413-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="b3413-121">**Required**</span></span>|<span data-ttu-id="b3413-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="b3413-122">**Description**</span></span>|<span data-ttu-id="b3413-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="b3413-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b3413-124">N</span><span class="sxs-lookup"><span data-stu-id="b3413-124">N</span></span>  <br/> |<span data-ttu-id="b3413-125">xsd: string</span><span class="sxs-lookup"><span data-stu-id="b3413-125">xsd:string</span></span>  <br/> |<span data-ttu-id="b3413-126">必須</span><span class="sxs-lookup"><span data-stu-id="b3413-126">required</span></span>  <br/> ||<span data-ttu-id="b3413-127">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="b3413-127">Values of the xsd:string type.</span></span>  <br/> |
   

