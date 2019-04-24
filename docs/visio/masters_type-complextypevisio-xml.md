---
title: Masters_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: 4b66e0cb7fded75a8c65f2ce93bc42442bedb033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341658"
---
# <a name="masterstype-complextype-visio-xml"></a><span data-ttu-id="40987-102">Masters_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="40987-102">Masters_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="40987-103">型情報</span><span class="sxs-lookup"><span data-stu-id="40987-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40987-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="40987-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="40987-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="40987-105">**Schema file**</span></span> <br/> |<span data-ttu-id="40987-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="40987-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="40987-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="40987-107">**Extension base**</span></span> <br/> |<span data-ttu-id="40987-108">なし</span><span class="sxs-lookup"><span data-stu-id="40987-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="40987-109">定義</span><span class="sxs-lookup"><span data-stu-id="40987-109">Definition</span></span>

```XML
          <xs:complexType name="Masters_Type">
          
          <xs:sequence>
    <xs:element name="Master"  type="Master_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="MasterShortcut"  type="MasterShortcut_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="40987-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="40987-110">Elements and attributes</span></span>

<span data-ttu-id="40987-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="40987-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="40987-112">子要素</span><span class="sxs-lookup"><span data-stu-id="40987-112">Child elements</span></span>

|<span data-ttu-id="40987-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="40987-113">**Element**</span></span>|<span data-ttu-id="40987-114">**型**</span><span class="sxs-lookup"><span data-stu-id="40987-114">**Type**</span></span>|<span data-ttu-id="40987-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="40987-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="40987-116">Master</span><span class="sxs-lookup"><span data-stu-id="40987-116">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="40987-117">Master_Type</span><span class="sxs-lookup"><span data-stu-id="40987-117">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="40987-118">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="40987-118">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="40987-119">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="40987-119">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="40987-120">属性</span><span class="sxs-lookup"><span data-stu-id="40987-120">Attributes</span></span>

<span data-ttu-id="40987-121">なし。</span><span class="sxs-lookup"><span data-stu-id="40987-121">None.</span></span>
  

