---
title: PidLidSharingResponseTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseTime
api_type:
- COM
ms.assetid: 5cf0cf25-d302-44a4-bee8-53f5cff62647
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 473c7898fec46e55e68b199e9738949c9c231a6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331158"
---
# <a name="pidlidsharingresponsetime-canonical-property"></a><span data-ttu-id="5fd42-103">PidLidSharingResponseTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5fd42-103">PidLidSharingResponseTime Canonical Property</span></span>

  
  
<span data-ttu-id="5fd42-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fd42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fd42-105">共有要求の受信者が共有応答を送信した時刻を指定します。</span><span class="sxs-lookup"><span data-stu-id="5fd42-105">Specifies the time at which the recipient of the sharing request sent a sharing response.</span></span> <span data-ttu-id="5fd42-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="5fd42-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5fd42-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5fd42-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="5fd42-108">dispidSharingResponseTime</span><span class="sxs-lookup"><span data-stu-id="5fd42-108">dispidSharingResponseTime</span></span>  <br/> |
|<span data-ttu-id="5fd42-109">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="5fd42-109">Property set:</span></span>  <br/> |<span data-ttu-id="5fd42-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="5fd42-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="5fd42-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5fd42-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5fd42-112">0x00008A28</span><span class="sxs-lookup"><span data-stu-id="5fd42-112">0x00008A28</span></span>  <br/> |
|<span data-ttu-id="5fd42-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5fd42-113">Data type:</span></span>  <br/> |<span data-ttu-id="5fd42-114">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5fd42-114">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5fd42-115">エリア:</span><span class="sxs-lookup"><span data-stu-id="5fd42-115">Area:</span></span>  <br/> |<span data-ttu-id="5fd42-116">共有</span><span class="sxs-lookup"><span data-stu-id="5fd42-116">Sharing</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5fd42-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5fd42-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5fd42-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5fd42-118">Protocol specifications</span></span>

<span data-ttu-id="5fd42-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fd42-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fd42-120">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="5fd42-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5fd42-121">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fd42-121">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fd42-122">クライアント間でメールボックス フォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="5fd42-122">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5fd42-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5fd42-123">Header files</span></span>

<span data-ttu-id="5fd42-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5fd42-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="5fd42-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5fd42-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5fd42-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="5fd42-126">See also</span></span>



[<span data-ttu-id="5fd42-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5fd42-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5fd42-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5fd42-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5fd42-129">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5fd42-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5fd42-130">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5fd42-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

