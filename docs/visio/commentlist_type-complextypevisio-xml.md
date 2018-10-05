---
title: CommentList_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: af23616556cecdbfa1157a8d4c49de1ca4b2fd88
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393097"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="3e637-102">CommentList_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="3e637-102">CommentList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3e637-103">型情報</span><span class="sxs-lookup"><span data-stu-id="3e637-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e637-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="3e637-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3e637-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="3e637-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3e637-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3e637-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3e637-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="3e637-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3e637-108">なし</span><span class="sxs-lookup"><span data-stu-id="3e637-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3e637-109">定義</span><span class="sxs-lookup"><span data-stu-id="3e637-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3e637-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="3e637-110">Elements and attributes</span></span>

<span data-ttu-id="3e637-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e637-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3e637-112">子要素</span><span class="sxs-lookup"><span data-stu-id="3e637-112">Child elements</span></span>

|<span data-ttu-id="3e637-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="3e637-113">**Element**</span></span>|<span data-ttu-id="3e637-114">**型**</span><span class="sxs-lookup"><span data-stu-id="3e637-114">**Type**</span></span>|<span data-ttu-id="3e637-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="3e637-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3e637-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="3e637-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3e637-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="3e637-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3e637-118">属性</span><span class="sxs-lookup"><span data-stu-id="3e637-118">Attributes</span></span>

<span data-ttu-id="3e637-119">なし。</span><span class="sxs-lookup"><span data-stu-id="3e637-119">None.</span></span>
  

