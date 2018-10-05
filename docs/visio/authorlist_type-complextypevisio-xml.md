---
title: AuthorList_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: 80a0dd01b3628bc44ed469ff7c236753d7677f51
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394553"
---
# <a name="authorlisttype-complextype-visio-xml"></a><span data-ttu-id="ef75f-102">AuthorList_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="ef75f-102">AuthorList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ef75f-103">型情報</span><span class="sxs-lookup"><span data-stu-id="ef75f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef75f-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="ef75f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ef75f-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ef75f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ef75f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ef75f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ef75f-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="ef75f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ef75f-108">なし</span><span class="sxs-lookup"><span data-stu-id="ef75f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ef75f-109">定義</span><span class="sxs-lookup"><span data-stu-id="ef75f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ef75f-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ef75f-110">Elements and attributes</span></span>

<span data-ttu-id="ef75f-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef75f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ef75f-112">子要素</span><span class="sxs-lookup"><span data-stu-id="ef75f-112">Child elements</span></span>

|<span data-ttu-id="ef75f-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="ef75f-113">**Element**</span></span>|<span data-ttu-id="ef75f-114">**型**</span><span class="sxs-lookup"><span data-stu-id="ef75f-114">**Type**</span></span>|<span data-ttu-id="ef75f-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="ef75f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ef75f-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="ef75f-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ef75f-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="ef75f-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ef75f-118">属性</span><span class="sxs-lookup"><span data-stu-id="ef75f-118">Attributes</span></span>

<span data-ttu-id="ef75f-119">なし。</span><span class="sxs-lookup"><span data-stu-id="ef75f-119">None.</span></span>
  

