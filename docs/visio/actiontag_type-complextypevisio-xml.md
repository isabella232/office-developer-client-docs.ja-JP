---
title: ActionTag_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bcc17e7-d59d-d392-f299-78d7665202fc
ms.openlocfilehash: a30290ee9dbb86c7af75820bd767bb95ce4add21
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384774"
---
# <a name="actiontagtype-complextype-visio-xml"></a><span data-ttu-id="352ed-102">ActionTag_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="352ed-102">ActionTag_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="352ed-103">型情報</span><span class="sxs-lookup"><span data-stu-id="352ed-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="352ed-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="352ed-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="352ed-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="352ed-105">**Schema file**</span></span> <br/> |<span data-ttu-id="352ed-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="352ed-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="352ed-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="352ed-107">**Extension base**</span></span> <br/> |<span data-ttu-id="352ed-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="352ed-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="352ed-109">定義</span><span class="sxs-lookup"><span data-stu-id="352ed-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTag_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionTagRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="352ed-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="352ed-110">Elements and attributes</span></span>

<span data-ttu-id="352ed-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="352ed-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="352ed-112">子要素</span><span class="sxs-lookup"><span data-stu-id="352ed-112">Child elements</span></span>

|<span data-ttu-id="352ed-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="352ed-113">**Element**</span></span>|<span data-ttu-id="352ed-114">**型**</span><span class="sxs-lookup"><span data-stu-id="352ed-114">**Type**</span></span>|<span data-ttu-id="352ed-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="352ed-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="352ed-116">Row</span><span class="sxs-lookup"><span data-stu-id="352ed-116">Row</span></span>](row-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="352ed-117">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="352ed-117">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="352ed-118">属性</span><span class="sxs-lookup"><span data-stu-id="352ed-118">Attributes</span></span>

<span data-ttu-id="352ed-119">なし。</span><span class="sxs-lookup"><span data-stu-id="352ed-119">None.</span></span>
  

