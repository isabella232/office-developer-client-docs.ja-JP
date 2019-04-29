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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429860"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="d88b0-103">PidTagResourcePath 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d88b0-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="d88b0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d88b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d88b0-105">サービスプロバイダーのサーバーへのパスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d88b0-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d88b0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d88b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d88b0-107">PR_RESOURCE_PATH、PR_RESOURCE_PATH_A、PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="d88b0-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="d88b0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d88b0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d88b0-109">0x3e07</span><span class="sxs-lookup"><span data-stu-id="d88b0-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="d88b0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d88b0-110">Data type:</span></span>  <br/> |<span data-ttu-id="d88b0-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d88b0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d88b0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d88b0-112">Area:</span></span>  <br/> |<span data-ttu-id="d88b0-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="d88b0-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d88b0-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d88b0-114">Remarks</span></span>

<span data-ttu-id="d88b0-115">これらのプロパティに含まれるパスは、ユーザーがリソースを検索できる、推奨されるパスを表します。</span><span class="sxs-lookup"><span data-stu-id="d88b0-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="d88b0-116">これらのプロパティの定義は、プロバイダーに固有のものです。</span><span class="sxs-lookup"><span data-stu-id="d88b0-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="d88b0-117">たとえば、スケジュールアプリケーションは、これらのプロパティを使用して、スケジューリングアプリケーションファイルに推奨される場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="d88b0-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="d88b0-118">メッセージングユーザープロファイルは、これらのプロパティを利便性として furnishes するので、クライアントアプリケーションは、ネットワークパスまたはネットワークドライブ文字の入力を要求する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d88b0-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="d88b0-119">MAPI は、米国規格協会 (ANSI) 文字セットのファイル名に対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="d88b0-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="d88b0-120">OEM (相手先ブランド供給) 文字セットでファイル名を使用するアプリケーションは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d88b0-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d88b0-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d88b0-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d88b0-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="d88b0-122">Header files</span></span>

<span data-ttu-id="d88b0-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d88b0-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d88b0-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d88b0-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d88b0-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="d88b0-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d88b0-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d88b0-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d88b0-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="d88b0-127">See also</span></span>



[<span data-ttu-id="d88b0-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d88b0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d88b0-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d88b0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d88b0-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d88b0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d88b0-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d88b0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

