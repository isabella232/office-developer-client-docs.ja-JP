---
title: PidTagMessageDownloadTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 43916f540ca324059d53f0413105146985835ffe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588700"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="5bbf0-103">PidTagMessageDownloadTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5bbf0-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="5bbf0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bbf0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bbf0-105">リモート サーバーからローカルのメッセージ ストアにメッセージをダウンロードする予定の時間が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5bbf0-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bbf0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5bbf0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5bbf0-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="5bbf0-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="5bbf0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5bbf0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5bbf0-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="5bbf0-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="5bbf0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5bbf0-110">Data type:</span></span>  <br/> |<span data-ttu-id="5bbf0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5bbf0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5bbf0-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5bbf0-112">Area:</span></span>  <br/> |<span data-ttu-id="5bbf0-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="5bbf0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bbf0-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5bbf0-114">Remarks</span></span>

<span data-ttu-id="5bbf0-115">このプロパティは、秒単位で表され、時間がかかるリモート トランスポート プロバイダーの現在の場所から、メッセージ ・ ストアに特定のメッセージをダウンロードするのにはローカル クライアントのヘッダーのフォルダーを表示するの最適な推定値を表します。</span><span class="sxs-lookup"><span data-stu-id="5bbf0-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="5bbf0-116">リモート トランスポート プロバイダーは、通常、 **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) プロパティの値を 1 秒あたりのバイト数での通信リンクの速度で割ることによってこのプロパティの値を計算します。</span><span class="sxs-lookup"><span data-stu-id="5bbf0-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="5bbf0-117">プロバイダーがリンクの速度がわからない場合など、ダウンロードにかかる時間を計算できない場合は、 **PT_ERROR**値**MAPI_E_NO_SUPPORT**ヘッダーのフォルダーの内容のテーブルのこの列が提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bbf0-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5bbf0-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5bbf0-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5bbf0-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5bbf0-119">Header files</span></span>

<span data-ttu-id="5bbf0-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5bbf0-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="5bbf0-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5bbf0-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="5bbf0-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5bbf0-122">Mapitags.h</span></span>
  
> <span data-ttu-id="5bbf0-123">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5bbf0-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bbf0-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="5bbf0-124">See also</span></span>



[<span data-ttu-id="5bbf0-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5bbf0-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5bbf0-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5bbf0-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5bbf0-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5bbf0-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5bbf0-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5bbf0-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

