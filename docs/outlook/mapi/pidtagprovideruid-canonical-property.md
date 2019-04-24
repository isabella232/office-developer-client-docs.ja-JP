---
title: PidTagProviderUid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0d79075ea1db451e0c3d327df9a662e5032ebb22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286416"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="7b848-103">PidTagProviderUid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7b848-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="7b848-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b848-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b848-105">メッセージを処理するサービスプロバイダーの**MAPIUID**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7b848-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b848-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7b848-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b848-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="7b848-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="7b848-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7b848-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b848-109">0x300c</span><span class="sxs-lookup"><span data-stu-id="7b848-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="7b848-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7b848-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b848-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7b848-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7b848-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7b848-112">Area:</span></span>  <br/> |<span data-ttu-id="7b848-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="7b848-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b848-114">解説</span><span class="sxs-lookup"><span data-stu-id="7b848-114">Remarks</span></span>

<span data-ttu-id="7b848-115">このプロパティは、すべてのサービスプロバイダーによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="7b848-115">This property is computed by all service providers.</span></span> <span data-ttu-id="7b848-116">この構造体には、に関連付けられ、通常はプロバイダーによってハードコーディングされた[MAPIUID](mapiuid.md)構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7b848-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="7b848-117">通常、特定のプロバイダーによって提供されるアドレス帳コンテナーのみを対象とするクライアントアプリケーションによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b848-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="7b848-118">このプロパティは、プロバイダテーブルの列エントリとしてのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="7b848-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7b848-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7b848-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7b848-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="7b848-120">Header files</span></span>

<span data-ttu-id="7b848-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b848-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b848-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7b848-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b848-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="7b848-123">Mapitags.h</span></span>
  
> <span data-ttu-id="7b848-124">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7b848-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b848-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="7b848-125">See also</span></span>



[<span data-ttu-id="7b848-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7b848-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b848-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7b848-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b848-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7b848-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b848-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7b848-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

