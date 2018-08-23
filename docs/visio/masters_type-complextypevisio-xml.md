---
title: Masters_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: ee53a4c5ce07151b0ba58ebe08a4b69cca12d313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805827"
---
# <a name="masterstype-complextype-visio-xml"></a><span data-ttu-id="a25cc-102">Masters_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a25cc-102">Masters_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a25cc-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a25cc-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a25cc-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a25cc-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a25cc-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a25cc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a25cc-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a25cc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a25cc-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a25cc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a25cc-108">なし</span><span class="sxs-lookup"><span data-stu-id="a25cc-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a25cc-109">定義</span><span class="sxs-lookup"><span data-stu-id="a25cc-109">Definition</span></span>

```XML
          <xs:complexType name="Masters_Type">
          
          <xs:sequence>
    <xs:element name="Master"  type="Master_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="MasterShortcut"  type="MasterShortcut_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a25cc-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a25cc-110">Elements and attributes</span></span>

<span data-ttu-id="a25cc-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a25cc-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a25cc-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a25cc-112">Child elements</span></span>

|<span data-ttu-id="a25cc-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="a25cc-113">**Element**</span></span>|<span data-ttu-id="a25cc-114">**型**</span><span class="sxs-lookup"><span data-stu-id="a25cc-114">**Type**</span></span>|<span data-ttu-id="a25cc-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="a25cc-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a25cc-116">Master</span><span class="sxs-lookup"><span data-stu-id="a25cc-116">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a25cc-117">Master_Type</span><span class="sxs-lookup"><span data-stu-id="a25cc-117">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a25cc-118">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="a25cc-118">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a25cc-119">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="a25cc-119">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a25cc-120">属性</span><span class="sxs-lookup"><span data-stu-id="a25cc-120">Attributes</span></span>

<span data-ttu-id="a25cc-121">なし。</span><span class="sxs-lookup"><span data-stu-id="a25cc-121">None.</span></span>
  

