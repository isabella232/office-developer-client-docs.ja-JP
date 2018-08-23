---
title: GlueSettings 要素 (DocumentSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a5675dea-3b78-9fc2-c1c0-51fefe45c6e3
description: ドキュメントで接着が有効になっているときに図形が接着するオブジェクトを指定します。
ms.openlocfilehash: 0341e3e405c42707c802d1f193d341c8f125c159
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805491"
---
# <a name="gluesettings-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="6cac4-103">GlueSettings 要素 (DocumentSettings_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="6cac4-103">GlueSettings element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6cac4-104">ドキュメントで接着が有効になっているときに図形が接着するオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="6cac4-104">Specifies the objects that shapes glue to when glue is enabled in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6cac4-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="6cac4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6cac4-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="6cac4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6cac4-107">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="6cac4-107">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6cac4-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="6cac4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6cac4-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6cac4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6cac4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6cac4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6cac4-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="6cac4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6cac4-112">windows.xml、document.xml</span><span class="sxs-lookup"><span data-stu-id="6cac4-112">windows.xml, document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6cac4-113">定義</span><span class="sxs-lookup"><span data-stu-id="6cac4-113">Definition</span></span>

```XML
< xs:element name="GlueSettings" type="GlueSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6cac4-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6cac4-114">Elements and attributes</span></span>

<span data-ttu-id="6cac4-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cac4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6cac4-116">親要素</span><span class="sxs-lookup"><span data-stu-id="6cac4-116">Parent elements</span></span>

|<span data-ttu-id="6cac4-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="6cac4-117">**Element**</span></span>|<span data-ttu-id="6cac4-118">**型**</span><span class="sxs-lookup"><span data-stu-id="6cac4-118">**Type**</span></span>|<span data-ttu-id="6cac4-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="6cac4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6cac4-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="6cac4-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6cac4-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="6cac4-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6cac4-122">ドキュメントの設定を指定する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6cac4-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6cac4-123">子要素</span><span class="sxs-lookup"><span data-stu-id="6cac4-123">Child elements</span></span>

<span data-ttu-id="6cac4-124">なし。</span><span class="sxs-lookup"><span data-stu-id="6cac4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6cac4-125">属性</span><span class="sxs-lookup"><span data-stu-id="6cac4-125">Attributes</span></span>

<span data-ttu-id="6cac4-126">なし。</span><span class="sxs-lookup"><span data-stu-id="6cac4-126">None.</span></span>
  

