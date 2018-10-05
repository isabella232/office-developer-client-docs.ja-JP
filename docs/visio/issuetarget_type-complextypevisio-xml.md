---
title: IssueTarget_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: d7b8309bb6dac9648d379c89687dc89165f44edf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393769"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="c522d-102">IssueTarget_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="c522d-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c522d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="c522d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c522d-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="c522d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c522d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c522d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c522d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c522d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c522d-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="c522d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c522d-108">なし</span><span class="sxs-lookup"><span data-stu-id="c522d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c522d-109">定義</span><span class="sxs-lookup"><span data-stu-id="c522d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c522d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c522d-110">Elements and attributes</span></span>

<span data-ttu-id="c522d-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c522d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c522d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="c522d-112">Child elements</span></span>

<span data-ttu-id="c522d-113">なし。</span><span class="sxs-lookup"><span data-stu-id="c522d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c522d-114">属性</span><span class="sxs-lookup"><span data-stu-id="c522d-114">Attributes</span></span>

|<span data-ttu-id="c522d-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="c522d-115">**Attribute**</span></span>|<span data-ttu-id="c522d-116">**型**</span><span class="sxs-lookup"><span data-stu-id="c522d-116">**Type**</span></span>|<span data-ttu-id="c522d-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="c522d-117">**Required**</span></span>|<span data-ttu-id="c522d-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="c522d-118">**Description**</span></span>|<span data-ttu-id="c522d-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="c522d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c522d-120">PageID</span><span class="sxs-lookup"><span data-stu-id="c522d-120">PageID</span></span>  <br/> |<span data-ttu-id="c522d-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c522d-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c522d-122">必須</span><span class="sxs-lookup"><span data-stu-id="c522d-122">required</span></span>  <br/> ||<span data-ttu-id="c522d-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c522d-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c522d-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="c522d-124">ShapeID</span></span>  <br/> |<span data-ttu-id="c522d-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c522d-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c522d-126">必須</span><span class="sxs-lookup"><span data-stu-id="c522d-126">required</span></span>  <br/> ||<span data-ttu-id="c522d-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c522d-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

