---
title: Colors_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: bddcb93451bfb6d1b519720040a9e3875dc2ec5c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540141"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="b9337-102">Colors_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b9337-102">Colors_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b9337-103">型情報</span><span class="sxs-lookup"><span data-stu-id="b9337-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9337-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b9337-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b9337-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b9337-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b9337-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="b9337-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b9337-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="b9337-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b9337-108">None</span><span class="sxs-lookup"><span data-stu-id="b9337-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b9337-109">定義</span><span class="sxs-lookup"><span data-stu-id="b9337-109">Definition</span></span>

```XML
          <xs:complexType name="Colors_Type">
          
          <xs:sequence>
    <xs:element name="ColorEntry"  type="ColorEntry_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b9337-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b9337-110">Elements and attributes</span></span>

<span data-ttu-id="b9337-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9337-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b9337-112">子要素</span><span class="sxs-lookup"><span data-stu-id="b9337-112">Child elements</span></span>

|<span data-ttu-id="b9337-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b9337-113">**Element**</span></span>|<span data-ttu-id="b9337-114">**型**</span><span class="sxs-lookup"><span data-stu-id="b9337-114">**Type**</span></span>|<span data-ttu-id="b9337-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="b9337-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b9337-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="b9337-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b9337-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="b9337-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b9337-118">属性</span><span class="sxs-lookup"><span data-stu-id="b9337-118">Attributes</span></span>

<span data-ttu-id="b9337-119">なし。</span><span class="sxs-lookup"><span data-stu-id="b9337-119">None.</span></span>
  

