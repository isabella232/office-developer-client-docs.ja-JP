---
title: Control_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eba241a-e64d-6bac-6d8e-a049e4febe96
ms.openlocfilehash: 13eb8f24377cb7c1b34d41c6ca963c545c3806e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805142"
---
# <a name="controltype-complextype-visio-xml"></a><span data-ttu-id="0e076-102">Control_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="0e076-102">Control_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0e076-103">型情報</span><span class="sxs-lookup"><span data-stu-id="0e076-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e076-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="0e076-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0e076-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0e076-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0e076-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0e076-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0e076-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="0e076-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0e076-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="0e076-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0e076-109">定義</span><span class="sxs-lookup"><span data-stu-id="0e076-109">Definition</span></span>

```XML
          <xs:complexType name="Control_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ControlRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0e076-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0e076-110">Elements and attributes</span></span>

<span data-ttu-id="0e076-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e076-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0e076-112">子要素</span><span class="sxs-lookup"><span data-stu-id="0e076-112">Child elements</span></span>

|<span data-ttu-id="0e076-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="0e076-113">**Element**</span></span>|<span data-ttu-id="0e076-114">**型**</span><span class="sxs-lookup"><span data-stu-id="0e076-114">**Type**</span></span>|<span data-ttu-id="0e076-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="0e076-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0e076-116">Row</span><span class="sxs-lookup"><span data-stu-id="0e076-116">Row</span></span>](row-element-controls-sectionvisio-xml.md) <br/> |[<span data-ttu-id="0e076-117">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="0e076-117">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0e076-118">属性</span><span class="sxs-lookup"><span data-stu-id="0e076-118">Attributes</span></span>

<span data-ttu-id="0e076-119">なし。</span><span class="sxs-lookup"><span data-stu-id="0e076-119">None.</span></span>
  

