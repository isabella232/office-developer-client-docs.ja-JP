---
title: DataRecordSets_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: 77a6588a1b5fba05d14e91a39ba570d21142f953
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539159"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="10eb6-102">DataRecordSets_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="10eb6-102">DataRecordSets_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="10eb6-103">型情報</span><span class="sxs-lookup"><span data-stu-id="10eb6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10eb6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="10eb6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="10eb6-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="10eb6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="10eb6-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="10eb6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="10eb6-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="10eb6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="10eb6-108">None</span><span class="sxs-lookup"><span data-stu-id="10eb6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="10eb6-109">定義</span><span class="sxs-lookup"><span data-stu-id="10eb6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="10eb6-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="10eb6-110">Elements and attributes</span></span>

<span data-ttu-id="10eb6-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="10eb6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="10eb6-112">子要素</span><span class="sxs-lookup"><span data-stu-id="10eb6-112">Child elements</span></span>

|<span data-ttu-id="10eb6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="10eb6-113">**Element**</span></span>|<span data-ttu-id="10eb6-114">**型**</span><span class="sxs-lookup"><span data-stu-id="10eb6-114">**Type**</span></span>|<span data-ttu-id="10eb6-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="10eb6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="10eb6-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="10eb6-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="10eb6-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="10eb6-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="10eb6-118">属性</span><span class="sxs-lookup"><span data-stu-id="10eb6-118">Attributes</span></span>

|<span data-ttu-id="10eb6-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="10eb6-119">**Attribute**</span></span>|<span data-ttu-id="10eb6-120">**型**</span><span class="sxs-lookup"><span data-stu-id="10eb6-120">**Type**</span></span>|<span data-ttu-id="10eb6-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="10eb6-121">**Required**</span></span>|<span data-ttu-id="10eb6-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="10eb6-122">**Description**</span></span>|<span data-ttu-id="10eb6-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="10eb6-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="10eb6-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="10eb6-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="10eb6-125">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="10eb6-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="10eb6-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="10eb6-126">optional</span></span>  <br/> ||<span data-ttu-id="10eb6-127">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="10eb6-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="10eb6-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="10eb6-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="10eb6-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="10eb6-129">xsd:string</span></span>  <br/> |<span data-ttu-id="10eb6-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="10eb6-130">optional</span></span>  <br/> ||<span data-ttu-id="10eb6-131">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="10eb6-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="10eb6-132">NextID</span><span class="sxs-lookup"><span data-stu-id="10eb6-132">NextID</span></span>  <br/> |<span data-ttu-id="10eb6-133">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="10eb6-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="10eb6-134">必須</span><span class="sxs-lookup"><span data-stu-id="10eb6-134">required</span></span>  <br/> ||<span data-ttu-id="10eb6-135">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="10eb6-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

