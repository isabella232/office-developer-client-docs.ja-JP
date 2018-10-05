---
title: Pages_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13508e59-e29a-ca70-676b-c5b23ca8e3d0
ms.openlocfilehash: a03c5df25a28da40724178cf1c7f917ee4e723c5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400160"
---
# <a name="pagestype-complextype-visio-xml"></a><span data-ttu-id="9fd87-102">Pages_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="9fd87-102">Pages_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9fd87-103">型情報</span><span class="sxs-lookup"><span data-stu-id="9fd87-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fd87-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="9fd87-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9fd87-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9fd87-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9fd87-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9fd87-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9fd87-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="9fd87-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9fd87-108">なし</span><span class="sxs-lookup"><span data-stu-id="9fd87-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9fd87-109">定義</span><span class="sxs-lookup"><span data-stu-id="9fd87-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9fd87-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9fd87-110">Elements and attributes</span></span>

<span data-ttu-id="9fd87-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9fd87-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9fd87-112">子要素</span><span class="sxs-lookup"><span data-stu-id="9fd87-112">Child elements</span></span>

|<span data-ttu-id="9fd87-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="9fd87-113">**Element**</span></span>|<span data-ttu-id="9fd87-114">**型**</span><span class="sxs-lookup"><span data-stu-id="9fd87-114">**Type**</span></span>|<span data-ttu-id="9fd87-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="9fd87-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fd87-116">Page</span><span class="sxs-lookup"><span data-stu-id="9fd87-116">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fd87-117">Page_Type</span><span class="sxs-lookup"><span data-stu-id="9fd87-117">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9fd87-118">属性</span><span class="sxs-lookup"><span data-stu-id="9fd87-118">Attributes</span></span>

<span data-ttu-id="9fd87-119">なし。</span><span class="sxs-lookup"><span data-stu-id="9fd87-119">None.</span></span>
  

