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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7c5cfa8f80895896eab9af5ce1f249b9b06cf425
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803108"
---
# <a name="pidtagoriginatingmtacertificate-canonical-property"></a><span data-ttu-id="a0c6b-103">PidTagOriginatingMtaCertificate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0c6b-103">PidTagOriginatingMtaCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="a0c6b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0c6b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0c6b-105">メッセージを生成したメッセージ転送エージェント (MTA) の識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a0c6b-105">Contains an identifier for the message transfer agent (MTA) that originated the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0c6b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a0c6b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0c6b-107">PR_ORIGINATING_MTA_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="a0c6b-107">PR_ORIGINATING_MTA_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="a0c6b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a0c6b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a0c6b-109">0x0E25</span><span class="sxs-lookup"><span data-stu-id="a0c6b-109">0x0E25</span></span>  <br/> |
|<span data-ttu-id="a0c6b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a0c6b-110">Data type:</span></span>  <br/> |<span data-ttu-id="a0c6b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a0c6b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a0c6b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="a0c6b-112">Area:</span></span>  <br/> |<span data-ttu-id="a0c6b-113">Server</span><span class="sxs-lookup"><span data-stu-id="a0c6b-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0c6b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a0c6b-114">Remarks</span></span>

<span data-ttu-id="a0c6b-115">このプロパティは、設定したかどうかがで利用可能な送信メッセージ送信済みアイテム フォルダーにします。</span><span class="sxs-lookup"><span data-stu-id="a0c6b-115">This property, if set, is available on sent messages in the Sent Items folder.</span></span>
  
<span data-ttu-id="a0c6b-116">このプロパティは、レポートの X.400 メッセージ属性に対応します。</span><span class="sxs-lookup"><span data-stu-id="a0c6b-116">This property corresponds to the X.400 report per-message attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a0c6b-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a0c6b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a0c6b-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a0c6b-118">Header files</span></span>

<span data-ttu-id="a0c6b-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0c6b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0c6b-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a0c6b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="a0c6b-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a0c6b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="a0c6b-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a0c6b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0c6b-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0c6b-123">See also</span></span>



[<span data-ttu-id="a0c6b-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0c6b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0c6b-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0c6b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0c6b-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a0c6b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0c6b-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a0c6b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

