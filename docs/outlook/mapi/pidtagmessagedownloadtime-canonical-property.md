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
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325677"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="ced87-103">PidTagMessageDownloadTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ced87-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="ced87-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ced87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ced87-105">リモートサーバーからローカルメッセージストアへのメッセージのダウンロードの推定時間が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ced87-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ced87-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ced87-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ced87-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="ced87-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="ced87-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ced87-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ced87-109">0x0e18</span><span class="sxs-lookup"><span data-stu-id="ced87-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="ced87-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ced87-110">Data type:</span></span>  <br/> |<span data-ttu-id="ced87-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ced87-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ced87-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ced87-112">Area:</span></span>  <br/> |<span data-ttu-id="ced87-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="ced87-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ced87-114">解説</span><span class="sxs-lookup"><span data-stu-id="ced87-114">Remarks</span></span>

<span data-ttu-id="ced87-115">このプロパティは秒単位で表され、指定されたメッセージを現在の場所からメッセージストアにダウンロードして、ヘッダーフォルダーを表示しているクライアントに対してリモートトランスポートプロバイダーがメッセージをローカルにダウンロードするのにかかる時間の最適な推定値を表します。</span><span class="sxs-lookup"><span data-stu-id="ced87-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="ced87-116">リモートトランスポートプロバイダーは、通常、 **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) プロパティの値を、通信リンクの速度 (バイト/秒) で割ることによって、このプロパティの値を計算します。</span><span class="sxs-lookup"><span data-stu-id="ced87-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="ced87-117">プロバイダーがダウンロード時間を計算できない場合 (リンク速度がわからない場合など) は、ヘッダーフォルダーの内容の表に、この列の**MAPI_E_NO_SUPPORT**などの**PT_ERROR**値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ced87-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ced87-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ced87-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ced87-119">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="ced87-119">Header files</span></span>

<span data-ttu-id="ced87-120">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ced87-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="ced87-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ced87-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="ced87-122">Mapitags</span><span class="sxs-lookup"><span data-stu-id="ced87-122">Mapitags.h</span></span>
  
> <span data-ttu-id="ced87-123">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ced87-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ced87-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="ced87-124">See also</span></span>



[<span data-ttu-id="ced87-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ced87-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ced87-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ced87-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ced87-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ced87-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ced87-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ced87-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

