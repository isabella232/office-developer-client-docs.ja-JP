---
title: Trigger_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: e34ef122a6f0a08168f838fdaeb130d68349ecb8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396331"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="764a0-102">Trigger_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="764a0-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="764a0-103">型情報</span><span class="sxs-lookup"><span data-stu-id="764a0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="764a0-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="764a0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="764a0-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="764a0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="764a0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="764a0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="764a0-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="764a0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="764a0-108">なし</span><span class="sxs-lookup"><span data-stu-id="764a0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="764a0-109">定義</span><span class="sxs-lookup"><span data-stu-id="764a0-109">Definition</span></span>

```XML
          <xs:complexType name="Trigger_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="764a0-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="764a0-110">Elements and attributes</span></span>

<span data-ttu-id="764a0-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="764a0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="764a0-112">子要素</span><span class="sxs-lookup"><span data-stu-id="764a0-112">Child elements</span></span>

|<span data-ttu-id="764a0-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="764a0-113">**Element**</span></span>|<span data-ttu-id="764a0-114">**型**</span><span class="sxs-lookup"><span data-stu-id="764a0-114">**Type**</span></span>|<span data-ttu-id="764a0-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="764a0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="764a0-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="764a0-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="764a0-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="764a0-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="764a0-118">属性</span><span class="sxs-lookup"><span data-stu-id="764a0-118">Attributes</span></span>

|<span data-ttu-id="764a0-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="764a0-119">**Attribute**</span></span>|<span data-ttu-id="764a0-120">**型**</span><span class="sxs-lookup"><span data-stu-id="764a0-120">**Type**</span></span>|<span data-ttu-id="764a0-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="764a0-121">**Required**</span></span>|<span data-ttu-id="764a0-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="764a0-122">**Description**</span></span>|<span data-ttu-id="764a0-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="764a0-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="764a0-124">N</span><span class="sxs-lookup"><span data-stu-id="764a0-124">N</span></span>  <br/> |<span data-ttu-id="764a0-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="764a0-125">xsd:string</span></span>  <br/> |<span data-ttu-id="764a0-126">必須</span><span class="sxs-lookup"><span data-stu-id="764a0-126">required</span></span>  <br/> ||<span data-ttu-id="764a0-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="764a0-127">Values of the xsd:string type.</span></span>  <br/> |
   

