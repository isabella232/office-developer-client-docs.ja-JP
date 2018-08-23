---
title: PidTagStoreEntryIdEmsmdbV1 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 74626b735599a5f1485b26fcb65d907b552b3089
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803591"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="62b1d-103">PidTagStoreEntryIdEmsmdbV1 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="62b1d-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="62b1d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="62b1d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="62b1d-105">以前の形式 (Microsoft Outlook 2002 およびそれ以前のバージョン) の Microsoft Exchange Server 2010 または Exchange Server 2013 のメッセージ ・ ストアのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="62b1d-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62b1d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="62b1d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62b1d-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="62b1d-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="62b1d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="62b1d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="62b1d-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="62b1d-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="62b1d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="62b1d-110">Data type:</span></span>  <br/> |<span data-ttu-id="62b1d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="62b1d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="62b1d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="62b1d-112">Area:</span></span>  <br/> |<span data-ttu-id="62b1d-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="62b1d-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62b1d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="62b1d-114">Remarks</span></span>

<span data-ttu-id="62b1d-115">Microsoft Outlook 2003 以降では、エントリ Id、参照の追加の Rpc を回避するためにサーバーの Fqdn が統合されています。</span><span class="sxs-lookup"><span data-stu-id="62b1d-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="62b1d-116">ただし、このエントリ Id が長いなりかどうかについて 2 つのエントリ Id と同じ**CompareEntryIDs**メソッドを使用する必要がある複数のシナリオを紹介します。</span><span class="sxs-lookup"><span data-stu-id="62b1d-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="62b1d-117">PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) のプロパティは古い形式の Microsoft Outlook 2002 (Microsoft Office XP) と以前のバージョンで使用されている Exchange Server のエントリ ID にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="62b1d-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="62b1d-118">領域を節約でき、 **CompareEntryIDs**呼び出しのエントリ Id が等しいときに判断するために必要な数を減らしてもこのことができます。</span><span class="sxs-lookup"><span data-stu-id="62b1d-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="62b1d-119">ある古いエントリ Id を使用してメールボックスを開くにかかる可能性がありますいくつか追加の Rpc の紹介が必要な場合に注意してください。</span><span class="sxs-lookup"><span data-stu-id="62b1d-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="62b1d-120">キャッシュ モードでの PR_STORE_ENTRYID_EMSMDB_V1 プロパティにアクセスするには、MAPI_NO_CACHE フラグを使用して、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを使用してキャッシュをバイパスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62b1d-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="62b1d-121">**PR_STORE_ENTRYID_EMSMDB_V1**を使用できない場合、コードする必要がありますに戻る PR_STORE_ENTRYID。</span><span class="sxs-lookup"><span data-stu-id="62b1d-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="62b1d-122">Microsoft Outlook 2013 で Outlook 2003 のみでは、PR_STORE_ENTRYID_EMSMDB_V1 プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="62b1d-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="62b1d-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="62b1d-123">See also</span></span>



[<span data-ttu-id="62b1d-124">PidTagStoreEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="62b1d-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="62b1d-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="62b1d-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62b1d-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="62b1d-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62b1d-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="62b1d-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62b1d-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="62b1d-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

