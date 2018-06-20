---
title: FaceNames_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 234bbe07-004e-0604-144c-376d7b06994b
ms.openlocfilehash: 092a1a303e61fd3b9ab754dbaaf06ac810d6a295
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805356"
---
# <a name="facenamestype-complextype-visio-xml"></a><span data-ttu-id="4663f-102">FaceNames_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="4663f-102">FaceNames_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4663f-103">型情報</span><span class="sxs-lookup"><span data-stu-id="4663f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4663f-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="4663f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4663f-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4663f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4663f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4663f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4663f-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="4663f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4663f-108">なし</span><span class="sxs-lookup"><span data-stu-id="4663f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4663f-109">定義</span><span class="sxs-lookup"><span data-stu-id="4663f-109">Definition</span></span>

```XML
          <xs:complexType name="FaceNames_Type">
          
          <xs:sequence>
    <xs:element name="FaceName"  type="FaceName_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4663f-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4663f-110">Elements and attributes</span></span>

<span data-ttu-id="4663f-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4663f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4663f-112">子要素</span><span class="sxs-lookup"><span data-stu-id="4663f-112">Child elements</span></span>

|<span data-ttu-id="4663f-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="4663f-113">**Element**</span></span>|<span data-ttu-id="4663f-114">**型**</span><span class="sxs-lookup"><span data-stu-id="4663f-114">**Type**</span></span>|<span data-ttu-id="4663f-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="4663f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4663f-116">フォント名</span><span class="sxs-lookup"><span data-stu-id="4663f-116">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4663f-117">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="4663f-117">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4663f-118">属性</span><span class="sxs-lookup"><span data-stu-id="4663f-118">Attributes</span></span>

<span data-ttu-id="4663f-119">なし。</span><span class="sxs-lookup"><span data-stu-id="4663f-119">None.</span></span>
  

