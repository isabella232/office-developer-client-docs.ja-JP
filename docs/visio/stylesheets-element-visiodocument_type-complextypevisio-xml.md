---
title: スタイル シートの要素 (VisioDocument_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da26de4b-3e5b-326b-de46-e8c542b74f02
description: ドキュメントのスタイル シートの要素のコレクションが含まれています。
ms.openlocfilehash: fdecd1ee6a22b4ffb918ff39f3806cf18c56654b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806592"
---
# <a name="stylesheets-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="cb209-103">スタイル シートの要素 (VisioDocument_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="cb209-103">StyleSheets element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="cb209-104">ドキュメントのスタイル シートの要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb209-104">Contains a collection of StyleSheet elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb209-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="cb209-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb209-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="cb209-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cb209-107">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="cb209-107">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cb209-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="cb209-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cb209-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="cb209-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cb209-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cb209-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cb209-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="cb209-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cb209-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="cb209-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cb209-113">定義</span><span class="sxs-lookup"><span data-stu-id="cb209-113">Definition</span></span>

```XML
< xs:element name="StyleSheets" type="StyleSheets_Type" minOccurs="0" maxOccurs="1" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cb209-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="cb209-114">Elements and attributes</span></span>

<span data-ttu-id="cb209-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb209-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cb209-116">親要素</span><span class="sxs-lookup"><span data-stu-id="cb209-116">Parent elements</span></span>

|<span data-ttu-id="cb209-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="cb209-117">**Element**</span></span>|<span data-ttu-id="cb209-118">**型**</span><span class="sxs-lookup"><span data-stu-id="cb209-118">**Type**</span></span>|<span data-ttu-id="cb209-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb209-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cb209-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="cb209-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="cb209-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="cb209-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb209-122">Microsoft Visio ドキュメントのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="cb209-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cb209-123">子要素</span><span class="sxs-lookup"><span data-stu-id="cb209-123">Child elements</span></span>

|<span data-ttu-id="cb209-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="cb209-124">**Element**</span></span>|<span data-ttu-id="cb209-125">**型**</span><span class="sxs-lookup"><span data-stu-id="cb209-125">**Type**</span></span>|<span data-ttu-id="cb209-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb209-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cb209-127">スタイル シート</span><span class="sxs-lookup"><span data-stu-id="cb209-127">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb209-128">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="cb209-128">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb209-129">図面で定義されているスタイルを表します。</span><span class="sxs-lookup"><span data-stu-id="cb209-129">Represents a style defined in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="cb209-130">属性</span><span class="sxs-lookup"><span data-stu-id="cb209-130">Attributes</span></span>

<span data-ttu-id="cb209-131">なし。</span><span class="sxs-lookup"><span data-stu-id="cb209-131">None.</span></span>
  

