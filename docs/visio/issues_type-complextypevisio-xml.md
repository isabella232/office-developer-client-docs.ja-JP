---
title: Issues_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 1ebec9e42c71b93637155037bd881c8ddf330367
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805632"
---
# <a name="issuestype-complextype-visio-xml"></a><span data-ttu-id="7bc57-102">Issues_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="7bc57-102">Issues_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7bc57-103">型情報</span><span class="sxs-lookup"><span data-stu-id="7bc57-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7bc57-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="7bc57-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7bc57-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="7bc57-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7bc57-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7bc57-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7bc57-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="7bc57-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7bc57-108">なし</span><span class="sxs-lookup"><span data-stu-id="7bc57-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7bc57-109">定義</span><span class="sxs-lookup"><span data-stu-id="7bc57-109">Definition</span></span>

```XML
          <xs:complexType name="Issues_Type">
          
          <xs:sequence>
    <xs:element name="Issue"  type="Issue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7bc57-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="7bc57-110">Elements and attributes</span></span>

<span data-ttu-id="7bc57-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bc57-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7bc57-112">子要素</span><span class="sxs-lookup"><span data-stu-id="7bc57-112">Child elements</span></span>

|<span data-ttu-id="7bc57-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="7bc57-113">**Element**</span></span>|<span data-ttu-id="7bc57-114">**型**</span><span class="sxs-lookup"><span data-stu-id="7bc57-114">**Type**</span></span>|<span data-ttu-id="7bc57-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="7bc57-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7bc57-116">問題</span><span class="sxs-lookup"><span data-stu-id="7bc57-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7bc57-117">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="7bc57-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7bc57-118">属性</span><span class="sxs-lookup"><span data-stu-id="7bc57-118">Attributes</span></span>

<span data-ttu-id="7bc57-119">なし。</span><span class="sxs-lookup"><span data-stu-id="7bc57-119">None.</span></span>
  

