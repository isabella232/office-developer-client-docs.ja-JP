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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 098261cd71631e4816d22272e1b1bef1d5932a94
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540946"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a><span data-ttu-id="ab8a9-103">PidNameExchangeJunkEmailMoveStamp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ab8a9-103">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>

  
  
<span data-ttu-id="ab8a9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab8a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab8a9-105">メッセージが既に処理されているか、または安全なので、メッセージがスパムフィルターによって処理されないことを示す永続的なメッセージ値が格納されています。</span><span class="sxs-lookup"><span data-stu-id="ab8a9-105">Contains the persisted message value that indicates that the message should not be processed by a spam filter because the message was either already processed or is safe.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ab8a9-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="ab8a9-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="ab8a9-107">None</span><span class="sxs-lookup"><span data-stu-id="ab8a9-107">None</span></span>  <br/> |
|<span data-ttu-id="ab8a9-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="ab8a9-108">Property set:</span></span>  <br/> |<span data-ttu-id="ab8a9-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="ab8a9-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="ab8a9-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="ab8a9-110">Property name:</span></span>  <br/> |http://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|<span data-ttu-id="ab8a9-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ab8a9-111">Data type:</span></span>  <br/> |<span data-ttu-id="ab8a9-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ab8a9-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ab8a9-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="ab8a9-113">Area:</span></span>  <br/> |<span data-ttu-id="ab8a9-114">セキュリティで保護されたメッセージング</span><span class="sxs-lookup"><span data-stu-id="ab8a9-114">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab8a9-115">注釈</span><span class="sxs-lookup"><span data-stu-id="ab8a9-115">Remarks</span></span>

<span data-ttu-id="ab8a9-116">このプロパティは、迷惑メールルールによって移動されるすべてのメッセージ、または信頼できるコンテンツとしてスタンプされます。</span><span class="sxs-lookup"><span data-stu-id="ab8a9-116">This property is stamped on every message that is moved by the Junk E-Mail Rule or is otherwise trusted content.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ab8a9-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ab8a9-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab8a9-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ab8a9-118">Protocol specifications</span></span>

<span data-ttu-id="ab8a9-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab8a9-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab8a9-120">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ab8a9-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ab8a9-121">[[OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab8a9-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab8a9-122">許可/ブロックリストの処理と、迷惑メールメッセージの決定を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ab8a9-122">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="ab8a9-123">[[OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab8a9-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab8a9-124">RSS アイテムを表すプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ab8a9-124">Specifies the properties and operations that represent RSS items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab8a9-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="ab8a9-125">Header files</span></span>

<span data-ttu-id="ab8a9-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab8a9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab8a9-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ab8a9-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab8a9-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab8a9-128">See also</span></span>



[<span data-ttu-id="ab8a9-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ab8a9-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab8a9-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ab8a9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab8a9-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ab8a9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab8a9-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ab8a9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

