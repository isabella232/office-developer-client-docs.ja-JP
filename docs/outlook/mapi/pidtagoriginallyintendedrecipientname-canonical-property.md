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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8637ef8036ccec79b82bcfff4a9f6d21fd5c2e11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419843"
---
# <a name="pidtagoriginallyintendedrecipientname-canonical-property"></a><span data-ttu-id="43437-103">PidTagOriginallyIntendedRecipientName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="43437-103">PidTagOriginallyIntendedRecipientName Canonical Property</span></span>

  
  
<span data-ttu-id="43437-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43437-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43437-105">自動送信されたメッセージの最初に意図された受信者のエンコードされた名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="43437-105">Contains the encoded name of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43437-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="43437-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43437-107">PR_ORIGINALLY_INTENDED_RECIPIENT_NAME</span><span class="sxs-lookup"><span data-stu-id="43437-107">PR_ORIGINALLY_INTENDED_RECIPIENT_NAME</span></span>  <br/> |
|<span data-ttu-id="43437-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="43437-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43437-109">0x0020</span><span class="sxs-lookup"><span data-stu-id="43437-109">0x0020</span></span>  <br/> |
|<span data-ttu-id="43437-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="43437-110">Data type:</span></span>  <br/> |<span data-ttu-id="43437-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="43437-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="43437-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="43437-112">Area:</span></span>  <br/> |<span data-ttu-id="43437-113">Server</span><span class="sxs-lookup"><span data-stu-id="43437-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43437-114">注釈</span><span class="sxs-lookup"><span data-stu-id="43437-114">Remarks</span></span>

<span data-ttu-id="43437-115">PR_ORIGINALLY_INTENDED_RECIPIENT_NAME **プロパティ** は、メッセージを転送した自動エージェントによって設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43437-115">The **PR_ORIGINALLY_INTENDED_RECIPIENT_NAME** property must be set by the automatic agent that has forwarded the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="43437-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="43437-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="43437-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="43437-117">Header files</span></span>

<span data-ttu-id="43437-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43437-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="43437-119">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="43437-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="43437-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="43437-120">Mapitags.h</span></span>
  
> <span data-ttu-id="43437-121">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="43437-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43437-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="43437-122">See also</span></span>



[<span data-ttu-id="43437-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="43437-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43437-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="43437-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43437-125">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="43437-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43437-126">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="43437-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

