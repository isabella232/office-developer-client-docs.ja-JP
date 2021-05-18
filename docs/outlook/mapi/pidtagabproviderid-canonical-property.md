---
title: PidTagAbProviderId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 820df61ec23e2dd1459582e5a7bb35ad9525e0b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422244"
---
# <a name="pidtagabproviderid-canonical-property"></a><span data-ttu-id="b126d-103">PidTagAbProviderId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b126d-103">PidTagAbProviderId Canonical Property</span></span>

  
  
<span data-ttu-id="b126d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b126d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b126d-105">アドレス帳プロバイダーの [MAPIUID 構造を含](mapiuid.md) む。</span><span class="sxs-lookup"><span data-stu-id="b126d-105">Contains an address book provider's [MAPIUID](mapiuid.md) structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b126d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b126d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b126d-107">PR_AB_PROVIDER_ID</span><span class="sxs-lookup"><span data-stu-id="b126d-107">PR_AB_PROVIDER_ID</span></span>  <br/> |
|<span data-ttu-id="b126d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b126d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b126d-109">0x3615</span><span class="sxs-lookup"><span data-stu-id="b126d-109">0x3615</span></span>  <br/> |
|<span data-ttu-id="b126d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b126d-110">Data type:</span></span>  <br/> |<span data-ttu-id="b126d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b126d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b126d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b126d-112">Area:</span></span>  <br/> |<span data-ttu-id="b126d-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="b126d-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b126d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b126d-114">Remarks</span></span>

<span data-ttu-id="b126d-115">**MAPIUID 構造体は**、コンテナー階層でこの特定のコンテナーを提供するアドレス帳プロバイダーを識別します。</span><span class="sxs-lookup"><span data-stu-id="b126d-115">The **MAPIUID** structure identifies which address book provider supplies this particular container in the container hierarchy.</span></span> <span data-ttu-id="b126d-116">値は、各プロバイダーに固有です。</span><span class="sxs-lookup"><span data-stu-id="b126d-116">The value is unique to each provider.</span></span> 
  
<span data-ttu-id="b126d-117">アドレス帳プロバイダーは、複数の識別子を指定できます。</span><span class="sxs-lookup"><span data-stu-id="b126d-117">An address book provider can provide more than one identifier.</span></span> <span data-ttu-id="b126d-118">たとえば、2 つの異なるコンテナーを提供するプロバイダーは、各コンテナー PR_AB_PROVIDER_ID一 **意** の識別子を発行できます。</span><span class="sxs-lookup"><span data-stu-id="b126d-118">For example, a provider that supplies two different containers can publish in **PR_AB_PROVIDER_ID** unique identifiers for each container.</span></span> 
  
 <span data-ttu-id="b126d-119">**PR_AB_PROVIDER_ID** は、メッセージ ストアの PR_MDB_PROVIDER **(** [PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) プロパティに類似しています。</span><span class="sxs-lookup"><span data-stu-id="b126d-119">**PR_AB_PROVIDER_ID** is analogous to the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for message stores.</span></span> <span data-ttu-id="b126d-120">クライアント アプリケーションは **、PR_AB_PROVIDER_IDを** 使用して、アドレス帳階層テーブル内の関連する行を検索できます。</span><span class="sxs-lookup"><span data-stu-id="b126d-120">Client applications can use **PR_AB_PROVIDER_ID** to find related rows in an address book hierarchy table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b126d-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b126d-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b126d-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b126d-122">Header files</span></span>

<span data-ttu-id="b126d-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b126d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="b126d-124">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="b126d-124">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="b126d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b126d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b126d-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b126d-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b126d-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="b126d-127">See also</span></span>



[<span data-ttu-id="b126d-128">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="b126d-128">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="b126d-129">PidTagStoreProvider 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b126d-129">PidTagStoreProvider Canonical Property</span></span>](pidtagstoreprovider-canonical-property.md)


[<span data-ttu-id="b126d-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b126d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b126d-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b126d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b126d-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b126d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

