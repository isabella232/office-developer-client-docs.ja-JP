---
title: Icon 要素 (MasterShortcut_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 07d8ba86-8e35-d151-e6c1-150c37cc2acd
description: ドキュメントの MasterShortcut 要素の MIME (多目的インターネットメール内線) エンコードされたバイナリアイコン (.ico 形式) を指定します。
ms.openlocfilehash: 6d223da406dd914c84aafdd3d37846c1ab30bb4e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541499"
---
# <a name="icon-element-mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="b1386-103">Icon 要素 (MasterShortcut_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b1386-103">Icon element (MasterShortcut_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b1386-104">ドキュメントの MasterShortcut 要素の MIME (多目的インターネットメール内線) エンコードされたバイナリアイコン (.ico 形式) を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1386-104">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a MasterShortcut element in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1386-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="b1386-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1386-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="b1386-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b1386-107">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="b1386-107">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b1386-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b1386-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b1386-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b1386-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b1386-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="b1386-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b1386-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="b1386-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b1386-112">masters</span><span class="sxs-lookup"><span data-stu-id="b1386-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b1386-113">定義</span><span class="sxs-lookup"><span data-stu-id="b1386-113">Definition</span></span>

```XML
< xs:element name="Icon" type="Icon_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b1386-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b1386-114">Elements and attributes</span></span>

<span data-ttu-id="b1386-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b1386-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b1386-116">親要素</span><span class="sxs-lookup"><span data-stu-id="b1386-116">Parent elements</span></span>

|<span data-ttu-id="b1386-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="b1386-117">**Element**</span></span>|<span data-ttu-id="b1386-118">**型**</span><span class="sxs-lookup"><span data-stu-id="b1386-118">**Type**</span></span>|<span data-ttu-id="b1386-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="b1386-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b1386-120">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="b1386-120">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b1386-121">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="b1386-121">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b1386-122">未使用のマスター形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1386-122">Specifies an unused master format.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b1386-123">子要素</span><span class="sxs-lookup"><span data-stu-id="b1386-123">Child elements</span></span>

<span data-ttu-id="b1386-124">なし。</span><span class="sxs-lookup"><span data-stu-id="b1386-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1386-125">属性</span><span class="sxs-lookup"><span data-stu-id="b1386-125">Attributes</span></span>

<span data-ttu-id="b1386-126">なし。</span><span class="sxs-lookup"><span data-stu-id="b1386-126">None.</span></span>
  

