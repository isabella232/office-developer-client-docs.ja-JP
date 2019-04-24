---
title: UserRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae2e014b-2e53-c317-0bfa-9a0cb1e09588
ms.openlocfilehash: 54edb9a1396582eae87db8735c4f75bd9597f1f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337073"
---
# <a name="userrowtype-complextype-visio-xml"></a><span data-ttu-id="dcb0b-102">UserRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="dcb0b-102">UserRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="dcb0b-103">型情報</span><span class="sxs-lookup"><span data-stu-id="dcb0b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dcb0b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dcb0b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dcb0b-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="dcb0b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dcb0b-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="dcb0b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dcb0b-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="dcb0b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dcb0b-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="dcb0b-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dcb0b-109">定義</span><span class="sxs-lookup"><span data-stu-id="dcb0b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="dcb0b-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="dcb0b-110">Elements and attributes</span></span>

<span data-ttu-id="dcb0b-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dcb0b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dcb0b-112">子要素</span><span class="sxs-lookup"><span data-stu-id="dcb0b-112">Child elements</span></span>

|<span data-ttu-id="dcb0b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="dcb0b-113">**Element**</span></span>|<span data-ttu-id="dcb0b-114">**型**</span><span class="sxs-lookup"><span data-stu-id="dcb0b-114">**Type**</span></span>|<span data-ttu-id="dcb0b-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="dcb0b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dcb0b-116">Cell</span><span class="sxs-lookup"><span data-stu-id="dcb0b-116">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="dcb0b-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="dcb0b-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="dcb0b-118">属性</span><span class="sxs-lookup"><span data-stu-id="dcb0b-118">Attributes</span></span>

<span data-ttu-id="dcb0b-119">なし。</span><span class="sxs-lookup"><span data-stu-id="dcb0b-119">None.</span></span>
  

