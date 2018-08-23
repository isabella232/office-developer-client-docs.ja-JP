---
title: CommentList_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: 640ba8825ffdfaa92c7a7ce43fb6bfb92e19ce12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805038"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="3e890-102">CommentList_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="3e890-102">CommentList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3e890-103">型情報</span><span class="sxs-lookup"><span data-stu-id="3e890-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e890-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="3e890-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3e890-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="3e890-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3e890-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3e890-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3e890-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="3e890-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3e890-108">なし</span><span class="sxs-lookup"><span data-stu-id="3e890-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3e890-109">定義</span><span class="sxs-lookup"><span data-stu-id="3e890-109">Definition</span></span>

```XML
          <xs:complexType name="CommentList_Type">
          
          <xs:sequence>
    <xs:element name="CommentEntry"  type="CommentEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3e890-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="3e890-110">Elements and attributes</span></span>

<span data-ttu-id="3e890-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e890-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3e890-112">子要素</span><span class="sxs-lookup"><span data-stu-id="3e890-112">Child elements</span></span>

|<span data-ttu-id="3e890-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="3e890-113">**Element**</span></span>|<span data-ttu-id="3e890-114">**型**</span><span class="sxs-lookup"><span data-stu-id="3e890-114">**Type**</span></span>|<span data-ttu-id="3e890-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="3e890-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3e890-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="3e890-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3e890-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="3e890-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3e890-118">属性</span><span class="sxs-lookup"><span data-stu-id="3e890-118">Attributes</span></span>

<span data-ttu-id="3e890-119">なし。</span><span class="sxs-lookup"><span data-stu-id="3e890-119">None.</span></span>
  

