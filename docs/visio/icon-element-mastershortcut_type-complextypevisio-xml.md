---
title: Icon 要素 (MasterShortcut_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 07d8ba86-8e35-d151-e6c1-150c37cc2acd
description: ドキュメント内の MasterShortcut 要素の MIME (多目的インターネット メール拡張機能) エンコードされたバイナリ アイコン (.ico 形式) を指定します。
ms.openlocfilehash: 6d223da406dd914c84aafdd3d37846c1ab30bb4e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541499"
---
# <a name="icon-element-mastershortcut_type-complextype-visio-xml"></a><span data-ttu-id="65cac-103">Icon 要素 (MasterShortcut_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="65cac-103">Icon element (MasterShortcut_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="65cac-104">ドキュメント内の MasterShortcut 要素の MIME (多目的インターネット メール拡張機能) エンコードされたバイナリ アイコン (.ico 形式) を指定します。</span><span class="sxs-lookup"><span data-stu-id="65cac-104">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a MasterShortcut element in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65cac-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="65cac-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65cac-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="65cac-106">**Element type**</span></span> <br/> |[<span data-ttu-id="65cac-107">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="65cac-107">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="65cac-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="65cac-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="65cac-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="65cac-109">**Schema file**</span></span> <br/> |<span data-ttu-id="65cac-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="65cac-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="65cac-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="65cac-111">**Document parts**</span></span> <br/> |<span data-ttu-id="65cac-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="65cac-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="65cac-113">定義</span><span class="sxs-lookup"><span data-stu-id="65cac-113">Definition</span></span>

```XML
< xs:element name="Icon" type="Icon_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="65cac-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="65cac-114">Elements and attributes</span></span>

<span data-ttu-id="65cac-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="65cac-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="65cac-116">親要素</span><span class="sxs-lookup"><span data-stu-id="65cac-116">Parent elements</span></span>

|<span data-ttu-id="65cac-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="65cac-117">**Element**</span></span>|<span data-ttu-id="65cac-118">**型**</span><span class="sxs-lookup"><span data-stu-id="65cac-118">**Type**</span></span>|<span data-ttu-id="65cac-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="65cac-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65cac-120">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="65cac-120">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65cac-121">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="65cac-121">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65cac-122">未使用のマスター形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="65cac-122">Specifies an unused master format.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="65cac-123">子要素</span><span class="sxs-lookup"><span data-stu-id="65cac-123">Child elements</span></span>

<span data-ttu-id="65cac-124">なし。</span><span class="sxs-lookup"><span data-stu-id="65cac-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65cac-125">属性</span><span class="sxs-lookup"><span data-stu-id="65cac-125">Attributes</span></span>

<span data-ttu-id="65cac-126">なし。</span><span class="sxs-lookup"><span data-stu-id="65cac-126">None.</span></span>
  

