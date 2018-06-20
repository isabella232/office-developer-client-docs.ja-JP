---
title: PidTagScheduleInfoDelegateNames の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fed2b23680cd2654bbb6960e3c6be07074307a98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803446"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a><span data-ttu-id="aea67-103">PidTagScheduleInfoDelegateNames の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="aea67-103">PidTagScheduleInfoDelegateNames Canonical Property</span></span>

  
  
<span data-ttu-id="aea67-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aea67-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aea67-105">代理人の名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="aea67-105">Contains the names of the delegates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aea67-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="aea67-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aea67-107">PR_SCHDINFO_DELEGATE_NAMES、PR_SCHDINFO_DELEGATE_NAMES_A、PR_SCHDINFO_DELEGATE_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="aea67-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="aea67-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="aea67-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aea67-109">0x6844</span><span class="sxs-lookup"><span data-stu-id="aea67-109">0x6844</span></span>  <br/> |
|<span data-ttu-id="aea67-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="aea67-110">Data type:</span></span>  <br/> |<span data-ttu-id="aea67-111">PT_MV_STRING8、PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aea67-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="aea67-112">領域:</span><span class="sxs-lookup"><span data-stu-id="aea67-112">Area:</span></span>  <br/> |<span data-ttu-id="aea67-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="aea67-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aea67-114">備考</span><span class="sxs-lookup"><span data-stu-id="aea67-114">Remarks</span></span>

<span data-ttu-id="aea67-115">これらのプロパティ内の各エントリには、各デリゲートのアドレス帳の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="aea67-115">Each entry in these properties must contain the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each delegate's address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aea67-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="aea67-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aea67-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="aea67-117">Protocol specifications</span></span>

<span data-ttu-id="aea67-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aea67-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aea67-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="aea67-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aea67-120">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aea67-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aea67-121">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="aea67-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aea67-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="aea67-122">Header files</span></span>

<span data-ttu-id="aea67-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aea67-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="aea67-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="aea67-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="aea67-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aea67-125">Mapitags.h</span></span>
  
> <span data-ttu-id="aea67-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="aea67-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aea67-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="aea67-127">See also</span></span>



[<span data-ttu-id="aea67-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="aea67-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aea67-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="aea67-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aea67-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="aea67-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aea67-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="aea67-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

