---
title: PublishSettings_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cf14299e-8d21-0eed-bbd7-ad33d4f03533
ms.openlocfilehash: 6e9974d35b904581d43f481a02b8a3adee811730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806130"
---
# <a name="publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="23cfb-102">PublishSettings_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="23cfb-102">PublishSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="23cfb-103">型情報</span><span class="sxs-lookup"><span data-stu-id="23cfb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23cfb-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="23cfb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="23cfb-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="23cfb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="23cfb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="23cfb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="23cfb-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="23cfb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="23cfb-108">なし</span><span class="sxs-lookup"><span data-stu-id="23cfb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="23cfb-109">定義</span><span class="sxs-lookup"><span data-stu-id="23cfb-109">Definition</span></span>

```XML
          <xs:complexType name="PublishSettings_Type">
          
          <xs:sequence>
    <xs:element name="PublishedPage"  type="PublishedPage_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshableData"  type="RefreshableData_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="23cfb-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="23cfb-110">Elements and attributes</span></span>

<span data-ttu-id="23cfb-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="23cfb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="23cfb-112">子要素</span><span class="sxs-lookup"><span data-stu-id="23cfb-112">Child elements</span></span>

|<span data-ttu-id="23cfb-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="23cfb-113">**Element**</span></span>|<span data-ttu-id="23cfb-114">**型**</span><span class="sxs-lookup"><span data-stu-id="23cfb-114">**Type**</span></span>|<span data-ttu-id="23cfb-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="23cfb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="23cfb-116">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="23cfb-116">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23cfb-117">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="23cfb-117">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23cfb-118">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="23cfb-118">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23cfb-119">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="23cfb-119">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="23cfb-120">属性</span><span class="sxs-lookup"><span data-stu-id="23cfb-120">Attributes</span></span>

<span data-ttu-id="23cfb-121">なし。</span><span class="sxs-lookup"><span data-stu-id="23cfb-121">None.</span></span>
  

