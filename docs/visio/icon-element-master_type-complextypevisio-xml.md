---
title: アイコン要素 (Master_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80061e7d-dbcb-f7a1-b63a-052eee4ec7d7
description: MIME (多目的インターネット メール拡張機能) マスターのバイナリのアイコン (.ico 形式でのエンコードを指定するドキュメント内の要素。
ms.openlocfilehash: 0c3d13db9c0f712067619e953441f2ebdfadf4c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805576"
---
# <a name="icon-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="e41db-103">アイコン要素 (Master_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="e41db-103">Icon element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e41db-104">MIME (多目的インターネット メール拡張機能) マスターのバイナリのアイコン (.ico 形式でのエンコードを指定するドキュメント内の要素。</span><span class="sxs-lookup"><span data-stu-id="e41db-104">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a Master element in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e41db-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="e41db-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e41db-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="e41db-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e41db-107">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="e41db-107">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e41db-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="e41db-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e41db-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e41db-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e41db-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e41db-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e41db-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="e41db-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e41db-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="e41db-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e41db-113">定義</span><span class="sxs-lookup"><span data-stu-id="e41db-113">Definition</span></span>

```XML
< xs:element name="Icon" type="Icon_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e41db-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e41db-114">Elements and attributes</span></span>

<span data-ttu-id="e41db-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e41db-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e41db-116">親要素</span><span class="sxs-lookup"><span data-stu-id="e41db-116">Parent elements</span></span>

|<span data-ttu-id="e41db-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="e41db-117">**Element**</span></span>|<span data-ttu-id="e41db-118">**型**</span><span class="sxs-lookup"><span data-stu-id="e41db-118">**Type**</span></span>|<span data-ttu-id="e41db-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="e41db-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e41db-120">Master</span><span class="sxs-lookup"><span data-stu-id="e41db-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e41db-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="e41db-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e41db-122">図面のマスター シェイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="e41db-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e41db-123">子要素</span><span class="sxs-lookup"><span data-stu-id="e41db-123">Child elements</span></span>

<span data-ttu-id="e41db-124">なし。</span><span class="sxs-lookup"><span data-stu-id="e41db-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e41db-125">属性</span><span class="sxs-lookup"><span data-stu-id="e41db-125">Attributes</span></span>

<span data-ttu-id="e41db-126">なし。</span><span class="sxs-lookup"><span data-stu-id="e41db-126">None.</span></span>
  

