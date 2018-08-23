---
title: Pages_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13508e59-e29a-ca70-676b-c5b23ca8e3d0
ms.openlocfilehash: 45a59c41e0f2bdb2c1b260a1803c7ac14a84a6ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806002"
---
# <a name="pagestype-complextype-visio-xml"></a><span data-ttu-id="c45ff-102">Pages_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="c45ff-102">Pages_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c45ff-103">型情報</span><span class="sxs-lookup"><span data-stu-id="c45ff-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c45ff-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="c45ff-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c45ff-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c45ff-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c45ff-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c45ff-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c45ff-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="c45ff-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c45ff-108">なし</span><span class="sxs-lookup"><span data-stu-id="c45ff-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c45ff-109">定義</span><span class="sxs-lookup"><span data-stu-id="c45ff-109">Definition</span></span>

```XML
          <xs:complexType name="Pages_Type">
          
          <xs:sequence>
    <xs:element name="Page"  type="Page_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c45ff-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c45ff-110">Elements and attributes</span></span>

<span data-ttu-id="c45ff-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c45ff-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c45ff-112">子要素</span><span class="sxs-lookup"><span data-stu-id="c45ff-112">Child elements</span></span>

|<span data-ttu-id="c45ff-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="c45ff-113">**Element**</span></span>|<span data-ttu-id="c45ff-114">**型**</span><span class="sxs-lookup"><span data-stu-id="c45ff-114">**Type**</span></span>|<span data-ttu-id="c45ff-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="c45ff-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c45ff-116">Page</span><span class="sxs-lookup"><span data-stu-id="c45ff-116">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c45ff-117">Page_Type</span><span class="sxs-lookup"><span data-stu-id="c45ff-117">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c45ff-118">属性</span><span class="sxs-lookup"><span data-stu-id="c45ff-118">Attributes</span></span>

<span data-ttu-id="c45ff-119">なし。</span><span class="sxs-lookup"><span data-stu-id="c45ff-119">None.</span></span>
  

