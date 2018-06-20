---
title: PidNameCrossReference の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameCrossReference
api_type:
- COM
ms.assetid: d16e1adf-c911-427e-9c98-678a303e6791
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 148d71dc0e99e23ffe10445068170617cb26b01b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802349"
---
# <a name="pidnamecrossreference-canonical-property"></a><span data-ttu-id="c4617-103">PidNameCrossReference の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="c4617-103">PidNameCrossReference Canonical Property</span></span>

  
  
<span data-ttu-id="c4617-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4617-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4617-105">[RFC3282] Xref ヘッダー フィールドの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c4617-105">Contains an [RFC3282] Xref header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4617-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="c4617-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="c4617-107">なし</span><span class="sxs-lookup"><span data-stu-id="c4617-107">None</span></span>  <br/> |
|<span data-ttu-id="c4617-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="c4617-108">Property set:</span></span>  <br/> |<span data-ttu-id="c4617-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="c4617-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="c4617-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="c4617-110">Property name:</span></span>  <br/> |<span data-ttu-id="c4617-111">相互参照</span><span class="sxs-lookup"><span data-stu-id="c4617-111">Xref</span></span>  <br/> |
|<span data-ttu-id="c4617-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="c4617-112">Data type:</span></span>  <br/> |<span data-ttu-id="c4617-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c4617-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c4617-114">領域:</span><span class="sxs-lookup"><span data-stu-id="c4617-114">Area:</span></span>  <br/> |<span data-ttu-id="c4617-115">Email</span><span class="sxs-lookup"><span data-stu-id="c4617-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4617-116">備考</span><span class="sxs-lookup"><span data-stu-id="c4617-116">Remarks</span></span>

<span data-ttu-id="c4617-117">このプロパティの値を設定するには、多目的インターネット メッセージの拡張機能 (MIME) クライアントは、相互参照のヘッダー フィールドに目的の値を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4617-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to an XRef header field.</span></span> <span data-ttu-id="c4617-118">MIME のリーダーは、このプロパティの値を相互参照のヘッダー フィールドの値をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4617-118">MIME readers must copy the value of an XRef header field to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c4617-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c4617-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4617-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c4617-120">Protocol specifications</span></span>

<span data-ttu-id="c4617-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4617-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4617-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c4617-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c4617-123">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4617-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4617-124">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="c4617-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4617-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c4617-125">Header files</span></span>

<span data-ttu-id="c4617-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4617-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4617-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c4617-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4617-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="c4617-128">See also</span></span>



[<span data-ttu-id="c4617-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4617-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4617-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4617-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4617-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="c4617-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4617-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="c4617-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

