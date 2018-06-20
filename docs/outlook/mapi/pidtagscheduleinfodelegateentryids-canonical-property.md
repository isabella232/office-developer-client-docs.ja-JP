---
title: PidTagScheduleInfoDelegateEntryIds の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8ea60fb989cd85b23e6dd9302bc03a9b5befd20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803453"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="9117d-103">PidTagScheduleInfoDelegateEntryIds の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="9117d-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="9117d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9117d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9117d-105">デリゲートの**エントリ Id**が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9117d-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9117d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="9117d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9117d-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="9117d-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="9117d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9117d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9117d-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="9117d-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="9117d-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="9117d-110">Data type:</span></span>  <br/> |<span data-ttu-id="9117d-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="9117d-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="9117d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="9117d-112">Area:</span></span>  <br/> |<span data-ttu-id="9117d-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="9117d-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9117d-114">備考</span><span class="sxs-lookup"><span data-stu-id="9117d-114">Remarks</span></span>

<span data-ttu-id="9117d-115">各エントリには、各デリゲートのアドレス帳のエントリの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティの値を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="9117d-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="9117d-116">代理人の情報オブジェクトにこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9117d-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9117d-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9117d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9117d-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9117d-118">Protocol specifications</span></span>

<span data-ttu-id="9117d-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9117d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9117d-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9117d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9117d-121">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9117d-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9117d-122">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="9117d-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9117d-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9117d-123">Header files</span></span>

<span data-ttu-id="9117d-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9117d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9117d-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9117d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9117d-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9117d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9117d-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9117d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9117d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9117d-128">See also</span></span>



[<span data-ttu-id="9117d-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9117d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9117d-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9117d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9117d-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="9117d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9117d-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="9117d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

