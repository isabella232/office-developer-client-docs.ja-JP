---
title: IssueTarget_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: 38c73e54ff75e94468cfb95258f1fde510d8019a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542143"
---
# <a name="issuetarget_type-complextype-visio-xml"></a><span data-ttu-id="25fb5-102">IssueTarget_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="25fb5-102">IssueTarget_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="25fb5-103">型情報</span><span class="sxs-lookup"><span data-stu-id="25fb5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25fb5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="25fb5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="25fb5-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="25fb5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="25fb5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="25fb5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="25fb5-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="25fb5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="25fb5-108">なし</span><span class="sxs-lookup"><span data-stu-id="25fb5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="25fb5-109">定義</span><span class="sxs-lookup"><span data-stu-id="25fb5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="25fb5-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="25fb5-110">Elements and attributes</span></span>

<span data-ttu-id="25fb5-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="25fb5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="25fb5-112">子要素</span><span class="sxs-lookup"><span data-stu-id="25fb5-112">Child elements</span></span>

<span data-ttu-id="25fb5-113">なし。</span><span class="sxs-lookup"><span data-stu-id="25fb5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25fb5-114">属性</span><span class="sxs-lookup"><span data-stu-id="25fb5-114">Attributes</span></span>

|<span data-ttu-id="25fb5-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="25fb5-115">**Attribute**</span></span>|<span data-ttu-id="25fb5-116">**型**</span><span class="sxs-lookup"><span data-stu-id="25fb5-116">**Type**</span></span>|<span data-ttu-id="25fb5-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="25fb5-117">**Required**</span></span>|<span data-ttu-id="25fb5-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="25fb5-118">**Description**</span></span>|<span data-ttu-id="25fb5-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="25fb5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="25fb5-120">PageID</span><span class="sxs-lookup"><span data-stu-id="25fb5-120">PageID</span></span>  <br/> |<span data-ttu-id="25fb5-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="25fb5-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="25fb5-122">必須</span><span class="sxs-lookup"><span data-stu-id="25fb5-122">required</span></span>  <br/> ||<span data-ttu-id="25fb5-123">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="25fb5-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="25fb5-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="25fb5-124">ShapeID</span></span>  <br/> |<span data-ttu-id="25fb5-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="25fb5-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="25fb5-126">必須</span><span class="sxs-lookup"><span data-stu-id="25fb5-126">required</span></span>  <br/> ||<span data-ttu-id="25fb5-127">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="25fb5-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

