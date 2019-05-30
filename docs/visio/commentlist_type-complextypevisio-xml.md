---
title: CommentList_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: 9b85a3731cfde30307084c65da1d23aa86280afd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542052"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="fd57f-102">CommentList_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fd57f-102">CommentList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="fd57f-103">型情報</span><span class="sxs-lookup"><span data-stu-id="fd57f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd57f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fd57f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fd57f-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="fd57f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fd57f-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="fd57f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fd57f-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="fd57f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fd57f-108">None</span><span class="sxs-lookup"><span data-stu-id="fd57f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fd57f-109">定義</span><span class="sxs-lookup"><span data-stu-id="fd57f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fd57f-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="fd57f-110">Elements and attributes</span></span>

<span data-ttu-id="fd57f-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd57f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fd57f-112">子要素</span><span class="sxs-lookup"><span data-stu-id="fd57f-112">Child elements</span></span>

|<span data-ttu-id="fd57f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd57f-113">**Element**</span></span>|<span data-ttu-id="fd57f-114">**型**</span><span class="sxs-lookup"><span data-stu-id="fd57f-114">**Type**</span></span>|<span data-ttu-id="fd57f-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="fd57f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fd57f-116">コメントエントリ</span><span class="sxs-lookup"><span data-stu-id="fd57f-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fd57f-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="fd57f-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fd57f-118">属性</span><span class="sxs-lookup"><span data-stu-id="fd57f-118">Attributes</span></span>

<span data-ttu-id="fd57f-119">なし。</span><span class="sxs-lookup"><span data-stu-id="fd57f-119">None.</span></span>
  

