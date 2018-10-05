---
title: ActionsRow_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32777219-850b-9526-425f-bcb017c45093
ms.openlocfilehash: d62513877dc2c441d521b20505f5849ea31a1a4a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383941"
---
# <a name="actionsrowtype-complextype-visio-xml"></a><span data-ttu-id="b85e4-102">ActionsRow_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="b85e4-102">ActionsRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b85e4-103">型情報</span><span class="sxs-lookup"><span data-stu-id="b85e4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b85e4-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="b85e4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b85e4-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b85e4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b85e4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b85e4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b85e4-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="b85e4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b85e4-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="b85e4-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b85e4-109">定義</span><span class="sxs-lookup"><span data-stu-id="b85e4-109">Definition</span></span>

```XML
          <xs:complexType name="ActionsRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedIndexedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b85e4-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b85e4-110">Elements and attributes</span></span>

<span data-ttu-id="b85e4-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b85e4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b85e4-112">子要素</span><span class="sxs-lookup"><span data-stu-id="b85e4-112">Child elements</span></span>

|<span data-ttu-id="b85e4-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="b85e4-113">**Element**</span></span>|<span data-ttu-id="b85e4-114">**型**</span><span class="sxs-lookup"><span data-stu-id="b85e4-114">**Type**</span></span>|<span data-ttu-id="b85e4-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="b85e4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b85e4-116">Cell</span><span class="sxs-lookup"><span data-stu-id="b85e4-116">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="b85e4-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="b85e4-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b85e4-118">属性</span><span class="sxs-lookup"><span data-stu-id="b85e4-118">Attributes</span></span>

<span data-ttu-id="b85e4-119">なし。</span><span class="sxs-lookup"><span data-stu-id="b85e4-119">None.</span></span>
  

