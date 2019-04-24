---
title: GlueSettings 要素 (DocumentSettings_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a5675dea-3b78-9fc2-c1c0-51fefe45c6e3
description: 図面で接着が有効になっている場合に、図形を接着するオブジェクトを指定します。
ms.openlocfilehash: c85f1b201a15f5edb7e3ddb0f21553d80b9dd17a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316472"
---
# <a name="gluesettings-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="1f0a4-103">GlueSettings 要素 (DocumentSettings_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1f0a4-103">GlueSettings element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1f0a4-104">図面で接着が有効になっている場合に、図形を接着するオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="1f0a4-104">Specifies the objects that shapes glue to when glue is enabled in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f0a4-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="1f0a4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f0a4-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="1f0a4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1f0a4-107">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="1f0a4-107">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1f0a4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1f0a4-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1f0a4-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1f0a4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1f0a4-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="1f0a4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1f0a4-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="1f0a4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1f0a4-112">windows .xml、document .xml</span><span class="sxs-lookup"><span data-stu-id="1f0a4-112">windows.xml, document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1f0a4-113">定義</span><span class="sxs-lookup"><span data-stu-id="1f0a4-113">Definition</span></span>

```XML
< xs:element name="GlueSettings" type="GlueSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1f0a4-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1f0a4-114">Elements and attributes</span></span>

<span data-ttu-id="1f0a4-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1f0a4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1f0a4-116">親要素</span><span class="sxs-lookup"><span data-stu-id="1f0a4-116">Parent elements</span></span>

|<span data-ttu-id="1f0a4-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="1f0a4-117">**Element**</span></span>|<span data-ttu-id="1f0a4-118">**型**</span><span class="sxs-lookup"><span data-stu-id="1f0a4-118">**Type**</span></span>|<span data-ttu-id="1f0a4-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="1f0a4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1f0a4-120">documentsettings</span><span class="sxs-lookup"><span data-stu-id="1f0a4-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f0a4-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="1f0a4-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1f0a4-122">ドキュメントの設定を指定する要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="1f0a4-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1f0a4-123">子要素</span><span class="sxs-lookup"><span data-stu-id="1f0a4-123">Child elements</span></span>

<span data-ttu-id="1f0a4-124">なし。</span><span class="sxs-lookup"><span data-stu-id="1f0a4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f0a4-125">属性</span><span class="sxs-lookup"><span data-stu-id="1f0a4-125">Attributes</span></span>

<span data-ttu-id="1f0a4-126">なし。</span><span class="sxs-lookup"><span data-stu-id="1f0a4-126">None.</span></span>
  

