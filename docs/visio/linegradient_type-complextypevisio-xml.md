---
title: LineGradient_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b36eb8f-d1af-9bbc-2822-0c3d09dfc2a9
ms.openlocfilehash: 026527ffb6b74ced088bc22ee715be9df1320334
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805688"
---
# <a name="linegradienttype-complextype-visio-xml"></a><span data-ttu-id="05070-102">LineGradient_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="05070-102">LineGradient_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="05070-103">型情報</span><span class="sxs-lookup"><span data-stu-id="05070-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05070-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="05070-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="05070-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="05070-105">**Schema file**</span></span> <br/> |<span data-ttu-id="05070-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="05070-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="05070-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="05070-107">**Extension base**</span></span> <br/> |<span data-ttu-id="05070-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="05070-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="05070-109">定義</span><span class="sxs-lookup"><span data-stu-id="05070-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LineGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="05070-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="05070-110">Elements and attributes</span></span>

<span data-ttu-id="05070-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="05070-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="05070-112">子要素</span><span class="sxs-lookup"><span data-stu-id="05070-112">Child elements</span></span>

|<span data-ttu-id="05070-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="05070-113">**Element**</span></span>|<span data-ttu-id="05070-114">**型**</span><span class="sxs-lookup"><span data-stu-id="05070-114">**Type**</span></span>|<span data-ttu-id="05070-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="05070-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="05070-116">Row</span><span class="sxs-lookup"><span data-stu-id="05070-116">Row</span></span>](row-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="05070-117">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="05070-117">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="05070-118">属性</span><span class="sxs-lookup"><span data-stu-id="05070-118">Attributes</span></span>

<span data-ttu-id="05070-119">なし。</span><span class="sxs-lookup"><span data-stu-id="05070-119">None.</span></span>
  

