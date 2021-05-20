---
title: AttachedToolbars 要素 (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cd7d8a06-5661-d515-f106-ff8275a04f40
description: カスタム ツールバーを表す MIME (Multipurpose Internet Mail Extensions) でエンコードされた Microsoft Visio (VSU) ファイル。
ms.openlocfilehash: 99bc85aff23abf11dafb644fb43ee540fff7a2ca
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537928"
---
# <a name="attachedtoolbars-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="afe2d-103">AttachedToolbars 要素 (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="afe2d-103">AttachedToolbars element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="afe2d-104">カスタム ツールバーを表す MIME (Multipurpose Internet Mail Extensions) でエンコードされた Microsoft Visio (VSU) ファイル。</span><span class="sxs-lookup"><span data-stu-id="afe2d-104">A MIME (Multipurpose Internet Mail Extensions) encoded Microsoft Visio user interface (VSU) file representing custom toolbars.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="afe2d-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="afe2d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afe2d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="afe2d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="afe2d-107">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="afe2d-107">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="afe2d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="afe2d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="afe2d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="afe2d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="afe2d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="afe2d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="afe2d-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="afe2d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="afe2d-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="afe2d-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="afe2d-113">定義</span><span class="sxs-lookup"><span data-stu-id="afe2d-113">Definition</span></span>

```XML
< xs:element name="AttachedToolbars" type="AttachedToolbars_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="afe2d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="afe2d-114">Elements and attributes</span></span>

<span data-ttu-id="afe2d-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="afe2d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="afe2d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="afe2d-116">Parent elements</span></span>

|<span data-ttu-id="afe2d-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="afe2d-117">**Element**</span></span>|<span data-ttu-id="afe2d-118">**型**</span><span class="sxs-lookup"><span data-stu-id="afe2d-118">**Type**</span></span>|<span data-ttu-id="afe2d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="afe2d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="afe2d-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="afe2d-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="afe2d-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="afe2d-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="afe2d-122">ドキュメント設定を指定する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="afe2d-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="afe2d-123">子要素</span><span class="sxs-lookup"><span data-stu-id="afe2d-123">Child elements</span></span>

<span data-ttu-id="afe2d-124">なし。</span><span class="sxs-lookup"><span data-stu-id="afe2d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="afe2d-125">属性</span><span class="sxs-lookup"><span data-stu-id="afe2d-125">Attributes</span></span>

<span data-ttu-id="afe2d-126">なし。</span><span class="sxs-lookup"><span data-stu-id="afe2d-126">None.</span></span>
  

