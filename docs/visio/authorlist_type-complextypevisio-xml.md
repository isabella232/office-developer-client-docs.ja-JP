---
title: AuthorList_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: 5df48bcc69f0bd4aa818f265d0c7db1986165b3e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537900"
---
# <a name="authorlist_type-complextype-visio-xml"></a><span data-ttu-id="a0aed-102">AuthorList_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a0aed-102">AuthorList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a0aed-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a0aed-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0aed-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a0aed-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a0aed-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a0aed-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a0aed-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a0aed-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a0aed-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a0aed-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a0aed-108">なし</span><span class="sxs-lookup"><span data-stu-id="a0aed-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a0aed-109">定義</span><span class="sxs-lookup"><span data-stu-id="a0aed-109">Definition</span></span>

```XML
          <xs:complexType name="AuthorList_Type">
          
          <xs:sequence>
    <xs:element name="AuthorEntry"  type="AuthorEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a0aed-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a0aed-110">Elements and attributes</span></span>

<span data-ttu-id="a0aed-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0aed-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a0aed-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a0aed-112">Child elements</span></span>

|<span data-ttu-id="a0aed-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a0aed-113">**Element**</span></span>|<span data-ttu-id="a0aed-114">**型**</span><span class="sxs-lookup"><span data-stu-id="a0aed-114">**Type**</span></span>|<span data-ttu-id="a0aed-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="a0aed-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a0aed-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="a0aed-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a0aed-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="a0aed-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a0aed-118">属性</span><span class="sxs-lookup"><span data-stu-id="a0aed-118">Attributes</span></span>

<span data-ttu-id="a0aed-119">なし。</span><span class="sxs-lookup"><span data-stu-id="a0aed-119">None.</span></span>
  

