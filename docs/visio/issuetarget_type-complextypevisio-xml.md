---
title: IssueTarget_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: d7b8309bb6dac9648d379c89687dc89165f44edf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314925"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="63fe9-102">IssueTarget_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="63fe9-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="63fe9-103">型情報</span><span class="sxs-lookup"><span data-stu-id="63fe9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63fe9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="63fe9-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="63fe9-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="63fe9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="63fe9-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="63fe9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="63fe9-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="63fe9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="63fe9-108">なし</span><span class="sxs-lookup"><span data-stu-id="63fe9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="63fe9-109">定義</span><span class="sxs-lookup"><span data-stu-id="63fe9-109">Definition</span></span>

```XML
      <xs:complexType name="IssueTarget_Type">
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="63fe9-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="63fe9-110">Elements and attributes</span></span>

<span data-ttu-id="63fe9-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="63fe9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="63fe9-112">子要素</span><span class="sxs-lookup"><span data-stu-id="63fe9-112">Child elements</span></span>

<span data-ttu-id="63fe9-113">なし。</span><span class="sxs-lookup"><span data-stu-id="63fe9-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63fe9-114">属性</span><span class="sxs-lookup"><span data-stu-id="63fe9-114">Attributes</span></span>

|<span data-ttu-id="63fe9-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="63fe9-115">**Attribute**</span></span>|<span data-ttu-id="63fe9-116">**型**</span><span class="sxs-lookup"><span data-stu-id="63fe9-116">**Type**</span></span>|<span data-ttu-id="63fe9-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="63fe9-117">**Required**</span></span>|<span data-ttu-id="63fe9-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="63fe9-118">**Description**</span></span>|<span data-ttu-id="63fe9-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="63fe9-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="63fe9-120">PageID</span><span class="sxs-lookup"><span data-stu-id="63fe9-120">PageID</span></span>  <br/> |<span data-ttu-id="63fe9-121">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="63fe9-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="63fe9-122">必須</span><span class="sxs-lookup"><span data-stu-id="63fe9-122">required</span></span>  <br/> ||<span data-ttu-id="63fe9-123">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="63fe9-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="63fe9-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="63fe9-124">ShapeID</span></span>  <br/> |<span data-ttu-id="63fe9-125">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="63fe9-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="63fe9-126">必須</span><span class="sxs-lookup"><span data-stu-id="63fe9-126">required</span></span>  <br/> ||<span data-ttu-id="63fe9-127">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="63fe9-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

