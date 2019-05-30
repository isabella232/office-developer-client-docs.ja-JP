---
title: Character_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 94a2aab3-6220-0cc5-ddc8-77a785821985
ms.openlocfilehash: c84a8d71fc2f080600a20625087d7c252bdcb3eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540204"
---
# <a name="charactertype-complextype-visio-xml"></a><span data-ttu-id="5e7ad-102">Character_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5e7ad-102">Character_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="5e7ad-103">型情報</span><span class="sxs-lookup"><span data-stu-id="5e7ad-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e7ad-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5e7ad-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5e7ad-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5e7ad-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5e7ad-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="5e7ad-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5e7ad-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="5e7ad-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5e7ad-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="5e7ad-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5e7ad-109">定義</span><span class="sxs-lookup"><span data-stu-id="5e7ad-109">Definition</span></span>

```XML
          <xs:complexType name="Character_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="CharacterRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5e7ad-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5e7ad-110">Elements and attributes</span></span>

<span data-ttu-id="5e7ad-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e7ad-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5e7ad-112">子要素</span><span class="sxs-lookup"><span data-stu-id="5e7ad-112">Child elements</span></span>

|<span data-ttu-id="5e7ad-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5e7ad-113">**Element**</span></span>|<span data-ttu-id="5e7ad-114">**型**</span><span class="sxs-lookup"><span data-stu-id="5e7ad-114">**Type**</span></span>|<span data-ttu-id="5e7ad-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="5e7ad-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5e7ad-116">Row</span><span class="sxs-lookup"><span data-stu-id="5e7ad-116">Row</span></span>](row-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="5e7ad-117">CharacterRow_Type</span><span class="sxs-lookup"><span data-stu-id="5e7ad-117">CharacterRow_Type</span></span>](characterrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5e7ad-118">属性</span><span class="sxs-lookup"><span data-stu-id="5e7ad-118">Attributes</span></span>

<span data-ttu-id="5e7ad-119">なし。</span><span class="sxs-lookup"><span data-stu-id="5e7ad-119">None.</span></span>
  

