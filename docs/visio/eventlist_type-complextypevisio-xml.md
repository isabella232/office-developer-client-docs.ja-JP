---
title: EventList_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: 454a54749e9f72cacc3e7359041705d3487b9e79
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392082"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="63dea-102">EventList_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="63dea-102">EventList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="63dea-103">型情報</span><span class="sxs-lookup"><span data-stu-id="63dea-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63dea-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="63dea-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="63dea-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="63dea-105">**Schema file**</span></span> <br/> |<span data-ttu-id="63dea-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="63dea-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="63dea-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="63dea-107">**Extension base**</span></span> <br/> |<span data-ttu-id="63dea-108">なし</span><span class="sxs-lookup"><span data-stu-id="63dea-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="63dea-109">定義</span><span class="sxs-lookup"><span data-stu-id="63dea-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="63dea-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="63dea-110">Elements and attributes</span></span>

<span data-ttu-id="63dea-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="63dea-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="63dea-112">子要素</span><span class="sxs-lookup"><span data-stu-id="63dea-112">Child elements</span></span>

|<span data-ttu-id="63dea-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="63dea-113">**Element**</span></span>|<span data-ttu-id="63dea-114">**型**</span><span class="sxs-lookup"><span data-stu-id="63dea-114">**Type**</span></span>|<span data-ttu-id="63dea-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="63dea-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="63dea-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="63dea-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="63dea-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="63dea-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="63dea-118">属性</span><span class="sxs-lookup"><span data-stu-id="63dea-118">Attributes</span></span>

<span data-ttu-id="63dea-119">なし。</span><span class="sxs-lookup"><span data-stu-id="63dea-119">None.</span></span>
  

