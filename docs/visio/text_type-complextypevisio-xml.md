---
title: Text_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc6b37c3-7f55-fe18-a9b7-884ea87b3f46
ms.openlocfilehash: cfacc84cb8b38acfbda3c37c669dd9714d899098
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541380"
---
# <a name="texttype-complextype-visio-xml"></a><span data-ttu-id="64e47-102">Text_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="64e47-102">Text_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="64e47-103">型情報</span><span class="sxs-lookup"><span data-stu-id="64e47-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64e47-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="64e47-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="64e47-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="64e47-105">**Schema file**</span></span> <br/> |<span data-ttu-id="64e47-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="64e47-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="64e47-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="64e47-107">**Extension base**</span></span> <br/> |<span data-ttu-id="64e47-108">None</span><span class="sxs-lookup"><span data-stu-id="64e47-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="64e47-109">定義</span><span class="sxs-lookup"><span data-stu-id="64e47-109">Definition</span></span>

```XML
          <xs:complexType name="Text_Type">
          
          <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="cp"  type="cp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="pp"  type="pp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="tp"  type="tp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="fld"  type="fld_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:choice>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="64e47-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="64e47-110">Elements and attributes</span></span>

<span data-ttu-id="64e47-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="64e47-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="64e47-112">子要素</span><span class="sxs-lookup"><span data-stu-id="64e47-112">Child elements</span></span>

|<span data-ttu-id="64e47-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="64e47-113">**Element**</span></span>|<span data-ttu-id="64e47-114">**型**</span><span class="sxs-lookup"><span data-stu-id="64e47-114">**Type**</span></span>|<span data-ttu-id="64e47-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="64e47-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="64e47-116">cp</span><span class="sxs-lookup"><span data-stu-id="64e47-116">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64e47-117">cp_Type</span><span class="sxs-lookup"><span data-stu-id="64e47-117">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="64e47-118">fld</span><span class="sxs-lookup"><span data-stu-id="64e47-118">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64e47-119">fld_Type</span><span class="sxs-lookup"><span data-stu-id="64e47-119">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="64e47-120">pptp</span><span class="sxs-lookup"><span data-stu-id="64e47-120">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64e47-121">pp_Type</span><span class="sxs-lookup"><span data-stu-id="64e47-121">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="64e47-122">tp</span><span class="sxs-lookup"><span data-stu-id="64e47-122">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64e47-123">tp_Type</span><span class="sxs-lookup"><span data-stu-id="64e47-123">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="64e47-124">属性</span><span class="sxs-lookup"><span data-stu-id="64e47-124">Attributes</span></span>

<span data-ttu-id="64e47-125">なし。</span><span class="sxs-lookup"><span data-stu-id="64e47-125">None.</span></span>
  

