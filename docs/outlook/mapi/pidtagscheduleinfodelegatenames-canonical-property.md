---
title: PidTagScheduleInfoDelegateNames 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateNames
api_type:
- COM
ms.assetid: 592d9c78-4487-4c68-8ae7-4cd3d6265685
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a257934411bb11a30378ee46317d323156f53e31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314939"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a><span data-ttu-id="6620f-103">PidTagScheduleInfoDelegateNames 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6620f-103">PidTagScheduleInfoDelegateNames Canonical Property</span></span>

  
  
<span data-ttu-id="6620f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6620f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6620f-105">代理人の名前を含みます。</span><span class="sxs-lookup"><span data-stu-id="6620f-105">Contains the names of the delegates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6620f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6620f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6620f-107">PR_SCHDINFO_DELEGATE_NAMES、PR_SCHDINFO_DELEGATE_NAMES_A、PR_SCHDINFO_DELEGATE_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="6620f-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="6620f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6620f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6620f-109">0x684 4</span><span class="sxs-lookup"><span data-stu-id="6620f-109">0x6844</span></span>  <br/> |
|<span data-ttu-id="6620f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6620f-110">Data type:</span></span>  <br/> |<span data-ttu-id="6620f-111">PT_MV_STRING8、PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6620f-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6620f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="6620f-112">Area:</span></span>  <br/> |<span data-ttu-id="6620f-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="6620f-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6620f-114">解説</span><span class="sxs-lookup"><span data-stu-id="6620f-114">Remarks</span></span>

<span data-ttu-id="6620f-115">これらのプロパティの各エントリには、各代理人のアドレス帳の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6620f-115">Each entry in these properties must contain the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each delegate's address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6620f-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6620f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6620f-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6620f-117">Protocol specifications</span></span>

<span data-ttu-id="6620f-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6620f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6620f-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6620f-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6620f-120">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6620f-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6620f-121">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="6620f-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6620f-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="6620f-122">Header files</span></span>

<span data-ttu-id="6620f-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6620f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6620f-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6620f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6620f-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="6620f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="6620f-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6620f-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6620f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="6620f-127">See also</span></span>



[<span data-ttu-id="6620f-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6620f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6620f-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6620f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6620f-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6620f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6620f-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6620f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

