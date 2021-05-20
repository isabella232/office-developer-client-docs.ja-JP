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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439444"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="c685e-103">PidLidRemoteTransport 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c685e-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="c685e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c685e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c685e-105">主に POP Leave on Server 機能を実装するために、ヘッダー アイテムが関連付けられているアカウントを識別します。</span><span class="sxs-lookup"><span data-stu-id="c685e-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c685e-106">関連付けられたプロパティ</span><span class="sxs-lookup"><span data-stu-id="c685e-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="c685e-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="c685e-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="c685e-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="c685e-108">Property set:</span></span>  <br/> |<span data-ttu-id="c685e-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="c685e-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="c685e-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c685e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c685e-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="c685e-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="c685e-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c685e-112">Data type:</span></span>  <br/> |<span data-ttu-id="c685e-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c685e-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="c685e-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="c685e-114">Area:</span></span>  <br/> |<span data-ttu-id="c685e-115">リモート メッセージ</span><span class="sxs-lookup"><span data-stu-id="c685e-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c685e-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c685e-116">Remarks</span></span>

<span data-ttu-id="c685e-117">このプロパティは、IPM のメッセージ クラスを持つメッセージにのみ関連します。リモート。</span><span class="sxs-lookup"><span data-stu-id="c685e-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="c685e-118">Microsoft Outlookは、フォルダー関連情報 (FAI) メッセージ内の特定のストアにダウンロードしているさまざまなアカウントのマッピングを保持しますが、この情報をレジストリに保持することもできます。</span><span class="sxs-lookup"><span data-stu-id="c685e-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c685e-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c685e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c685e-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c685e-120">Protocol specifications</span></span>

<span data-ttu-id="c685e-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="c685e-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="c685e-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="c685e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c685e-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c685e-123">Header files</span></span>

<span data-ttu-id="c685e-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c685e-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="c685e-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c685e-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c685e-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="c685e-126">See also</span></span>



[<span data-ttu-id="c685e-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c685e-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c685e-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c685e-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c685e-129">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c685e-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c685e-130">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c685e-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

