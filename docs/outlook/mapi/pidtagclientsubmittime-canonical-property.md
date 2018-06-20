---
title: PidTagClientSubmitTime の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ccf4a6054ecc89e280f2f5cbc4c72b2a8a829055
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802541"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="99a1e-103">PidTagClientSubmitTime の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="99a1e-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="99a1e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99a1e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99a1e-105">メッセージの送信者にメッセージが送信されたときの日時が含まれています。</span><span class="sxs-lookup"><span data-stu-id="99a1e-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99a1e-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="99a1e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="99a1e-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="99a1e-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="99a1e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="99a1e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="99a1e-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="99a1e-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="99a1e-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="99a1e-110">Data type:</span></span>  <br/> |<span data-ttu-id="99a1e-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="99a1e-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="99a1e-112">領域:</span><span class="sxs-lookup"><span data-stu-id="99a1e-112">Area:</span></span>  <br/> |<span data-ttu-id="99a1e-113">メッセージの時刻</span><span class="sxs-lookup"><span data-stu-id="99a1e-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99a1e-114">備考</span><span class="sxs-lookup"><span data-stu-id="99a1e-114">Remarks</span></span>

<span data-ttu-id="99a1e-115">ストア プロバイダーは、クライアント アプリケーションが[IMessage::SubmitMessage](imessage-submitmessage.md)を呼び出したときに**PR_CLIENT_SUBMIT_TIME**を設定します。</span><span class="sxs-lookup"><span data-stu-id="99a1e-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="99a1e-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="99a1e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="99a1e-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="99a1e-117">Protocol specifications</span></span>

<span data-ttu-id="99a1e-118">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99a1e-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99a1e-119">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="99a1e-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="99a1e-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="99a1e-120">Header files</span></span>

<span data-ttu-id="99a1e-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99a1e-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="99a1e-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="99a1e-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="99a1e-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="99a1e-123">Mapitags.h</span></span>
  
> <span data-ttu-id="99a1e-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="99a1e-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99a1e-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="99a1e-125">See also</span></span>



[<span data-ttu-id="99a1e-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="99a1e-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="99a1e-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="99a1e-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="99a1e-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="99a1e-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="99a1e-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="99a1e-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

