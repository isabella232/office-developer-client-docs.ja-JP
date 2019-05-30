---
title: Trigger_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: 53a9efabe698e6b9c98c0471b97551c8ea2406da
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541898"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="f8d5a-102">Trigger_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f8d5a-102">Trigger_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f8d5a-103">型情報</span><span class="sxs-lookup"><span data-stu-id="f8d5a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8d5a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f8d5a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f8d5a-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f8d5a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f8d5a-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="f8d5a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f8d5a-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="f8d5a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f8d5a-108">None</span><span class="sxs-lookup"><span data-stu-id="f8d5a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f8d5a-109">定義</span><span class="sxs-lookup"><span data-stu-id="f8d5a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f8d5a-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f8d5a-110">Elements and attributes</span></span>

<span data-ttu-id="f8d5a-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8d5a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f8d5a-112">子要素</span><span class="sxs-lookup"><span data-stu-id="f8d5a-112">Child elements</span></span>

|<span data-ttu-id="f8d5a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f8d5a-113">**Element**</span></span>|<span data-ttu-id="f8d5a-114">**型**</span><span class="sxs-lookup"><span data-stu-id="f8d5a-114">**Type**</span></span>|<span data-ttu-id="f8d5a-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="f8d5a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f8d5a-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="f8d5a-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f8d5a-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="f8d5a-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f8d5a-118">属性</span><span class="sxs-lookup"><span data-stu-id="f8d5a-118">Attributes</span></span>

|<span data-ttu-id="f8d5a-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="f8d5a-119">**Attribute**</span></span>|<span data-ttu-id="f8d5a-120">**型**</span><span class="sxs-lookup"><span data-stu-id="f8d5a-120">**Type**</span></span>|<span data-ttu-id="f8d5a-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="f8d5a-121">**Required**</span></span>|<span data-ttu-id="f8d5a-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="f8d5a-122">**Description**</span></span>|<span data-ttu-id="f8d5a-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="f8d5a-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f8d5a-124">N</span><span class="sxs-lookup"><span data-stu-id="f8d5a-124">N</span></span>  <br/> |<span data-ttu-id="f8d5a-125">xsd: string</span><span class="sxs-lookup"><span data-stu-id="f8d5a-125">xsd:string</span></span>  <br/> |<span data-ttu-id="f8d5a-126">必須</span><span class="sxs-lookup"><span data-stu-id="f8d5a-126">required</span></span>  <br/> ||<span data-ttu-id="f8d5a-127">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="f8d5a-127">Values of the xsd:string type.</span></span>  <br/> |
   

