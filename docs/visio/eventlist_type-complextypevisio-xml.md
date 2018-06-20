---
title: EventList_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: 7bbb8d1074d869a9171a188118c920260b3a903d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805335"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="e4245-102">EventList_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="e4245-102">EventList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e4245-103">型情報</span><span class="sxs-lookup"><span data-stu-id="e4245-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e4245-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="e4245-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e4245-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e4245-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e4245-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e4245-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e4245-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="e4245-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e4245-108">なし</span><span class="sxs-lookup"><span data-stu-id="e4245-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e4245-109">定義</span><span class="sxs-lookup"><span data-stu-id="e4245-109">Definition</span></span>

```XML
          <xs:complexType name="EventList_Type">
          
          <xs:sequence>
    <xs:element name="EventItem"  type="EventItem_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e4245-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e4245-110">Elements and attributes</span></span>

<span data-ttu-id="e4245-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4245-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e4245-112">子要素</span><span class="sxs-lookup"><span data-stu-id="e4245-112">Child elements</span></span>

|<span data-ttu-id="e4245-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="e4245-113">**Element**</span></span>|<span data-ttu-id="e4245-114">**型**</span><span class="sxs-lookup"><span data-stu-id="e4245-114">**Type**</span></span>|<span data-ttu-id="e4245-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="e4245-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e4245-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="e4245-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e4245-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="e4245-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e4245-118">属性</span><span class="sxs-lookup"><span data-stu-id="e4245-118">Attributes</span></span>

<span data-ttu-id="e4245-119">なし。</span><span class="sxs-lookup"><span data-stu-id="e4245-119">None.</span></span>
  

