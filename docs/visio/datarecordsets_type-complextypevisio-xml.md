---
title: DataRecordSets_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: 1705d0ea92e278008c33321f135409373b7317fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360348"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="7e41e-102">DataRecordSets_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="7e41e-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7e41e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="7e41e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e41e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7e41e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7e41e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="7e41e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7e41e-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="7e41e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7e41e-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="7e41e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7e41e-108">なし</span><span class="sxs-lookup"><span data-stu-id="7e41e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7e41e-109">定義</span><span class="sxs-lookup"><span data-stu-id="7e41e-109">Definition</span></span>

```XML
          <xs:complexType name="DataRecordSets_Type">
          
          <xs:sequence>
    <xs:element name="DataRecordSet"  type="DataRecordSet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="NextID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ActiveRecordsetID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DataWindowOrder"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7e41e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="7e41e-110">Elements and attributes</span></span>

<span data-ttu-id="7e41e-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e41e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7e41e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="7e41e-112">Child elements</span></span>

|<span data-ttu-id="7e41e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7e41e-113">**Element**</span></span>|<span data-ttu-id="7e41e-114">**型**</span><span class="sxs-lookup"><span data-stu-id="7e41e-114">**Type**</span></span>|<span data-ttu-id="7e41e-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="7e41e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7e41e-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="7e41e-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7e41e-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="7e41e-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7e41e-118">属性</span><span class="sxs-lookup"><span data-stu-id="7e41e-118">Attributes</span></span>

|<span data-ttu-id="7e41e-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="7e41e-119">**Attribute**</span></span>|<span data-ttu-id="7e41e-120">**型**</span><span class="sxs-lookup"><span data-stu-id="7e41e-120">**Type**</span></span>|<span data-ttu-id="7e41e-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="7e41e-121">**Required**</span></span>|<span data-ttu-id="7e41e-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="7e41e-122">**Description**</span></span>|<span data-ttu-id="7e41e-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="7e41e-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7e41e-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="7e41e-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="7e41e-125">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="7e41e-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7e41e-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="7e41e-126">optional</span></span>  <br/> ||<span data-ttu-id="7e41e-127">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="7e41e-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7e41e-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="7e41e-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="7e41e-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="7e41e-129">xsd:string</span></span>  <br/> |<span data-ttu-id="7e41e-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="7e41e-130">optional</span></span>  <br/> ||<span data-ttu-id="7e41e-131">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="7e41e-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7e41e-132">NextID</span><span class="sxs-lookup"><span data-stu-id="7e41e-132">NextID</span></span>  <br/> |<span data-ttu-id="7e41e-133">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="7e41e-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7e41e-134">必須</span><span class="sxs-lookup"><span data-stu-id="7e41e-134">required</span></span>  <br/> ||<span data-ttu-id="7e41e-135">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="7e41e-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

