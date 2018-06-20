---
title: PidTagDeliverTime の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliverTime
api_type:
- HeaderDef
ms.assetid: da0ad17b-08ac-4c50-ac1d-13062b890dfd
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 40839e34a61b5e5fdd3d7b69d8c553d7e469cd22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802675"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="ed9a5-103">PidTagDeliverTime の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ed9a5-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="ed9a5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed9a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed9a5-105">元のメッセージが配信されたときの日時が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ed9a5-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed9a5-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="ed9a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed9a5-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="ed9a5-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="ed9a5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ed9a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed9a5-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="ed9a5-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="ed9a5-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="ed9a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed9a5-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ed9a5-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ed9a5-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ed9a5-112">Area:</span></span>  <br/> |<span data-ttu-id="ed9a5-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="ed9a5-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed9a5-114">備考</span><span class="sxs-lookup"><span data-stu-id="ed9a5-114">Remarks</span></span>

<span data-ttu-id="ed9a5-115">このプロパティは、元のメッセージが配信レポートを生成しているメッセージング ユーザーに配信された時刻を示す配信レポートの受信者ごとのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="ed9a5-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ed9a5-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ed9a5-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ed9a5-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ed9a5-117">Header files</span></span>

<span data-ttu-id="ed9a5-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed9a5-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed9a5-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed9a5-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed9a5-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ed9a5-120">Mapitags.h</span></span>
  
> <span data-ttu-id="ed9a5-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ed9a5-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed9a5-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed9a5-122">See also</span></span>



[<span data-ttu-id="ed9a5-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="ed9a5-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="ed9a5-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed9a5-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed9a5-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed9a5-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed9a5-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="ed9a5-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed9a5-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="ed9a5-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

