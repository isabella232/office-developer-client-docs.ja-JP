---
title: アイコン要素 (MasterShortcut_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 07d8ba86-8e35-d151-e6c1-150c37cc2acd
description: MasterShortcut 要素のドキュメントの MIME (多目的インターネット メール拡張機能) にエンコードされたバイナリ] アイコン (.ico 形式) を指定します。
ms.openlocfilehash: 46ca7c3f6ba733d31823f6b47f083c46dd941c14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805557"
---
# <a name="icon-element-mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="1b813-103">アイコン要素 (MasterShortcut_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="1b813-103">Icon element (MasterShortcut_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1b813-104">MasterShortcut 要素のドキュメントの MIME (多目的インターネット メール拡張機能) にエンコードされたバイナリ] アイコン (.ico 形式) を指定します。</span><span class="sxs-lookup"><span data-stu-id="1b813-104">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a MasterShortcut element in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b813-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="1b813-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b813-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="1b813-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1b813-107">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="1b813-107">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1b813-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="1b813-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1b813-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1b813-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1b813-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1b813-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1b813-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="1b813-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1b813-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="1b813-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1b813-113">定義</span><span class="sxs-lookup"><span data-stu-id="1b813-113">Definition</span></span>

```XML
< xs:element name="Icon" type="Icon_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1b813-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1b813-114">Elements and attributes</span></span>

<span data-ttu-id="1b813-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b813-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1b813-116">親要素</span><span class="sxs-lookup"><span data-stu-id="1b813-116">Parent elements</span></span>

|<span data-ttu-id="1b813-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="1b813-117">**Element**</span></span>|<span data-ttu-id="1b813-118">**型**</span><span class="sxs-lookup"><span data-stu-id="1b813-118">**Type**</span></span>|<span data-ttu-id="1b813-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="1b813-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1b813-120">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="1b813-120">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1b813-121">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="1b813-121">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1b813-122">未使用のマスター形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="1b813-122">Specifies an unused master format.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1b813-123">子要素</span><span class="sxs-lookup"><span data-stu-id="1b813-123">Child elements</span></span>

<span data-ttu-id="1b813-124">なし。</span><span class="sxs-lookup"><span data-stu-id="1b813-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b813-125">属性</span><span class="sxs-lookup"><span data-stu-id="1b813-125">Attributes</span></span>

<span data-ttu-id="1b813-126">なし。</span><span class="sxs-lookup"><span data-stu-id="1b813-126">None.</span></span>
  

