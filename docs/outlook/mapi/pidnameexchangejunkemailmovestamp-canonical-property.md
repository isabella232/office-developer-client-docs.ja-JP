---
title: PidNameExchangeJunkEmailMoveStamp 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameExchangeJunkEmailMoveStamp
api_type:
- COM
ms.assetid: 7a52f46c-371c-46d0-8d66-e154482e8269
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 07acfd8715dccad8833ee14ac8e573fb995539ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399705"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a><span data-ttu-id="4f5d8-103">PidNameExchangeJunkEmailMoveStamp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f5d8-103">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>

  
  
<span data-ttu-id="4f5d8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f5d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f5d8-105">メッセージ必要があるために処理できませんスパム フィルターによってメッセージが既に処理されたか、安全にされたことを示すメッセージが永続化された値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4f5d8-105">Contains the persisted message value that indicates that the message should not be processed by a spam filter because the message was either already processed or is safe.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f5d8-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="4f5d8-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="4f5d8-107">なし</span><span class="sxs-lookup"><span data-stu-id="4f5d8-107">None</span></span>  <br/> |
|<span data-ttu-id="4f5d8-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4f5d8-108">Property set:</span></span>  <br/> |<span data-ttu-id="4f5d8-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="4f5d8-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="4f5d8-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="4f5d8-110">Property name:</span></span>  <br/> |https://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|<span data-ttu-id="4f5d8-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4f5d8-111">Data type:</span></span>  <br/> |<span data-ttu-id="4f5d8-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4f5d8-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4f5d8-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="4f5d8-113">Area:</span></span>  <br/> |<span data-ttu-id="4f5d8-114">メッセージのセキュリティ保護します。</span><span class="sxs-lookup"><span data-stu-id="4f5d8-114">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f5d8-115">備考</span><span class="sxs-lookup"><span data-stu-id="4f5d8-115">Remarks</span></span>

<span data-ttu-id="4f5d8-116">このプロパティがスタンプ迷惑メール ルールを移動するか、それ以外の場合は、すべてのメッセージには、コンテンツが信頼されています。</span><span class="sxs-lookup"><span data-stu-id="4f5d8-116">This property is stamped on every message that is moved by the Junk E-Mail Rule or is otherwise trusted content.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4f5d8-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4f5d8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f5d8-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4f5d8-118">Protocol specifications</span></span>

<span data-ttu-id="4f5d8-119">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f5d8-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f5d8-120">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f5d8-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4f5d8-121">[[MS OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f5d8-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f5d8-122">許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。</span><span class="sxs-lookup"><span data-stu-id="4f5d8-122">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="4f5d8-123">[[MS OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f5d8-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f5d8-124">RSS 項目を表すための操作のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="4f5d8-124">Specifies the properties and operations that represent RSS items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4f5d8-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4f5d8-125">Header files</span></span>

<span data-ttu-id="4f5d8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f5d8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f5d8-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f5d8-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f5d8-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f5d8-128">See also</span></span>



[<span data-ttu-id="4f5d8-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f5d8-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f5d8-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f5d8-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f5d8-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4f5d8-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f5d8-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4f5d8-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

