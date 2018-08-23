---
title: PidTagOriginallyIntendedRecipientName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipientName
api_type:
- COM
ms.assetid: 56c406fb-8778-4f85-bbdc-4cabfa140248
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7fae59d23d2d335513cbbddc22638ed623d894b7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583793"
---
# <a name="pidtagoriginallyintendedrecipientname-canonical-property"></a><span data-ttu-id="e7fc3-103">PidTagOriginallyIntendedRecipientName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e7fc3-103">PidTagOriginallyIntendedRecipientName Canonical Property</span></span>

  
  
<span data-ttu-id="e7fc3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7fc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7fc3-105">自動転送されたメッセージの受信者を元のエンコード済みの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e7fc3-105">Contains the encoded name of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7fc3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e7fc3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7fc3-107">PR_ORIGINALLY_INTENDED_RECIPIENT_NAME</span><span class="sxs-lookup"><span data-stu-id="e7fc3-107">PR_ORIGINALLY_INTENDED_RECIPIENT_NAME</span></span>  <br/> |
|<span data-ttu-id="e7fc3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e7fc3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e7fc3-109">0x0020</span><span class="sxs-lookup"><span data-stu-id="e7fc3-109">0x0020</span></span>  <br/> |
|<span data-ttu-id="e7fc3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e7fc3-110">Data type:</span></span>  <br/> |<span data-ttu-id="e7fc3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e7fc3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e7fc3-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e7fc3-112">Area:</span></span>  <br/> |<span data-ttu-id="e7fc3-113">Server</span><span class="sxs-lookup"><span data-stu-id="e7fc3-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7fc3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e7fc3-114">Remarks</span></span>

<span data-ttu-id="e7fc3-115">**PR_ORIGINALLY_INTENDED_RECIPIENT_NAME**プロパティは、メッセージを転送するには自動エージェントによって設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7fc3-115">The **PR_ORIGINALLY_INTENDED_RECIPIENT_NAME** property must be set by the automatic agent that has forwarded the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e7fc3-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e7fc3-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e7fc3-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e7fc3-117">Header files</span></span>

<span data-ttu-id="e7fc3-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7fc3-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7fc3-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e7fc3-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="e7fc3-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e7fc3-120">Mapitags.h</span></span>
  
> <span data-ttu-id="e7fc3-121">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e7fc3-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7fc3-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7fc3-122">See also</span></span>



[<span data-ttu-id="e7fc3-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e7fc3-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7fc3-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e7fc3-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7fc3-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e7fc3-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7fc3-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e7fc3-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

