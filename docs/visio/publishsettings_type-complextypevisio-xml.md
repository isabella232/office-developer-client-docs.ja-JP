---
title: PublishSettings_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cf14299e-8d21-0eed-bbd7-ad33d4f03533
ms.openlocfilehash: 05bf2d6ec7e0b7d05f5aa85351c266712dcee851
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538922"
---
# <a name="publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="24077-102">PublishSettings_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="24077-102">PublishSettings_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="24077-103">型情報</span><span class="sxs-lookup"><span data-stu-id="24077-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24077-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="24077-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="24077-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="24077-105">**Schema file**</span></span> <br/> |<span data-ttu-id="24077-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="24077-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="24077-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="24077-107">**Extension base**</span></span> <br/> |<span data-ttu-id="24077-108">None</span><span class="sxs-lookup"><span data-stu-id="24077-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="24077-109">定義</span><span class="sxs-lookup"><span data-stu-id="24077-109">Definition</span></span>

```XML
          <xs:complexType name="PublishSettings_Type">
          
          <xs:sequence>
    <xs:element name="PublishedPage"  type="PublishedPage_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshableData"  type="RefreshableData_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="24077-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="24077-110">Elements and attributes</span></span>

<span data-ttu-id="24077-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="24077-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="24077-112">子要素</span><span class="sxs-lookup"><span data-stu-id="24077-112">Child elements</span></span>

|<span data-ttu-id="24077-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="24077-113">**Element**</span></span>|<span data-ttu-id="24077-114">**型**</span><span class="sxs-lookup"><span data-stu-id="24077-114">**Type**</span></span>|<span data-ttu-id="24077-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="24077-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="24077-116">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="24077-116">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="24077-117">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="24077-117">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="24077-118">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="24077-118">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="24077-119">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="24077-119">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="24077-120">属性</span><span class="sxs-lookup"><span data-stu-id="24077-120">Attributes</span></span>

<span data-ttu-id="24077-121">なし。</span><span class="sxs-lookup"><span data-stu-id="24077-121">None.</span></span>
  

