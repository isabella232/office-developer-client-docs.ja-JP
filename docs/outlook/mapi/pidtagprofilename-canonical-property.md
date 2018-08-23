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
ms.openlocfilehash: 708e77e4df097f5a0de008e09808ffcbc0289f61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574581"
---
# <a name="pidtagprofilename-canonical-property"></a><span data-ttu-id="7f4ed-103">PidTagProfileName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7f4ed-103">PidTagProfileName Canonical Property</span></span>

  
  
<span data-ttu-id="7f4ed-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f4ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f4ed-105">プロファイルの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f4ed-105">Contains the name of the profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f4ed-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7f4ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f4ed-107">PR_PROFILE_NAME、PR_PROFILE_NAME_A、PR_PROFILE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="7f4ed-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="7f4ed-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7f4ed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f4ed-109">0x3D12</span><span class="sxs-lookup"><span data-stu-id="7f4ed-109">0x3D12</span></span>  <br/> |
|<span data-ttu-id="7f4ed-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7f4ed-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f4ed-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7f4ed-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7f4ed-112">領域:</span><span class="sxs-lookup"><span data-stu-id="7f4ed-112">Area:</span></span>  <br/> |<span data-ttu-id="7f4ed-113">MAPI プロファイルの構成</span><span class="sxs-lookup"><span data-stu-id="7f4ed-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f4ed-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7f4ed-114">Remarks</span></span>

<span data-ttu-id="7f4ed-115">これらのプロパティは、サービス プロバイダーによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="7f4ed-115">These properties are computed by service providers.</span></span> <span data-ttu-id="7f4ed-116">**ServiceEntry**関数のプロバイダーの実装では、プロファイル名を検出するのにはこれらのプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f4ed-116">A provider's implementation of the **ServiceEntry** function can use these properties to discover the profile name.</span></span> 
  
<span data-ttu-id="7f4ed-117">クライアント アプリケーションでは、MAPI サブシステムの状態テーブルの行の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティを調べることによって、プロファイル名を取得するための便利な方法として、これらのプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f4ed-117">Client applications can use these properties as a convenient alternative to obtaining the profile name by examining the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MAPI subsystem's status table row.</span></span>
  
<span data-ttu-id="7f4ed-118">これらのプロパティが一意でくださいない時、たとえば、プロファイルが削除され、同じ名前の後で再作成で。</span><span class="sxs-lookup"><span data-stu-id="7f4ed-118">These properties may not be unique across time, for example where a profile is deleted and later recreated with the same name.</span></span> <span data-ttu-id="7f4ed-119">MAPI と呼ばれるハード コーディングされたプロファイル セクションで完全に一意の**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティを提供する**MUID_PROFILE_INSTANCE です**。</span><span class="sxs-lookup"><span data-stu-id="7f4ed-119">MAPI furnishes a totally unique **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property in a hard-coded profile section called **MUID_PROFILE_INSTANCE.**</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7f4ed-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7f4ed-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7f4ed-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7f4ed-121">Header files</span></span>

<span data-ttu-id="7f4ed-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f4ed-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f4ed-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f4ed-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f4ed-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7f4ed-124">Mapitags.h</span></span>
  
> <span data-ttu-id="7f4ed-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f4ed-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f4ed-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="7f4ed-126">See also</span></span>



[<span data-ttu-id="7f4ed-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7f4ed-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f4ed-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7f4ed-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f4ed-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7f4ed-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f4ed-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7f4ed-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

