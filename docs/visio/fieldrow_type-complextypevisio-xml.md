---
title: FieldRow_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3474d268-4435-cb4d-9c66-a30924635e20
ms.openlocfilehash: 5f59ca23fa83d98622624cc20544f9b482ce5378
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400783"
---
# <a name="fieldrowtype-complextype-visio-xml"></a><span data-ttu-id="88cb7-102">FieldRow_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="88cb7-102">FieldRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="88cb7-103">型情報</span><span class="sxs-lookup"><span data-stu-id="88cb7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88cb7-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="88cb7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="88cb7-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="88cb7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="88cb7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="88cb7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="88cb7-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="88cb7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="88cb7-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="88cb7-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88cb7-109">定義</span><span class="sxs-lookup"><span data-stu-id="88cb7-109">Definition</span></span>

```XML
          <xs:complexType name="FieldRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="88cb7-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="88cb7-110">Elements and attributes</span></span>

<span data-ttu-id="88cb7-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88cb7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="88cb7-112">子要素</span><span class="sxs-lookup"><span data-stu-id="88cb7-112">Child elements</span></span>

|<span data-ttu-id="88cb7-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="88cb7-113">**Element**</span></span>|<span data-ttu-id="88cb7-114">**型**</span><span class="sxs-lookup"><span data-stu-id="88cb7-114">**Type**</span></span>|<span data-ttu-id="88cb7-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="88cb7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="88cb7-116">Cell</span><span class="sxs-lookup"><span data-stu-id="88cb7-116">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="88cb7-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="88cb7-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="88cb7-118">属性</span><span class="sxs-lookup"><span data-stu-id="88cb7-118">Attributes</span></span>

<span data-ttu-id="88cb7-119">なし。</span><span class="sxs-lookup"><span data-stu-id="88cb7-119">None.</span></span>
  

