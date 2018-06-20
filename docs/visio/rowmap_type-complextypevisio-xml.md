---
title: RowMap_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: 18f573a480e3ae057074a219def192f6b1b2829b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806307"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="88c34-102">RowMap_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="88c34-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="88c34-103">型情報</span><span class="sxs-lookup"><span data-stu-id="88c34-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88c34-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="88c34-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="88c34-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="88c34-105">**Schema file**</span></span> <br/> |<span data-ttu-id="88c34-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="88c34-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="88c34-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="88c34-107">**Extension base**</span></span> <br/> |<span data-ttu-id="88c34-108">なし</span><span class="sxs-lookup"><span data-stu-id="88c34-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88c34-109">定義</span><span class="sxs-lookup"><span data-stu-id="88c34-109">Definition</span></span>

```XML
      <xs:complexType name="RowMap_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
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

## <a name="elements-and-attributes"></a><span data-ttu-id="88c34-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="88c34-110">Elements and attributes</span></span>

<span data-ttu-id="88c34-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88c34-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="88c34-112">子要素</span><span class="sxs-lookup"><span data-stu-id="88c34-112">Child elements</span></span>

<span data-ttu-id="88c34-113">なし。</span><span class="sxs-lookup"><span data-stu-id="88c34-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88c34-114">属性</span><span class="sxs-lookup"><span data-stu-id="88c34-114">Attributes</span></span>

|<span data-ttu-id="88c34-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="88c34-115">**Attribute**</span></span>|<span data-ttu-id="88c34-116">**型**</span><span class="sxs-lookup"><span data-stu-id="88c34-116">**Type**</span></span>|<span data-ttu-id="88c34-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="88c34-117">**Required**</span></span>|<span data-ttu-id="88c34-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="88c34-118">**Description**</span></span>|<span data-ttu-id="88c34-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="88c34-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="88c34-120">PageID</span><span class="sxs-lookup"><span data-stu-id="88c34-120">PageID</span></span>  <br/> |<span data-ttu-id="88c34-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88c34-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88c34-122">必須</span><span class="sxs-lookup"><span data-stu-id="88c34-122">required</span></span>  <br/> ||<span data-ttu-id="88c34-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88c34-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88c34-124">RowID</span><span class="sxs-lookup"><span data-stu-id="88c34-124">RowID</span></span>  <br/> |<span data-ttu-id="88c34-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88c34-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88c34-126">必須</span><span class="sxs-lookup"><span data-stu-id="88c34-126">required</span></span>  <br/> ||<span data-ttu-id="88c34-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88c34-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88c34-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="88c34-128">ShapeID</span></span>  <br/> |<span data-ttu-id="88c34-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88c34-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88c34-130">必須</span><span class="sxs-lookup"><span data-stu-id="88c34-130">required</span></span>  <br/> ||<span data-ttu-id="88c34-131">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88c34-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

