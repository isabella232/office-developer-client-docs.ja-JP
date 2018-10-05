---
title: アイコン要素 (Master_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80061e7d-dbcb-f7a1-b63a-052eee4ec7d7
description: MIME (多目的インターネット メール拡張機能) マスターのバイナリのアイコン (.ico 形式でのエンコードを指定するドキュメント内の要素。
ms.openlocfilehash: 80d9089442318c834a9a211941187588359f7041
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395757"
---
# <a name="icon-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="a4831-103">アイコン要素 (Master_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a4831-103">Icon element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a4831-104">MIME (多目的インターネット メール拡張機能) マスターのバイナリのアイコン (.ico 形式でのエンコードを指定するドキュメント内の要素。</span><span class="sxs-lookup"><span data-stu-id="a4831-104">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a Master element in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4831-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="a4831-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4831-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a4831-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a4831-107">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="a4831-107">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a4831-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a4831-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a4831-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a4831-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a4831-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a4831-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a4831-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="a4831-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a4831-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="a4831-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a4831-113">定義</span><span class="sxs-lookup"><span data-stu-id="a4831-113">Definition</span></span>

```XML
< xs:element name="Icon" type="Icon_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a4831-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a4831-114">Elements and attributes</span></span>

<span data-ttu-id="a4831-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4831-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a4831-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a4831-116">Parent elements</span></span>

|<span data-ttu-id="a4831-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a4831-117">**Element**</span></span>|<span data-ttu-id="a4831-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a4831-118">**Type**</span></span>|<span data-ttu-id="a4831-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a4831-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a4831-120">Master</span><span class="sxs-lookup"><span data-stu-id="a4831-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a4831-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="a4831-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a4831-122">図面のマスター シェイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="a4831-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a4831-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a4831-123">Child elements</span></span>

<span data-ttu-id="a4831-124">なし。</span><span class="sxs-lookup"><span data-stu-id="a4831-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4831-125">属性</span><span class="sxs-lookup"><span data-stu-id="a4831-125">Attributes</span></span>

<span data-ttu-id="a4831-126">なし。</span><span class="sxs-lookup"><span data-stu-id="a4831-126">None.</span></span>
  

