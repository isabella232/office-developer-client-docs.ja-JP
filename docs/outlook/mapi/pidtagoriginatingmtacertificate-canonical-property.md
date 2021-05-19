---
title: PidTagOriginatingMtaCertificate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatingMtaCertificate
api_type:
- COM
ms.assetid: f6b7ff0c-19a0-4cad-8868-c05397fcebf4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f78609537b85a89617e7b2fa8f30a4ba952805b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414810"
---
# <a name="pidtagoriginatingmtacertificate-canonical-property"></a><span data-ttu-id="8b1cc-103">PidTagOriginatingMtaCertificate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8b1cc-103">PidTagOriginatingMtaCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="8b1cc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b1cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b1cc-105">メッセージを発信したメッセージ転送エージェント (MTA) の識別子を含む。</span><span class="sxs-lookup"><span data-stu-id="8b1cc-105">Contains an identifier for the message transfer agent (MTA) that originated the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b1cc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8b1cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b1cc-107">PR_ORIGINATING_MTA_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="8b1cc-107">PR_ORIGINATING_MTA_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="8b1cc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8b1cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b1cc-109">0x0E25</span><span class="sxs-lookup"><span data-stu-id="8b1cc-109">0x0E25</span></span>  <br/> |
|<span data-ttu-id="8b1cc-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8b1cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b1cc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8b1cc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8b1cc-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8b1cc-112">Area:</span></span>  <br/> |<span data-ttu-id="8b1cc-113">Server</span><span class="sxs-lookup"><span data-stu-id="8b1cc-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b1cc-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8b1cc-114">Remarks</span></span>

<span data-ttu-id="8b1cc-115">このプロパティを設定すると、[送信されたアイテム] フォルダー内の送信メッセージで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b1cc-115">This property, if set, is available on sent messages in the Sent Items folder.</span></span>
  
<span data-ttu-id="8b1cc-116">このプロパティは、メッセージごとの X.400 レポート属性に対応します。</span><span class="sxs-lookup"><span data-stu-id="8b1cc-116">This property corresponds to the X.400 report per-message attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8b1cc-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8b1cc-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8b1cc-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8b1cc-118">Header files</span></span>

<span data-ttu-id="8b1cc-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b1cc-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b1cc-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8b1cc-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b1cc-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8b1cc-121">Mapitags.h</span></span>
  
> <span data-ttu-id="8b1cc-122">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="8b1cc-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b1cc-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="8b1cc-123">See also</span></span>



[<span data-ttu-id="8b1cc-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8b1cc-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b1cc-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8b1cc-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b1cc-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8b1cc-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b1cc-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8b1cc-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

