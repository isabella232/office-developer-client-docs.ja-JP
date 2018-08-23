---
title: Colors_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: 187d51c2102e9d13ffea15c6de2db849ef980fb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805016"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="0b202-102">Colors_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="0b202-102">Colors_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0b202-103">型情報</span><span class="sxs-lookup"><span data-stu-id="0b202-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b202-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="0b202-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0b202-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0b202-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0b202-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0b202-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0b202-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="0b202-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0b202-108">なし</span><span class="sxs-lookup"><span data-stu-id="0b202-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0b202-109">定義</span><span class="sxs-lookup"><span data-stu-id="0b202-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0b202-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0b202-110">Elements and attributes</span></span>

<span data-ttu-id="0b202-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b202-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0b202-112">子要素</span><span class="sxs-lookup"><span data-stu-id="0b202-112">Child elements</span></span>

|<span data-ttu-id="0b202-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="0b202-113">**Element**</span></span>|<span data-ttu-id="0b202-114">**型**</span><span class="sxs-lookup"><span data-stu-id="0b202-114">**Type**</span></span>|<span data-ttu-id="0b202-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="0b202-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0b202-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="0b202-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0b202-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="0b202-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0b202-118">属性</span><span class="sxs-lookup"><span data-stu-id="0b202-118">Attributes</span></span>

<span data-ttu-id="0b202-119">なし。</span><span class="sxs-lookup"><span data-stu-id="0b202-119">None.</span></span>
  

