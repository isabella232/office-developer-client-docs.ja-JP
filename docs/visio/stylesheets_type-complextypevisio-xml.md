---
title: StyleSheets_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2603bc5-86bd-df29-43c2-25a39419ad1e
ms.openlocfilehash: a48dc8d4c8327cffc53469a8c6d8a81d021a4500
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806586"
---
# <a name="stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="de711-102">StyleSheets_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="de711-102">StyleSheets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="de711-103">型情報</span><span class="sxs-lookup"><span data-stu-id="de711-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de711-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="de711-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="de711-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="de711-105">**Schema file**</span></span> <br/> |<span data-ttu-id="de711-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="de711-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="de711-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="de711-107">**Extension base**</span></span> <br/> |<span data-ttu-id="de711-108">なし</span><span class="sxs-lookup"><span data-stu-id="de711-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="de711-109">定義</span><span class="sxs-lookup"><span data-stu-id="de711-109">Definition</span></span>

```XML
          <xs:complexType name="StyleSheets_Type">
          
          <xs:sequence>
    <xs:element name="StyleSheet"  type="StyleSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="de711-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="de711-110">Elements and attributes</span></span>

<span data-ttu-id="de711-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de711-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="de711-112">子要素</span><span class="sxs-lookup"><span data-stu-id="de711-112">Child elements</span></span>

|<span data-ttu-id="de711-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="de711-113">**Element**</span></span>|<span data-ttu-id="de711-114">**型**</span><span class="sxs-lookup"><span data-stu-id="de711-114">**Type**</span></span>|<span data-ttu-id="de711-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="de711-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="de711-116">スタイル シート</span><span class="sxs-lookup"><span data-stu-id="de711-116">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="de711-117">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="de711-117">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="de711-118">属性</span><span class="sxs-lookup"><span data-stu-id="de711-118">Attributes</span></span>

<span data-ttu-id="de711-119">なし。</span><span class="sxs-lookup"><span data-stu-id="de711-119">None.</span></span>
  

