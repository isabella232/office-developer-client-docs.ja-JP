---
title: RowKeyValue_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: dcd4c972aac1e86fa7a66766a756ebef2cca7c02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806302"
---
# <a name="rowkeyvaluetype-complextype-visio-xml"></a><span data-ttu-id="6ce64-102">RowKeyValue_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="6ce64-102">RowKeyValue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6ce64-103">型情報</span><span class="sxs-lookup"><span data-stu-id="6ce64-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ce64-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="6ce64-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6ce64-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6ce64-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6ce64-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6ce64-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6ce64-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="6ce64-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6ce64-108">なし</span><span class="sxs-lookup"><span data-stu-id="6ce64-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6ce64-109">定義</span><span class="sxs-lookup"><span data-stu-id="6ce64-109">Definition</span></span>

```XML
      <xs:complexType name="RowKeyValue_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Value"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6ce64-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6ce64-110">Elements and attributes</span></span>

<span data-ttu-id="6ce64-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ce64-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6ce64-112">子要素</span><span class="sxs-lookup"><span data-stu-id="6ce64-112">Child elements</span></span>

<span data-ttu-id="6ce64-113">なし。</span><span class="sxs-lookup"><span data-stu-id="6ce64-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ce64-114">属性</span><span class="sxs-lookup"><span data-stu-id="6ce64-114">Attributes</span></span>

|<span data-ttu-id="6ce64-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="6ce64-115">**Attribute**</span></span>|<span data-ttu-id="6ce64-116">**型**</span><span class="sxs-lookup"><span data-stu-id="6ce64-116">**Type**</span></span>|<span data-ttu-id="6ce64-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="6ce64-117">**Required**</span></span>|<span data-ttu-id="6ce64-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="6ce64-118">**Description**</span></span>|<span data-ttu-id="6ce64-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="6ce64-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6ce64-120">RowID</span><span class="sxs-lookup"><span data-stu-id="6ce64-120">RowID</span></span>  <br/> |<span data-ttu-id="6ce64-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6ce64-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6ce64-122">必須</span><span class="sxs-lookup"><span data-stu-id="6ce64-122">required</span></span>  <br/> ||<span data-ttu-id="6ce64-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6ce64-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6ce64-124">値</span><span class="sxs-lookup"><span data-stu-id="6ce64-124">Value</span></span>  <br/> |<span data-ttu-id="6ce64-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6ce64-125">xsd:string</span></span>  <br/> |<span data-ttu-id="6ce64-126">必須</span><span class="sxs-lookup"><span data-stu-id="6ce64-126">required</span></span>  <br/> ||<span data-ttu-id="6ce64-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6ce64-127">Values of the xsd:string type.</span></span>  <br/> |
   

