---
title: fld_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: 2b1ecb21090658e1d2b042ac0f7e394d929d43c1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390605"
---
# <a name="fldtype-complextype-visio-xml"></a><span data-ttu-id="5bd77-102">fld_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="5bd77-102">fld_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5bd77-103">型情報</span><span class="sxs-lookup"><span data-stu-id="5bd77-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5bd77-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="5bd77-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5bd77-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5bd77-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5bd77-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5bd77-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5bd77-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="5bd77-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5bd77-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5bd77-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5bd77-109">定義</span><span class="sxs-lookup"><span data-stu-id="5bd77-109">Definition</span></span>

```XML
      <xs:complexType name="fld_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5bd77-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5bd77-110">Elements and attributes</span></span>

<span data-ttu-id="5bd77-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5bd77-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5bd77-112">子要素</span><span class="sxs-lookup"><span data-stu-id="5bd77-112">Child elements</span></span>

<span data-ttu-id="5bd77-113">なし。</span><span class="sxs-lookup"><span data-stu-id="5bd77-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5bd77-114">属性</span><span class="sxs-lookup"><span data-stu-id="5bd77-114">Attributes</span></span>

|<span data-ttu-id="5bd77-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="5bd77-115">**Attribute**</span></span>|<span data-ttu-id="5bd77-116">**型**</span><span class="sxs-lookup"><span data-stu-id="5bd77-116">**Type**</span></span>|<span data-ttu-id="5bd77-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="5bd77-117">**Required**</span></span>|<span data-ttu-id="5bd77-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="5bd77-118">**Description**</span></span>|<span data-ttu-id="5bd77-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="5bd77-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5bd77-120">IX</span><span class="sxs-lookup"><span data-stu-id="5bd77-120">IX</span></span>  <br/> |<span data-ttu-id="5bd77-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5bd77-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5bd77-122">必須</span><span class="sxs-lookup"><span data-stu-id="5bd77-122">required</span></span>  <br/> ||<span data-ttu-id="5bd77-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bd77-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

