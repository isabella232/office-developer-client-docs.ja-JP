---
title: DataRecordSets_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: 1705d0ea92e278008c33321f135409373b7317fd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388561"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="a86ed-102">DataRecordSets_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a86ed-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a86ed-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a86ed-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a86ed-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a86ed-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a86ed-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a86ed-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a86ed-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a86ed-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a86ed-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a86ed-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a86ed-108">なし</span><span class="sxs-lookup"><span data-stu-id="a86ed-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a86ed-109">定義</span><span class="sxs-lookup"><span data-stu-id="a86ed-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a86ed-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a86ed-110">Elements and attributes</span></span>

<span data-ttu-id="a86ed-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a86ed-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a86ed-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a86ed-112">Child elements</span></span>

|<span data-ttu-id="a86ed-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="a86ed-113">**Element**</span></span>|<span data-ttu-id="a86ed-114">**型**</span><span class="sxs-lookup"><span data-stu-id="a86ed-114">**Type**</span></span>|<span data-ttu-id="a86ed-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="a86ed-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a86ed-116">データ レコード セット</span><span class="sxs-lookup"><span data-stu-id="a86ed-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86ed-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="a86ed-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a86ed-118">属性</span><span class="sxs-lookup"><span data-stu-id="a86ed-118">Attributes</span></span>

|<span data-ttu-id="a86ed-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="a86ed-119">**Attribute**</span></span>|<span data-ttu-id="a86ed-120">**型**</span><span class="sxs-lookup"><span data-stu-id="a86ed-120">**Type**</span></span>|<span data-ttu-id="a86ed-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="a86ed-121">**Required**</span></span>|<span data-ttu-id="a86ed-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="a86ed-122">**Description**</span></span>|<span data-ttu-id="a86ed-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="a86ed-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a86ed-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="a86ed-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="a86ed-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a86ed-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a86ed-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="a86ed-126">optional</span></span>  <br/> ||<span data-ttu-id="a86ed-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a86ed-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a86ed-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="a86ed-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="a86ed-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a86ed-129">xsd:string</span></span>  <br/> |<span data-ttu-id="a86ed-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="a86ed-130">optional</span></span>  <br/> ||<span data-ttu-id="a86ed-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a86ed-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a86ed-132">NextID</span><span class="sxs-lookup"><span data-stu-id="a86ed-132">NextID</span></span>  <br/> |<span data-ttu-id="a86ed-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a86ed-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a86ed-134">必須</span><span class="sxs-lookup"><span data-stu-id="a86ed-134">required</span></span>  <br/> ||<span data-ttu-id="a86ed-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a86ed-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

