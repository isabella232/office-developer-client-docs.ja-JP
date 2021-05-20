---
title: PidTagOriginatorRequestedAlternateRecipient 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 45cd0e8a95f908d7ef56d03b3ecab5d5df5bcae1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437862"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="b6ba6-103">PidTagOriginatorRequestedAlternateRecipient 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b6ba6-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="b6ba6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6ba6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6ba6-105">送信者が指定した別の受信者のエントリ識別子を含む。</span><span class="sxs-lookup"><span data-stu-id="b6ba6-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6ba6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b6ba6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6ba6-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="b6ba6-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="b6ba6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b6ba6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6ba6-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="b6ba6-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="b6ba6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b6ba6-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6ba6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b6ba6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b6ba6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b6ba6-112">Area:</span></span>  <br/> |<span data-ttu-id="b6ba6-113">MIME</span><span class="sxs-lookup"><span data-stu-id="b6ba6-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6ba6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b6ba6-114">Remarks</span></span>

<span data-ttu-id="b6ba6-115">このプロパティは、自動送信メッセージで使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6ba6-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="b6ba6-116">自動フォワードが許可されていない場合、または別の受信者が指定されていない場合は、配信以外のレポートを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6ba6-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b6ba6-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b6ba6-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b6ba6-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b6ba6-118">Header files</span></span>

<span data-ttu-id="b6ba6-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6ba6-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6ba6-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b6ba6-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6ba6-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b6ba6-121">Mapitags.h</span></span>
  
> <span data-ttu-id="b6ba6-122">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="b6ba6-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6ba6-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6ba6-123">See also</span></span>



[<span data-ttu-id="b6ba6-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b6ba6-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6ba6-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b6ba6-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6ba6-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b6ba6-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6ba6-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b6ba6-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

