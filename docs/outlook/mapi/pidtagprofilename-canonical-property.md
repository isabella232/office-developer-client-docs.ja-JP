---
title: PidTagProfileName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 992b3a6a30e15d267ffeda11ec98c7b4aeacb2c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341651"
---
# <a name="pidtagprofilename-canonical-property"></a><span data-ttu-id="676f2-103">PidTagProfileName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="676f2-103">PidTagProfileName Canonical Property</span></span>

  
  
<span data-ttu-id="676f2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="676f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="676f2-105">プロファイルの名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="676f2-105">Contains the name of the profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="676f2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="676f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="676f2-107">PR_PROFILE_NAME、PR_PROFILE_NAME_A、PR_PROFILE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="676f2-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="676f2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="676f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="676f2-109">0x3d12</span><span class="sxs-lookup"><span data-stu-id="676f2-109">0x3D12</span></span>  <br/> |
|<span data-ttu-id="676f2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="676f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="676f2-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="676f2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="676f2-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="676f2-112">Area:</span></span>  <br/> |<span data-ttu-id="676f2-113">MAPI プロファイルの構成</span><span class="sxs-lookup"><span data-stu-id="676f2-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="676f2-114">解説</span><span class="sxs-lookup"><span data-stu-id="676f2-114">Remarks</span></span>

<span data-ttu-id="676f2-115">これらのプロパティは、サービスプロバイダーによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="676f2-115">These properties are computed by service providers.</span></span> <span data-ttu-id="676f2-116">プロバイダーの**serviceentry**関数の実装では、これらのプロパティを使用してプロファイル名を検出できます。</span><span class="sxs-lookup"><span data-stu-id="676f2-116">A provider's implementation of the **ServiceEntry** function can use these properties to discover the profile name.</span></span> 
  
<span data-ttu-id="676f2-117">クライアントアプリケーションは、これらのプロパティを使用して、プロファイル名を取得する便利な方法として、MAPI サブシステムの状態テーブル行の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="676f2-117">Client applications can use these properties as a convenient alternative to obtaining the profile name by examining the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MAPI subsystem's status table row.</span></span>
  
<span data-ttu-id="676f2-118">これらのプロパティは、プロファイルが削除された後に同じ名前で再作成された場合など、時間の経過とともに一意になることはありません。</span><span class="sxs-lookup"><span data-stu-id="676f2-118">These properties may not be unique across time, for example where a profile is deleted and later recreated with the same name.</span></span> <span data-ttu-id="676f2-119">MAPI furnishes は、MUID_PROFILE_INSTANCE という名前のハードコーディングされたプロファイルセクションで、完全に一意の**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティを**示しています。**</span><span class="sxs-lookup"><span data-stu-id="676f2-119">MAPI furnishes a totally unique **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property in a hard-coded profile section called **MUID_PROFILE_INSTANCE.**</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="676f2-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="676f2-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="676f2-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="676f2-121">Header files</span></span>

<span data-ttu-id="676f2-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="676f2-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="676f2-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="676f2-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="676f2-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="676f2-124">Mapitags.h</span></span>
  
> <span data-ttu-id="676f2-125">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="676f2-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="676f2-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="676f2-126">See also</span></span>



[<span data-ttu-id="676f2-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="676f2-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="676f2-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="676f2-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="676f2-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="676f2-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="676f2-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="676f2-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

