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
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285180"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="f4a5d-103">PidLidRemoteTransport 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f4a5d-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="f4a5d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4a5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4a5d-105">ヘッダーアイテムが関連付けられているアカウントを識別します。主に、サーバー機能に POP を適用するために使用します。</span><span class="sxs-lookup"><span data-stu-id="f4a5d-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4a5d-106">関連付けられたプロパティ</span><span class="sxs-lookup"><span data-stu-id="f4a5d-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="f4a5d-107">dispidremotexp</span><span class="sxs-lookup"><span data-stu-id="f4a5d-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="f4a5d-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="f4a5d-108">Property set:</span></span>  <br/> |<span data-ttu-id="f4a5d-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="f4a5d-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="f4a5d-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f4a5d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f4a5d-111">0x00008f03</span><span class="sxs-lookup"><span data-stu-id="f4a5d-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="f4a5d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f4a5d-112">Data type:</span></span>  <br/> |<span data-ttu-id="f4a5d-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="f4a5d-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="f4a5d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="f4a5d-114">Area:</span></span>  <br/> |<span data-ttu-id="f4a5d-115">リモートメッセージ</span><span class="sxs-lookup"><span data-stu-id="f4a5d-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4a5d-116">解説</span><span class="sxs-lookup"><span data-stu-id="f4a5d-116">Remarks</span></span>

<span data-ttu-id="f4a5d-117">このプロパティは、メッセージクラスが IPM であるメッセージにのみ関連しています。リモート.</span><span class="sxs-lookup"><span data-stu-id="f4a5d-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="f4a5d-118">Microsoft Outlook では、フォルダー関連情報 (fai) メッセージ内の特定のストアにダウンロードされるさまざまなアカウントのマッピングを保持しますが、この情報をレジストリに保持することもできます。</span><span class="sxs-lookup"><span data-stu-id="f4a5d-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f4a5d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f4a5d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4a5d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f4a5d-120">Protocol specifications</span></span>

<span data-ttu-id="f4a5d-121">[[OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="f4a5d-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="f4a5d-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f4a5d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4a5d-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="f4a5d-123">Header files</span></span>

<span data-ttu-id="f4a5d-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4a5d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4a5d-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f4a5d-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4a5d-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="f4a5d-126">See also</span></span>



[<span data-ttu-id="f4a5d-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f4a5d-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4a5d-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f4a5d-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4a5d-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f4a5d-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4a5d-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f4a5d-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

