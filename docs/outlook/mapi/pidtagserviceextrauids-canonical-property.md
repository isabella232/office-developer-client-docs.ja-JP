---
title: PidTagServiceExtraUids 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0fb688e2a845186224c1802f9df2ac537d5bb4d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422307"
---
# <a name="pidtagserviceextrauids-canonical-property"></a><span data-ttu-id="ad556-103">PidTagServiceExtraUids 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ad556-103">PidTagServiceExtraUids Canonical Property</span></span>

  
  
<span data-ttu-id="ad556-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad556-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad556-105">メッセージ サービスの追加のプロファイル セクションを識別する [MAPIUID](mapiuid.md) 構造の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ad556-105">Contains a list of [MAPIUID](mapiuid.md) structures that identify additional profile sections for the message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad556-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ad556-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad556-107">PR_SERVICE_EXTRA_UIDS</span><span class="sxs-lookup"><span data-stu-id="ad556-107">PR_SERVICE_EXTRA_UIDS</span></span>  <br/> |
|<span data-ttu-id="ad556-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ad556-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad556-109">0x3D0D</span><span class="sxs-lookup"><span data-stu-id="ad556-109">0x3D0D</span></span>  <br/> |
|<span data-ttu-id="ad556-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ad556-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad556-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ad556-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ad556-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ad556-112">Area:</span></span>  <br/> |<span data-ttu-id="ad556-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="ad556-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad556-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ad556-114">Remarks</span></span>

<span data-ttu-id="ad556-115">メッセージ フィルターごとに新しいプロファイル セクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="ad556-115">New profile sections can be created for each message filter.</span></span> <span data-ttu-id="ad556-116">メッセージ サービスに関する情報を別のプロファイルにコピーする場合は、フィルターの追加プロファイル セクションもコピーすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="ad556-116">When the information about the message service is to be copied to another profile, it is important to copy the additional profile sections for the filters as well.</span></span> <span data-ttu-id="ad556-117">追加のプロファイル セクションを使用するサービス プロバイダーは、これらのプロファイル セクションの **MAPIUID** 構造を PR_SERVICE_EXTRA_UIDS に格納できます **。これにより**、MAPI は追加のメッセージ サービス情報をコピーできます。</span><span class="sxs-lookup"><span data-stu-id="ad556-117">A service provider that uses additional profile sections can store the **MAPIUID** structures of those profile sections in **PR_SERVICE_EXTRA_UIDS**, which allows MAPI to copy the additional message service information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ad556-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ad556-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ad556-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ad556-119">Header files</span></span>

<span data-ttu-id="ad556-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad556-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad556-121">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ad556-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad556-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ad556-122">Mapitags.h</span></span>
  
> <span data-ttu-id="ad556-123">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="ad556-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad556-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad556-124">See also</span></span>



[<span data-ttu-id="ad556-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ad556-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad556-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ad556-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad556-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ad556-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad556-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ad556-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

