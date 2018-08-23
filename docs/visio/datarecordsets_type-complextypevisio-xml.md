---
title: DataRecordSets_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: b646e7a0d4e1f49aa71b162aecdd901813b01f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805176"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="0db37-102">DataRecordSets_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="0db37-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0db37-103">型情報</span><span class="sxs-lookup"><span data-stu-id="0db37-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0db37-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="0db37-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0db37-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0db37-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0db37-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0db37-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0db37-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="0db37-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0db37-108">なし</span><span class="sxs-lookup"><span data-stu-id="0db37-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0db37-109">定義</span><span class="sxs-lookup"><span data-stu-id="0db37-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0db37-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0db37-110">Elements and attributes</span></span>

<span data-ttu-id="0db37-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db37-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0db37-112">子要素</span><span class="sxs-lookup"><span data-stu-id="0db37-112">Child elements</span></span>

|<span data-ttu-id="0db37-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="0db37-113">**Element**</span></span>|<span data-ttu-id="0db37-114">**型**</span><span class="sxs-lookup"><span data-stu-id="0db37-114">**Type**</span></span>|<span data-ttu-id="0db37-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="0db37-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0db37-116">データ レコード セット</span><span class="sxs-lookup"><span data-stu-id="0db37-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0db37-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="0db37-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0db37-118">属性</span><span class="sxs-lookup"><span data-stu-id="0db37-118">Attributes</span></span>

|<span data-ttu-id="0db37-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="0db37-119">**Attribute**</span></span>|<span data-ttu-id="0db37-120">**型**</span><span class="sxs-lookup"><span data-stu-id="0db37-120">**Type**</span></span>|<span data-ttu-id="0db37-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="0db37-121">**Required**</span></span>|<span data-ttu-id="0db37-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="0db37-122">**Description**</span></span>|<span data-ttu-id="0db37-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="0db37-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0db37-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="0db37-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="0db37-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0db37-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0db37-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="0db37-126">optional</span></span>  <br/> ||<span data-ttu-id="0db37-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0db37-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0db37-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="0db37-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="0db37-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0db37-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0db37-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="0db37-130">optional</span></span>  <br/> ||<span data-ttu-id="0db37-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0db37-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0db37-132">NextID</span><span class="sxs-lookup"><span data-stu-id="0db37-132">NextID</span></span>  <br/> |<span data-ttu-id="0db37-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0db37-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0db37-134">必須</span><span class="sxs-lookup"><span data-stu-id="0db37-134">required</span></span>  <br/> ||<span data-ttu-id="0db37-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0db37-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

