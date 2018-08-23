---
title: AttachedToolbars 要素 (DocumentSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cd7d8a06-5661-d515-f106-ff8275a04f40
description: MIME (多目的インターネット メール拡張機能) では、Microsoft Visio ユーザー インターフェイス (VSU) ファイルをユーザー設定のツールバーを表すエンコードされています。
ms.openlocfilehash: c62cc334d8a0c4142c8a47d5dc8aab16a755ceb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804817"
---
# <a name="attachedtoolbars-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="633e8-103">AttachedToolbars 要素 (DocumentSettings_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="633e8-103">AttachedToolbars element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="633e8-104">MIME (多目的インターネット メール拡張機能) では、Microsoft Visio ユーザー インターフェイス (VSU) ファイルをユーザー設定のツールバーを表すエンコードされています。</span><span class="sxs-lookup"><span data-stu-id="633e8-104">A MIME (Multipurpose Internet Mail Extensions) encoded Microsoft Visio user interface (VSU) file representing custom toolbars.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="633e8-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="633e8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="633e8-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="633e8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="633e8-107">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="633e8-107">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="633e8-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="633e8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="633e8-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="633e8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="633e8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="633e8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="633e8-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="633e8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="633e8-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="633e8-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="633e8-113">定義</span><span class="sxs-lookup"><span data-stu-id="633e8-113">Definition</span></span>

```XML
< xs:element name="AttachedToolbars" type="AttachedToolbars_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="633e8-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="633e8-114">Elements and attributes</span></span>

<span data-ttu-id="633e8-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="633e8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="633e8-116">親要素</span><span class="sxs-lookup"><span data-stu-id="633e8-116">Parent elements</span></span>

|<span data-ttu-id="633e8-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="633e8-117">**Element**</span></span>|<span data-ttu-id="633e8-118">**型**</span><span class="sxs-lookup"><span data-stu-id="633e8-118">**Type**</span></span>|<span data-ttu-id="633e8-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="633e8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="633e8-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="633e8-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="633e8-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="633e8-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="633e8-122">ドキュメントの設定を指定する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="633e8-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="633e8-123">子要素</span><span class="sxs-lookup"><span data-stu-id="633e8-123">Child elements</span></span>

<span data-ttu-id="633e8-124">なし。</span><span class="sxs-lookup"><span data-stu-id="633e8-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="633e8-125">属性</span><span class="sxs-lookup"><span data-stu-id="633e8-125">Attributes</span></span>

<span data-ttu-id="633e8-126">なし。</span><span class="sxs-lookup"><span data-stu-id="633e8-126">None.</span></span>
  

