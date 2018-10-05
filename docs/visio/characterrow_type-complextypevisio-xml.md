---
title: CharacterRow_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61c99712-d451-408a-de15-fb088605b07c
ms.openlocfilehash: 40c67d638776015b7aca0992191af154a9852f26
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387371"
---
# <a name="characterrowtype-complextype-visio-xml"></a><span data-ttu-id="e3b80-102">CharacterRow_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="e3b80-102">CharacterRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e3b80-103">型情報</span><span class="sxs-lookup"><span data-stu-id="e3b80-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3b80-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="e3b80-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e3b80-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e3b80-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e3b80-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e3b80-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e3b80-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="e3b80-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e3b80-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="e3b80-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e3b80-109">定義</span><span class="sxs-lookup"><span data-stu-id="e3b80-109">Definition</span></span>

```XML
          <xs:complexType name="CharacterRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e3b80-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e3b80-110">Elements and attributes</span></span>

<span data-ttu-id="e3b80-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e3b80-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e3b80-112">子要素</span><span class="sxs-lookup"><span data-stu-id="e3b80-112">Child elements</span></span>

|<span data-ttu-id="e3b80-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="e3b80-113">**Element**</span></span>|<span data-ttu-id="e3b80-114">**型**</span><span class="sxs-lookup"><span data-stu-id="e3b80-114">**Type**</span></span>|<span data-ttu-id="e3b80-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="e3b80-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e3b80-116">Cell</span><span class="sxs-lookup"><span data-stu-id="e3b80-116">Cell</span></span>](cell-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e3b80-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e3b80-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e3b80-118">属性</span><span class="sxs-lookup"><span data-stu-id="e3b80-118">Attributes</span></span>

<span data-ttu-id="e3b80-119">なし。</span><span class="sxs-lookup"><span data-stu-id="e3b80-119">None.</span></span>
  

