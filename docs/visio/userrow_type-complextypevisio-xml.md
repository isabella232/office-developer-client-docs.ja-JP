---
title: UserRow_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae2e014b-2e53-c317-0bfa-9a0cb1e09588
ms.openlocfilehash: 54edb9a1396582eae87db8735c4f75bd9597f1f3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399670"
---
# <a name="userrowtype-complextype-visio-xml"></a><span data-ttu-id="4f856-102">UserRow_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="4f856-102">UserRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4f856-103">型情報</span><span class="sxs-lookup"><span data-stu-id="4f856-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f856-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="4f856-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4f856-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4f856-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4f856-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4f856-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4f856-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="4f856-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4f856-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="4f856-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f856-109">定義</span><span class="sxs-lookup"><span data-stu-id="4f856-109">Definition</span></span>

```XML
          <xs:complexType name="UserRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="4f856-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4f856-110">Elements and attributes</span></span>

<span data-ttu-id="4f856-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f856-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4f856-112">子要素</span><span class="sxs-lookup"><span data-stu-id="4f856-112">Child elements</span></span>

|<span data-ttu-id="4f856-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="4f856-113">**Element**</span></span>|<span data-ttu-id="4f856-114">**型**</span><span class="sxs-lookup"><span data-stu-id="4f856-114">**Type**</span></span>|<span data-ttu-id="4f856-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="4f856-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f856-116">Cell</span><span class="sxs-lookup"><span data-stu-id="4f856-116">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="4f856-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4f856-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4f856-118">属性</span><span class="sxs-lookup"><span data-stu-id="4f856-118">Attributes</span></span>

<span data-ttu-id="4f856-119">なし。</span><span class="sxs-lookup"><span data-stu-id="4f856-119">None.</span></span>
  

