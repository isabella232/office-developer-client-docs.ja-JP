---
title: PidTagResourcePath 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d7385ea403e7ea45c97f6fd98e422ad7eb762c4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803358"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="420e7-103">PidTagResourcePath 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="420e7-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="420e7-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="420e7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="420e7-105">サービス プロバイダーのサーバーへのパスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="420e7-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="420e7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="420e7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="420e7-107">PR_RESOURCE_PATH、PR_RESOURCE_PATH_A、PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="420e7-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="420e7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="420e7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="420e7-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="420e7-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="420e7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="420e7-110">Data type:</span></span>  <br/> |<span data-ttu-id="420e7-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="420e7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="420e7-112">領域:</span><span class="sxs-lookup"><span data-stu-id="420e7-112">Area:</span></span>  <br/> |<span data-ttu-id="420e7-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="420e7-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="420e7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="420e7-114">Remarks</span></span>

<span data-ttu-id="420e7-115">これらのプロパティに含まれているパスは、ユーザーがリソースを検索する場所として推奨されるパスを表します。</span><span class="sxs-lookup"><span data-stu-id="420e7-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="420e7-116">これらのプロパティの定義は、特定のプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="420e7-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="420e7-117">などのスケジュール アプリケーションは、そのスケジュールのアプリケーション ファイルの推奨される場所を指定するのにこれらのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="420e7-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="420e7-118">メッセージングのユーザー プロファイルは、クライアント アプリケーションが、ネットワーク パスまたはネットワーク ドライブの文字のメッセージのユーザーに確認する必要があるないように、必要に応じてこれらのプロパティを提供します。</span><span class="sxs-lookup"><span data-stu-id="420e7-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="420e7-119">MAPI は、米国規格協会 (ANSI) 文字セットのファイル名でのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="420e7-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="420e7-120">正規機器製造元 (OEM) 文字セットでファイル名を使用するアプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。</span><span class="sxs-lookup"><span data-stu-id="420e7-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="420e7-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="420e7-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="420e7-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="420e7-122">Header files</span></span>

<span data-ttu-id="420e7-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="420e7-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="420e7-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="420e7-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="420e7-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="420e7-125">Mapitags.h</span></span>
  
> <span data-ttu-id="420e7-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="420e7-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="420e7-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="420e7-127">See also</span></span>



[<span data-ttu-id="420e7-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="420e7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="420e7-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="420e7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="420e7-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="420e7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="420e7-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="420e7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

