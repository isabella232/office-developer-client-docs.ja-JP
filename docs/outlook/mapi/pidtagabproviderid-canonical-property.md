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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 820df61ec23e2dd1459582e5a7bb35ad9525e0b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315821"
---
# <a name="pidtagabproviderid-canonical-property"></a><span data-ttu-id="ac780-103">PidTagAbProviderId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac780-103">PidTagAbProviderId Canonical Property</span></span>

  
  
<span data-ttu-id="ac780-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac780-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac780-105">アドレス帳プロバイダーの[MAPIUID](mapiuid.md)構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac780-105">Contains an address book provider's [MAPIUID](mapiuid.md) structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac780-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ac780-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac780-107">PR_AB_PROVIDER_ID</span><span class="sxs-lookup"><span data-stu-id="ac780-107">PR_AB_PROVIDER_ID</span></span>  <br/> |
|<span data-ttu-id="ac780-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ac780-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac780-109">0x3615</span><span class="sxs-lookup"><span data-stu-id="ac780-109">0x3615</span></span>  <br/> |
|<span data-ttu-id="ac780-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ac780-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac780-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ac780-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ac780-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ac780-112">Area:</span></span>  <br/> |<span data-ttu-id="ac780-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="ac780-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac780-114">解説</span><span class="sxs-lookup"><span data-stu-id="ac780-114">Remarks</span></span>

<span data-ttu-id="ac780-115">**MAPIUID**構造体は、コンテナー階層にこの特定のコンテナーを提供するアドレス帳プロバイダーを識別します。</span><span class="sxs-lookup"><span data-stu-id="ac780-115">The **MAPIUID** structure identifies which address book provider supplies this particular container in the container hierarchy.</span></span> <span data-ttu-id="ac780-116">値は、各プロバイダーに対して一意です。</span><span class="sxs-lookup"><span data-stu-id="ac780-116">The value is unique to each provider.</span></span> 
  
<span data-ttu-id="ac780-117">アドレス帳プロバイダーは、複数の識別子を提供できます。</span><span class="sxs-lookup"><span data-stu-id="ac780-117">An address book provider can provide more than one identifier.</span></span> <span data-ttu-id="ac780-118">たとえば、2つの異なるコンテナーを提供するプロバイダーは、各コンテナーの**PR_AB_PROVIDER_ID**一意識別子で公開できます。</span><span class="sxs-lookup"><span data-stu-id="ac780-118">For example, a provider that supplies two different containers can publish in **PR_AB_PROVIDER_ID** unique identifiers for each container.</span></span> 
  
 <span data-ttu-id="ac780-119">**PR_AB_PROVIDER_ID**は、メッセージストアの**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) プロパティに似ています。</span><span class="sxs-lookup"><span data-stu-id="ac780-119">**PR_AB_PROVIDER_ID** is analogous to the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for message stores.</span></span> <span data-ttu-id="ac780-120">クライアントアプリケーションは、 **PR_AB_PROVIDER_ID**を使用して、アドレス帳階層テーブル内の関連する行を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="ac780-120">Client applications can use **PR_AB_PROVIDER_ID** to find related rows in an address book hierarchy table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ac780-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ac780-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ac780-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="ac780-122">Header files</span></span>

<span data-ttu-id="ac780-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="ac780-123">Mapitags.h</span></span>
  
> <span data-ttu-id="ac780-124">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ac780-124">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="ac780-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac780-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac780-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ac780-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac780-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac780-127">See also</span></span>



[<span data-ttu-id="ac780-128">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ac780-128">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ac780-129">PidTagStoreProvider 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac780-129">PidTagStoreProvider Canonical Property</span></span>](pidtagstoreprovider-canonical-property.md)


[<span data-ttu-id="ac780-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac780-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac780-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ac780-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac780-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ac780-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

