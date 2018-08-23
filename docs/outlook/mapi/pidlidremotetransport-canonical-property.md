---
title: PidLidRemoteTransport 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b0f86b2260299d2d0294598628f2895c50ed9452
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802147"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="8cb94-103">PidLidRemoteTransport 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8cb94-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="8cb94-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8cb94-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8cb94-105">どのようなアカウントのヘッダー項目に関連付けられて、POP を置くサーバーの機能に実装するには、主に識別します。</span><span class="sxs-lookup"><span data-stu-id="8cb94-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8cb94-106">関連するプロパティ</span><span class="sxs-lookup"><span data-stu-id="8cb94-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="8cb94-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="8cb94-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="8cb94-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8cb94-108">Property set:</span></span>  <br/> |<span data-ttu-id="8cb94-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="8cb94-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="8cb94-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8cb94-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8cb94-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="8cb94-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="8cb94-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8cb94-112">Data type:</span></span>  <br/> |<span data-ttu-id="8cb94-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8cb94-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8cb94-114">領域:</span><span class="sxs-lookup"><span data-stu-id="8cb94-114">Area:</span></span>  <br/> |<span data-ttu-id="8cb94-115">リモート ・ メッセージ</span><span class="sxs-lookup"><span data-stu-id="8cb94-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8cb94-116">注釈</span><span class="sxs-lookup"><span data-stu-id="8cb94-116">Remarks</span></span>

<span data-ttu-id="8cb94-117">このプロパティは、メッセージ クラスは IPM メッセージだけに関連します。リモートです。</span><span class="sxs-lookup"><span data-stu-id="8cb94-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="8cb94-118">Microsoft Outlook フォルダー関連の情報 (FAI) メッセージでは、特定の店舗へのダウンロードは、さまざまなアカウントのマッピングを保持するが、この情報をレジストリにも保存できます。</span><span class="sxs-lookup"><span data-stu-id="8cb94-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8cb94-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8cb94-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8cb94-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8cb94-120">Protocol specifications</span></span>

<span data-ttu-id="8cb94-121">[MS OXPROPS]</span><span class="sxs-lookup"><span data-stu-id="8cb94-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="8cb94-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8cb94-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8cb94-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8cb94-123">Header files</span></span>

<span data-ttu-id="8cb94-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8cb94-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="8cb94-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8cb94-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8cb94-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="8cb94-126">See also</span></span>



[<span data-ttu-id="8cb94-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8cb94-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8cb94-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8cb94-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8cb94-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8cb94-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8cb94-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8cb94-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

