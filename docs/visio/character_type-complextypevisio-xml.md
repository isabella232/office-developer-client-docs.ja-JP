---
title: Character_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 94a2aab3-6220-0cc5-ddc8-77a785821985
ms.openlocfilehash: 0605298eadf57492b4af4ce1c987f01a9130281b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805000"
---
# <a name="charactertype-complextype-visio-xml"></a><span data-ttu-id="c2ad1-102">Character_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="c2ad1-102">Character_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c2ad1-103">型情報</span><span class="sxs-lookup"><span data-stu-id="c2ad1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2ad1-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="c2ad1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c2ad1-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c2ad1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c2ad1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c2ad1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c2ad1-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="c2ad1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c2ad1-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="c2ad1-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c2ad1-109">定義</span><span class="sxs-lookup"><span data-stu-id="c2ad1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c2ad1-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c2ad1-110">Elements and attributes</span></span>

<span data-ttu-id="c2ad1-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c2ad1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c2ad1-112">子要素</span><span class="sxs-lookup"><span data-stu-id="c2ad1-112">Child elements</span></span>

|<span data-ttu-id="c2ad1-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="c2ad1-113">**Element**</span></span>|<span data-ttu-id="c2ad1-114">**型**</span><span class="sxs-lookup"><span data-stu-id="c2ad1-114">**Type**</span></span>|<span data-ttu-id="c2ad1-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="c2ad1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c2ad1-116">Row</span><span class="sxs-lookup"><span data-stu-id="c2ad1-116">Row</span></span>](row-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c2ad1-117">CharacterRow_Type</span><span class="sxs-lookup"><span data-stu-id="c2ad1-117">CharacterRow_Type</span></span>](characterrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c2ad1-118">属性</span><span class="sxs-lookup"><span data-stu-id="c2ad1-118">Attributes</span></span>

<span data-ttu-id="c2ad1-119">なし。</span><span class="sxs-lookup"><span data-stu-id="c2ad1-119">None.</span></span>
  

