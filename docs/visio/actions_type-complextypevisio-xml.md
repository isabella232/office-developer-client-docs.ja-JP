---
title: Actions_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: e28b80e64865196fd6ba13035385b9523f6b1bc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804759"
---
# <a name="actionstype-complextype-visio-xml"></a><span data-ttu-id="b2b6a-102">Actions_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="b2b6a-102">Actions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b2b6a-103">型情報</span><span class="sxs-lookup"><span data-stu-id="b2b6a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2b6a-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="b2b6a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b2b6a-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b2b6a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b2b6a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b2b6a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b2b6a-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="b2b6a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b2b6a-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="b2b6a-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b2b6a-109">定義</span><span class="sxs-lookup"><span data-stu-id="b2b6a-109">Definition</span></span>

```XML
          <xs:complexType name="Actions_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b2b6a-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b2b6a-110">Elements and attributes</span></span>

<span data-ttu-id="b2b6a-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2b6a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b2b6a-112">子要素</span><span class="sxs-lookup"><span data-stu-id="b2b6a-112">Child elements</span></span>

|<span data-ttu-id="b2b6a-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="b2b6a-113">**Element**</span></span>|<span data-ttu-id="b2b6a-114">**型**</span><span class="sxs-lookup"><span data-stu-id="b2b6a-114">**Type**</span></span>|<span data-ttu-id="b2b6a-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="b2b6a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b2b6a-116">Row</span><span class="sxs-lookup"><span data-stu-id="b2b6a-116">Row</span></span>](row-element-actions-sectionvisio-xml.md) <br/> |[<span data-ttu-id="b2b6a-117">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="b2b6a-117">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b2b6a-118">属性</span><span class="sxs-lookup"><span data-stu-id="b2b6a-118">Attributes</span></span>

<span data-ttu-id="b2b6a-119">なし。</span><span class="sxs-lookup"><span data-stu-id="b2b6a-119">None.</span></span>
  

