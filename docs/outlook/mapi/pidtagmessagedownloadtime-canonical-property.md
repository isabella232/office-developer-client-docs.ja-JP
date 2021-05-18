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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407929"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="2e23a-103">PidTagMessageDownloadTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2e23a-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="2e23a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e23a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e23a-105">リモート サーバーからローカル メッセージ ストアにメッセージをダウンロードする推定時間を格納します。</span><span class="sxs-lookup"><span data-stu-id="2e23a-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e23a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2e23a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e23a-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="2e23a-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="2e23a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2e23a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2e23a-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="2e23a-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="2e23a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2e23a-110">Data type:</span></span>  <br/> |<span data-ttu-id="2e23a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2e23a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2e23a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2e23a-112">Area:</span></span>  <br/> |<span data-ttu-id="2e23a-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="2e23a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e23a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2e23a-114">Remarks</span></span>

<span data-ttu-id="2e23a-115">このプロパティは秒で表され、リモート トランスポート プロバイダーが現在の場所からヘッダー フォルダーを表示しているクライアントにローカルなメッセージ ストアに特定のメッセージをダウンロードする時間の最良の推定値を表します。</span><span class="sxs-lookup"><span data-stu-id="2e23a-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="2e23a-116">リモート トランスポート プロバイダーは、通常 **、PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) プロパティの値を、通信リンクの速度を 1 秒あたりのバイト数で割って、このプロパティの値を計算します。</span><span class="sxs-lookup"><span data-stu-id="2e23a-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="2e23a-117">プロバイダーがダウンロード時間を計算できない場合 (リンク速度が分からない場合など)、ヘッダー フォルダーのコンテンツテーブルにこの列の **MAPI_E_NO_SUPPORT** などの PT_ERROR 値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e23a-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2e23a-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2e23a-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2e23a-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2e23a-119">Header files</span></span>

<span data-ttu-id="2e23a-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e23a-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e23a-121">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2e23a-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e23a-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2e23a-122">Mapitags.h</span></span>
  
> <span data-ttu-id="2e23a-123">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="2e23a-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e23a-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e23a-124">See also</span></span>



[<span data-ttu-id="2e23a-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2e23a-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e23a-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2e23a-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e23a-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2e23a-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e23a-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2e23a-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

