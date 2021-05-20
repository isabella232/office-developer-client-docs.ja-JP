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
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="53d0a-103">PidTagResourcePath 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="53d0a-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="53d0a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53d0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53d0a-105">サービス プロバイダーのサーバーへのパスを含む。</span><span class="sxs-lookup"><span data-stu-id="53d0a-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53d0a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="53d0a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53d0a-107">PR_RESOURCE_PATH、PR_RESOURCE_PATH_A、PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="53d0a-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="53d0a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="53d0a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53d0a-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="53d0a-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="53d0a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="53d0a-110">Data type:</span></span>  <br/> |<span data-ttu-id="53d0a-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="53d0a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="53d0a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="53d0a-112">Area:</span></span>  <br/> |<span data-ttu-id="53d0a-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="53d0a-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53d0a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="53d0a-114">Remarks</span></span>

<span data-ttu-id="53d0a-115">これらのプロパティに含まれるパスは、ユーザーがリソースを検索できる推奨パスを表します。</span><span class="sxs-lookup"><span data-stu-id="53d0a-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="53d0a-116">これらのプロパティの定義はプロバイダー固有です。</span><span class="sxs-lookup"><span data-stu-id="53d0a-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="53d0a-117">たとえば、スケジュール アプリケーションは、これらのプロパティを使用して、スケジュール アプリケーション ファイルの推奨場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="53d0a-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="53d0a-118">メッセージング ユーザー プロファイルは、クライアント アプリケーションがメッセージング ユーザーにネットワーク パスまたはネットワーク ドライブ文字の入力を求める必要が生じないので、これらのプロパティを便利に提供します。</span><span class="sxs-lookup"><span data-stu-id="53d0a-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="53d0a-119">MAPI は、米国国立標準研究所 (ANSI) の文字セットのファイル名でのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="53d0a-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="53d0a-120">元の機器メーカー (OEM) の文字セットでファイル名を使用するアプリケーションは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d0a-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="53d0a-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="53d0a-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="53d0a-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="53d0a-122">Header files</span></span>

<span data-ttu-id="53d0a-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53d0a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="53d0a-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="53d0a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="53d0a-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="53d0a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="53d0a-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="53d0a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53d0a-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="53d0a-127">See also</span></span>



[<span data-ttu-id="53d0a-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="53d0a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53d0a-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="53d0a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53d0a-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="53d0a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53d0a-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="53d0a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

