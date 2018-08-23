---
title: ValidationProperties_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: eb1373881b1584b77c6663dd4ec375c50a61efd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806745"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="d7291-102">ValidationProperties_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="d7291-102">ValidationProperties_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d7291-103">型情報</span><span class="sxs-lookup"><span data-stu-id="d7291-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7291-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="d7291-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d7291-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d7291-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d7291-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d7291-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d7291-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="d7291-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d7291-108">なし</span><span class="sxs-lookup"><span data-stu-id="d7291-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d7291-109">定義</span><span class="sxs-lookup"><span data-stu-id="d7291-109">Definition</span></span>

```XML
      <xs:complexType name="ValidationProperties_Type">
    <xs:attribute name="LastValidated"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="ShowIgnored"
  type="xsd:boolean"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d7291-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d7291-110">Elements and attributes</span></span>

<span data-ttu-id="d7291-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7291-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d7291-112">子要素</span><span class="sxs-lookup"><span data-stu-id="d7291-112">Child elements</span></span>

<span data-ttu-id="d7291-113">なし。</span><span class="sxs-lookup"><span data-stu-id="d7291-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7291-114">属性</span><span class="sxs-lookup"><span data-stu-id="d7291-114">Attributes</span></span>

|<span data-ttu-id="d7291-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="d7291-115">**Attribute**</span></span>|<span data-ttu-id="d7291-116">**型**</span><span class="sxs-lookup"><span data-stu-id="d7291-116">**Type**</span></span>|<span data-ttu-id="d7291-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="d7291-117">**Required**</span></span>|<span data-ttu-id="d7291-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="d7291-118">**Description**</span></span>|<span data-ttu-id="d7291-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="d7291-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d7291-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="d7291-120">LastValidated</span></span>  <br/> |<span data-ttu-id="d7291-121">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="d7291-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="d7291-122">必須</span><span class="sxs-lookup"><span data-stu-id="d7291-122">required</span></span>  <br/> ||<span data-ttu-id="d7291-123">Xsd:dateTime の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7291-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="d7291-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="d7291-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="d7291-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="d7291-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d7291-126">必須</span><span class="sxs-lookup"><span data-stu-id="d7291-126">required</span></span>  <br/> ||<span data-ttu-id="d7291-127">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7291-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

