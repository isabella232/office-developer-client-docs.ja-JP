---
title: GlueSettings 要素 (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a5675dea-3b78-9fc2-c1c0-51fefe45c6e3
description: 図面で接着が有効な場合に、図形が接着するオブジェクトを指定します。
ms.openlocfilehash: 6a876275fd604eab4b65a28386c052dcc5cac1cf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542220"
---
# <a name="gluesettings-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="5c93e-103">GlueSettings 要素 (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5c93e-103">GlueSettings element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="5c93e-104">図面で接着が有効な場合に、図形が接着するオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="5c93e-104">Specifies the objects that shapes glue to when glue is enabled in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c93e-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="5c93e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c93e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="5c93e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5c93e-107">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="5c93e-107">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5c93e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5c93e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5c93e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5c93e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5c93e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5c93e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5c93e-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="5c93e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5c93e-112">windows.xml、document.xml</span><span class="sxs-lookup"><span data-stu-id="5c93e-112">windows.xml, document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5c93e-113">定義</span><span class="sxs-lookup"><span data-stu-id="5c93e-113">Definition</span></span>

```XML
< xs:element name="GlueSettings" type="GlueSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5c93e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5c93e-114">Elements and attributes</span></span>

<span data-ttu-id="5c93e-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c93e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5c93e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="5c93e-116">Parent elements</span></span>

|<span data-ttu-id="5c93e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="5c93e-117">**Element**</span></span>|<span data-ttu-id="5c93e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="5c93e-118">**Type**</span></span>|<span data-ttu-id="5c93e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="5c93e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5c93e-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="5c93e-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5c93e-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="5c93e-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5c93e-122">ドキュメント設定を指定する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5c93e-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5c93e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="5c93e-123">Child elements</span></span>

<span data-ttu-id="5c93e-124">なし。</span><span class="sxs-lookup"><span data-stu-id="5c93e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c93e-125">属性</span><span class="sxs-lookup"><span data-stu-id="5c93e-125">Attributes</span></span>

<span data-ttu-id="5c93e-126">なし。</span><span class="sxs-lookup"><span data-stu-id="5c93e-126">None.</span></span>
  

