---
title: Text_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc6b37c3-7f55-fe18-a9b7-884ea87b3f46
ms.openlocfilehash: 3309184c47eaf6c6a8cb20d7c6485c21c5ec8c50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806608"
---
# <a name="texttype-complextype-visio-xml"></a><span data-ttu-id="641fa-102">Text_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="641fa-102">Text_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="641fa-103">型情報</span><span class="sxs-lookup"><span data-stu-id="641fa-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="641fa-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="641fa-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="641fa-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="641fa-105">**Schema file**</span></span> <br/> |<span data-ttu-id="641fa-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="641fa-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="641fa-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="641fa-107">**Extension base**</span></span> <br/> |<span data-ttu-id="641fa-108">なし</span><span class="sxs-lookup"><span data-stu-id="641fa-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="641fa-109">定義</span><span class="sxs-lookup"><span data-stu-id="641fa-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="641fa-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="641fa-110">Elements and attributes</span></span>

<span data-ttu-id="641fa-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="641fa-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="641fa-112">子要素</span><span class="sxs-lookup"><span data-stu-id="641fa-112">Child elements</span></span>

|<span data-ttu-id="641fa-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="641fa-113">**Element**</span></span>|<span data-ttu-id="641fa-114">**型**</span><span class="sxs-lookup"><span data-stu-id="641fa-114">**Type**</span></span>|<span data-ttu-id="641fa-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="641fa-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="641fa-116">cp</span><span class="sxs-lookup"><span data-stu-id="641fa-116">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="641fa-117">cp_Type</span><span class="sxs-lookup"><span data-stu-id="641fa-117">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="641fa-118">fld</span><span class="sxs-lookup"><span data-stu-id="641fa-118">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="641fa-119">fld_Type</span><span class="sxs-lookup"><span data-stu-id="641fa-119">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="641fa-120">pp</span><span class="sxs-lookup"><span data-stu-id="641fa-120">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="641fa-121">pp_Type</span><span class="sxs-lookup"><span data-stu-id="641fa-121">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="641fa-122">tp</span><span class="sxs-lookup"><span data-stu-id="641fa-122">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="641fa-123">tp_Type</span><span class="sxs-lookup"><span data-stu-id="641fa-123">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="641fa-124">属性</span><span class="sxs-lookup"><span data-stu-id="641fa-124">Attributes</span></span>

<span data-ttu-id="641fa-125">なし。</span><span class="sxs-lookup"><span data-stu-id="641fa-125">None.</span></span>
  

