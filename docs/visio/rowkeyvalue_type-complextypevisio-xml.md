---
title: RowKeyValue_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: 512675538aa17415fa44684613dcd635fe23857f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387686"
---
# <a name="rowkeyvaluetype-complextype-visio-xml"></a><span data-ttu-id="27c7f-102">RowKeyValue_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="27c7f-102">RowKeyValue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="27c7f-103">型情報</span><span class="sxs-lookup"><span data-stu-id="27c7f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27c7f-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="27c7f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="27c7f-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="27c7f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="27c7f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="27c7f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="27c7f-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="27c7f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="27c7f-108">なし</span><span class="sxs-lookup"><span data-stu-id="27c7f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="27c7f-109">定義</span><span class="sxs-lookup"><span data-stu-id="27c7f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="27c7f-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="27c7f-110">Elements and attributes</span></span>

<span data-ttu-id="27c7f-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="27c7f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="27c7f-112">子要素</span><span class="sxs-lookup"><span data-stu-id="27c7f-112">Child elements</span></span>

<span data-ttu-id="27c7f-113">なし。</span><span class="sxs-lookup"><span data-stu-id="27c7f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27c7f-114">属性</span><span class="sxs-lookup"><span data-stu-id="27c7f-114">Attributes</span></span>

|<span data-ttu-id="27c7f-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="27c7f-115">**Attribute**</span></span>|<span data-ttu-id="27c7f-116">**型**</span><span class="sxs-lookup"><span data-stu-id="27c7f-116">**Type**</span></span>|<span data-ttu-id="27c7f-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="27c7f-117">**Required**</span></span>|<span data-ttu-id="27c7f-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="27c7f-118">**Description**</span></span>|<span data-ttu-id="27c7f-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="27c7f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="27c7f-120">RowID</span><span class="sxs-lookup"><span data-stu-id="27c7f-120">RowID</span></span>  <br/> |<span data-ttu-id="27c7f-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="27c7f-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="27c7f-122">必須</span><span class="sxs-lookup"><span data-stu-id="27c7f-122">required</span></span>  <br/> ||<span data-ttu-id="27c7f-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27c7f-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="27c7f-124">値</span><span class="sxs-lookup"><span data-stu-id="27c7f-124">Value</span></span>  <br/> |<span data-ttu-id="27c7f-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="27c7f-125">xsd:string</span></span>  <br/> |<span data-ttu-id="27c7f-126">必須</span><span class="sxs-lookup"><span data-stu-id="27c7f-126">required</span></span>  <br/> ||<span data-ttu-id="27c7f-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27c7f-127">Values of the xsd:string type.</span></span>  <br/> |
   

