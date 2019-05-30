---
title: Icon 要素 (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80061e7d-dbcb-f7a1-b63a-052eee4ec7d7
description: ドキュメントのマスター要素に対して、MIME (多目的インターネットメール内線) のエンコードされたバイナリアイコン (.ico 形式) を指定します。
ms.openlocfilehash: fb66e79348b6fba5d5dfd163e6165e7c1bfddfcd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537746"
---
# <a name="icon-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="fd62a-103">Icon 要素 (Master_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fd62a-103">Icon element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="fd62a-104">ドキュメントのマスター要素に対して、MIME (多目的インターネットメール内線) のエンコードされたバイナリアイコン (.ico 形式) を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd62a-104">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a Master element in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd62a-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="fd62a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd62a-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="fd62a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fd62a-107">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="fd62a-107">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fd62a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fd62a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fd62a-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="fd62a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fd62a-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="fd62a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fd62a-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="fd62a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fd62a-112">masters</span><span class="sxs-lookup"><span data-stu-id="fd62a-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fd62a-113">定義</span><span class="sxs-lookup"><span data-stu-id="fd62a-113">Definition</span></span>

```XML
< xs:element name="Icon" type="Icon_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fd62a-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="fd62a-114">Elements and attributes</span></span>

<span data-ttu-id="fd62a-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd62a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fd62a-116">親要素</span><span class="sxs-lookup"><span data-stu-id="fd62a-116">Parent elements</span></span>

|<span data-ttu-id="fd62a-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="fd62a-117">**Element**</span></span>|<span data-ttu-id="fd62a-118">**型**</span><span class="sxs-lookup"><span data-stu-id="fd62a-118">**Type**</span></span>|<span data-ttu-id="fd62a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="fd62a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fd62a-120">Master</span><span class="sxs-lookup"><span data-stu-id="fd62a-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fd62a-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="fd62a-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fd62a-122">図面のマスターシェイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="fd62a-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fd62a-123">子要素</span><span class="sxs-lookup"><span data-stu-id="fd62a-123">Child elements</span></span>

<span data-ttu-id="fd62a-124">なし。</span><span class="sxs-lookup"><span data-stu-id="fd62a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd62a-125">属性</span><span class="sxs-lookup"><span data-stu-id="fd62a-125">Attributes</span></span>

<span data-ttu-id="fd62a-126">なし。</span><span class="sxs-lookup"><span data-stu-id="fd62a-126">None.</span></span>
  

