---
title: Colors_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: e447ceb6fc0e6b79ec6e62b5f3b73a32cec589d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359025"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="5cebe-102">Colors_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="5cebe-102">Colors_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5cebe-103">型情報</span><span class="sxs-lookup"><span data-stu-id="5cebe-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5cebe-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5cebe-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5cebe-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5cebe-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5cebe-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="5cebe-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5cebe-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="5cebe-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5cebe-108">なし</span><span class="sxs-lookup"><span data-stu-id="5cebe-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5cebe-109">定義</span><span class="sxs-lookup"><span data-stu-id="5cebe-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5cebe-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5cebe-110">Elements and attributes</span></span>

<span data-ttu-id="5cebe-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cebe-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5cebe-112">子要素</span><span class="sxs-lookup"><span data-stu-id="5cebe-112">Child elements</span></span>

|<span data-ttu-id="5cebe-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5cebe-113">**Element**</span></span>|<span data-ttu-id="5cebe-114">**型**</span><span class="sxs-lookup"><span data-stu-id="5cebe-114">**Type**</span></span>|<span data-ttu-id="5cebe-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="5cebe-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5cebe-116">colorentry</span><span class="sxs-lookup"><span data-stu-id="5cebe-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5cebe-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="5cebe-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5cebe-118">属性</span><span class="sxs-lookup"><span data-stu-id="5cebe-118">Attributes</span></span>

<span data-ttu-id="5cebe-119">なし。</span><span class="sxs-lookup"><span data-stu-id="5cebe-119">None.</span></span>
  

