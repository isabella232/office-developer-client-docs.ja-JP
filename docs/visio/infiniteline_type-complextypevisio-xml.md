---
title: InfiniteLine_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4463d388-f5dd-4c43-71d4-82ba216d8d39
ms.openlocfilehash: f9db3947381da563f2f7d9973d7b2578094d5235
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390374"
---
# <a name="infinitelinetype-complextype-visio-xml"></a><span data-ttu-id="399d1-102">InfiniteLine_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="399d1-102">InfiniteLine_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="399d1-103">型情報</span><span class="sxs-lookup"><span data-stu-id="399d1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="399d1-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="399d1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="399d1-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="399d1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="399d1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="399d1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="399d1-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="399d1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="399d1-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="399d1-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="399d1-109">定義</span><span class="sxs-lookup"><span data-stu-id="399d1-109">Definition</span></span>

```XML
          <xs:complexType name="InfiniteLine_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="399d1-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="399d1-110">Elements and attributes</span></span>

<span data-ttu-id="399d1-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="399d1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="399d1-112">子要素</span><span class="sxs-lookup"><span data-stu-id="399d1-112">Child elements</span></span>

|<span data-ttu-id="399d1-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="399d1-113">**Element**</span></span>|<span data-ttu-id="399d1-114">**型**</span><span class="sxs-lookup"><span data-stu-id="399d1-114">**Type**</span></span>|<span data-ttu-id="399d1-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="399d1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="399d1-116">Cell</span><span class="sxs-lookup"><span data-stu-id="399d1-116">Cell</span></span>](cell-element-infiniteline-rowvisio-xml.md) <br/> |[<span data-ttu-id="399d1-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="399d1-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="399d1-118">属性</span><span class="sxs-lookup"><span data-stu-id="399d1-118">Attributes</span></span>

<span data-ttu-id="399d1-119">なし。</span><span class="sxs-lookup"><span data-stu-id="399d1-119">None.</span></span>
  

