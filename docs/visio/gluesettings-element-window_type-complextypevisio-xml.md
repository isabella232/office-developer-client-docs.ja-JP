---
title: GlueSettings 要素 (Window_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b5292f82-f299-ea96-6101-ebb799bbec9a
description: 図面で接着が有効になっている場合に、図形を接着するオブジェクトを指定します。
ms.openlocfilehash: 46d1ec09729cd26cfa3fc2f78a39edb6e7b7b02f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351213"
---
# <a name="gluesettings-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="b5ce5-103">GlueSettings 要素 (Window_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b5ce5-103">GlueSettings element (Window_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b5ce5-104">図面で接着が有効になっている場合に、図形を接着するオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="b5ce5-104">Specifies the objects that shapes glue to when glue is enabled in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5ce5-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="b5ce5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5ce5-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="b5ce5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b5ce5-107">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="b5ce5-107">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b5ce5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b5ce5-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b5ce5-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b5ce5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b5ce5-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="b5ce5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b5ce5-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="b5ce5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b5ce5-112">windows .xml、document .xml</span><span class="sxs-lookup"><span data-stu-id="b5ce5-112">windows.xml, document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5ce5-113">定義</span><span class="sxs-lookup"><span data-stu-id="b5ce5-113">Definition</span></span>

```XML
< xs:element name="GlueSettings" type="GlueSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5ce5-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b5ce5-114">Elements and attributes</span></span>

<span data-ttu-id="b5ce5-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5ce5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b5ce5-116">親要素</span><span class="sxs-lookup"><span data-stu-id="b5ce5-116">Parent elements</span></span>

|<span data-ttu-id="b5ce5-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="b5ce5-117">**Element**</span></span>|<span data-ttu-id="b5ce5-118">**型**</span><span class="sxs-lookup"><span data-stu-id="b5ce5-118">**Type**</span></span>|<span data-ttu-id="b5ce5-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="b5ce5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5ce5-120">Window</span><span class="sxs-lookup"><span data-stu-id="b5ce5-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b5ce5-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="b5ce5-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b5ce5-122">Microsoft Visio インスタンスで開いているウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="b5ce5-122">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b5ce5-123">子要素</span><span class="sxs-lookup"><span data-stu-id="b5ce5-123">Child elements</span></span>

<span data-ttu-id="b5ce5-124">なし。</span><span class="sxs-lookup"><span data-stu-id="b5ce5-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5ce5-125">属性</span><span class="sxs-lookup"><span data-stu-id="b5ce5-125">Attributes</span></span>

<span data-ttu-id="b5ce5-126">なし。</span><span class="sxs-lookup"><span data-stu-id="b5ce5-126">None.</span></span>
  

