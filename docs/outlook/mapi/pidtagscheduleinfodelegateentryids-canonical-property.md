---
title: PidTagScheduleInfoDelegateEntryIds 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateEntryIds
api_type:
- COM
ms.assetid: c178a4e4-6f4c-409c-9db3-f6338bd4f40f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b2adde7c5ecc75fda25b94d005fabfcd705d5d07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321295"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="8bb8d-103">PidTagScheduleInfoDelegateEntryIds 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8bb8d-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="8bb8d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bb8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bb8d-105">代理人の**entryids**を含みます。</span><span class="sxs-lookup"><span data-stu-id="8bb8d-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8bb8d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8bb8d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8bb8d-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="8bb8d-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="8bb8d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8bb8d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8bb8d-109">0x684 5</span><span class="sxs-lookup"><span data-stu-id="8bb8d-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="8bb8d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8bb8d-110">Data type:</span></span>  <br/> |<span data-ttu-id="8bb8d-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="8bb8d-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="8bb8d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8bb8d-112">Area:</span></span>  <br/> |<span data-ttu-id="8bb8d-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="8bb8d-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bb8d-114">解説</span><span class="sxs-lookup"><span data-stu-id="8bb8d-114">Remarks</span></span>

<span data-ttu-id="8bb8d-115">各エントリには、各代理人のアドレス帳エントリの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティの値が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb8d-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="8bb8d-116">このプロパティは、デリゲート情報オブジェクトで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb8d-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8bb8d-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8bb8d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8bb8d-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8bb8d-118">Protocol specifications</span></span>

<span data-ttu-id="8bb8d-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb8d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb8d-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8bb8d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8bb8d-121">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb8d-121">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb8d-122">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="8bb8d-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8bb8d-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="8bb8d-123">Header files</span></span>

<span data-ttu-id="8bb8d-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8bb8d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="8bb8d-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8bb8d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="8bb8d-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="8bb8d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="8bb8d-127">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8bb8d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8bb8d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="8bb8d-128">See also</span></span>



[<span data-ttu-id="8bb8d-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8bb8d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8bb8d-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8bb8d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8bb8d-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8bb8d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8bb8d-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8bb8d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

