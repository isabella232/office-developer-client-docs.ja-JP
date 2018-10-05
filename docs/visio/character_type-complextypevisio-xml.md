---
title: Character_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 94a2aab3-6220-0cc5-ddc8-77a785821985
ms.openlocfilehash: d4145bf92c053f67ed11e827b528e05fd4ffc7f5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386601"
---
# <a name="charactertype-complextype-visio-xml"></a><span data-ttu-id="d8a84-102">Character_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="d8a84-102">Character_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d8a84-103">型情報</span><span class="sxs-lookup"><span data-stu-id="d8a84-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8a84-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="d8a84-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d8a84-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d8a84-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d8a84-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d8a84-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d8a84-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="d8a84-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d8a84-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d8a84-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d8a84-109">定義</span><span class="sxs-lookup"><span data-stu-id="d8a84-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d8a84-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d8a84-110">Elements and attributes</span></span>

<span data-ttu-id="d8a84-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d8a84-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d8a84-112">子要素</span><span class="sxs-lookup"><span data-stu-id="d8a84-112">Child elements</span></span>

|<span data-ttu-id="d8a84-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="d8a84-113">**Element**</span></span>|<span data-ttu-id="d8a84-114">**型**</span><span class="sxs-lookup"><span data-stu-id="d8a84-114">**Type**</span></span>|<span data-ttu-id="d8a84-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="d8a84-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d8a84-116">Row</span><span class="sxs-lookup"><span data-stu-id="d8a84-116">Row</span></span>](row-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d8a84-117">CharacterRow_Type</span><span class="sxs-lookup"><span data-stu-id="d8a84-117">CharacterRow_Type</span></span>](characterrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d8a84-118">属性</span><span class="sxs-lookup"><span data-stu-id="d8a84-118">Attributes</span></span>

<span data-ttu-id="d8a84-119">なし。</span><span class="sxs-lookup"><span data-stu-id="d8a84-119">None.</span></span>
  

