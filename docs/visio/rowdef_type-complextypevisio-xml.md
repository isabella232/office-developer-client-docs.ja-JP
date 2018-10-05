---
title: RowDef_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: 11acab820fe51b6dde9cf9d57977699ca3c977cb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394588"
---
# <a name="rowdeftype-complextype-visio-xml"></a><span data-ttu-id="c9e66-102">RowDef_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="c9e66-102">RowDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c9e66-103">型情報</span><span class="sxs-lookup"><span data-stu-id="c9e66-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9e66-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="c9e66-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c9e66-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c9e66-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c9e66-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c9e66-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c9e66-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="c9e66-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c9e66-108">なし</span><span class="sxs-lookup"><span data-stu-id="c9e66-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c9e66-109">定義</span><span class="sxs-lookup"><span data-stu-id="c9e66-109">Definition</span></span>

```XML
          <xs:complexType name="RowDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c9e66-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c9e66-110">Elements and attributes</span></span>

<span data-ttu-id="c9e66-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9e66-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c9e66-112">子要素</span><span class="sxs-lookup"><span data-stu-id="c9e66-112">Child elements</span></span>

|<span data-ttu-id="c9e66-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="c9e66-113">**Element**</span></span>|<span data-ttu-id="c9e66-114">**型**</span><span class="sxs-lookup"><span data-stu-id="c9e66-114">**Type**</span></span>|<span data-ttu-id="c9e66-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="c9e66-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9e66-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="c9e66-116">CellDef</span></span> <br/> |[<span data-ttu-id="c9e66-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="c9e66-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c9e66-118">属性</span><span class="sxs-lookup"><span data-stu-id="c9e66-118">Attributes</span></span>

<span data-ttu-id="c9e66-119">なし。</span><span class="sxs-lookup"><span data-stu-id="c9e66-119">None.</span></span>
  

