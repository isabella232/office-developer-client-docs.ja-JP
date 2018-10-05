---
title: HyperlinkRow_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f8ded1a6-3bbd-0d59-c9f0-ab84341888cd
ms.openlocfilehash: 0056c87f4926f440ffcfd85619fd5ab7cba308db
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401651"
---
# <a name="hyperlinkrowtype-complextype-visio-xml"></a><span data-ttu-id="f95d9-102">HyperlinkRow_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="f95d9-102">HyperlinkRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f95d9-103">型情報</span><span class="sxs-lookup"><span data-stu-id="f95d9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f95d9-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="f95d9-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f95d9-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f95d9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f95d9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f95d9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f95d9-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="f95d9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f95d9-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="f95d9-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f95d9-109">定義</span><span class="sxs-lookup"><span data-stu-id="f95d9-109">Definition</span></span>

```XML
          <xs:complexType name="HyperlinkRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="f95d9-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f95d9-110">Elements and attributes</span></span>

<span data-ttu-id="f95d9-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f95d9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f95d9-112">子要素</span><span class="sxs-lookup"><span data-stu-id="f95d9-112">Child elements</span></span>

|<span data-ttu-id="f95d9-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="f95d9-113">**Element**</span></span>|<span data-ttu-id="f95d9-114">**型**</span><span class="sxs-lookup"><span data-stu-id="f95d9-114">**Type**</span></span>|<span data-ttu-id="f95d9-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="f95d9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f95d9-116">Cell</span><span class="sxs-lookup"><span data-stu-id="f95d9-116">Cell</span></span>](cell-element-hyperlink-rowvisio-xml.md) <br/> |[<span data-ttu-id="f95d9-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="f95d9-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f95d9-118">属性</span><span class="sxs-lookup"><span data-stu-id="f95d9-118">Attributes</span></span>

<span data-ttu-id="f95d9-119">なし。</span><span class="sxs-lookup"><span data-stu-id="f95d9-119">None.</span></span>
  

