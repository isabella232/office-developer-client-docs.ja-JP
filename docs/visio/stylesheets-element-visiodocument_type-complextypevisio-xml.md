---
title: StyleSheets 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da26de4b-3e5b-326b-de46-e8c542b74f02
description: ドキュメントの StyleSheet 要素のコレクションを格納します。
ms.openlocfilehash: 363cb102fb545ffd20601bf0125c22aeb06defa8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541989"
---
# <a name="stylesheets-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="0337c-103">StyleSheets 要素 (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0337c-103">StyleSheets element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="0337c-104">ドキュメントの StyleSheet 要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="0337c-104">Contains a collection of StyleSheet elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0337c-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="0337c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0337c-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="0337c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0337c-107">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="0337c-107">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0337c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0337c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0337c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0337c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0337c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0337c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0337c-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="0337c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0337c-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="0337c-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0337c-113">定義</span><span class="sxs-lookup"><span data-stu-id="0337c-113">Definition</span></span>

```XML
< xs:element name="StyleSheets" type="StyleSheets_Type" minOccurs="0" maxOccurs="1" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0337c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0337c-114">Elements and attributes</span></span>

<span data-ttu-id="0337c-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0337c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0337c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="0337c-116">Parent elements</span></span>

|<span data-ttu-id="0337c-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="0337c-117">**Element**</span></span>|<span data-ttu-id="0337c-118">**型**</span><span class="sxs-lookup"><span data-stu-id="0337c-118">**Type**</span></span>|<span data-ttu-id="0337c-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="0337c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0337c-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="0337c-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="0337c-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="0337c-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0337c-122">Microsoft ドキュメントのルートVisioです。</span><span class="sxs-lookup"><span data-stu-id="0337c-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0337c-123">子要素</span><span class="sxs-lookup"><span data-stu-id="0337c-123">Child elements</span></span>

|<span data-ttu-id="0337c-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0337c-124">**Element**</span></span>|<span data-ttu-id="0337c-125">**型**</span><span class="sxs-lookup"><span data-stu-id="0337c-125">**Type**</span></span>|<span data-ttu-id="0337c-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="0337c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0337c-127">StyleSheet</span><span class="sxs-lookup"><span data-stu-id="0337c-127">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0337c-128">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="0337c-128">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0337c-129">図面で定義されているスタイルを表します。</span><span class="sxs-lookup"><span data-stu-id="0337c-129">Represents a style defined in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0337c-130">属性</span><span class="sxs-lookup"><span data-stu-id="0337c-130">Attributes</span></span>

<span data-ttu-id="0337c-131">なし。</span><span class="sxs-lookup"><span data-stu-id="0337c-131">None.</span></span>
  

