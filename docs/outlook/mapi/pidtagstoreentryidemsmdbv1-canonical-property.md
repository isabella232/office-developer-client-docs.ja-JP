---
title: PidTagStoreEntryIdEmsmdbV1 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415153"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="91988-103">PidTagStoreEntryIdEmsmdbV1 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91988-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="91988-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91988-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91988-105">microsoft exchange server 2010 または exchange server 2013 のメッセージストアのエントリ識別子の古いスタイル (microsoft Outlook 2002 以前のバージョン) が格納されています。</span><span class="sxs-lookup"><span data-stu-id="91988-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91988-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="91988-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91988-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="91988-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="91988-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="91988-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91988-109">0x65f60102</span><span class="sxs-lookup"><span data-stu-id="91988-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="91988-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="91988-110">Data type:</span></span>  <br/> |<span data-ttu-id="91988-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="91988-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="91988-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="91988-112">Area:</span></span>  <br/> |<span data-ttu-id="91988-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="91988-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91988-114">注釈</span><span class="sxs-lookup"><span data-stu-id="91988-114">Remarks</span></span>

<span data-ttu-id="91988-115">Microsoft Outlook 2003 以降では、サーバー fqdn がエントリ id に統合されているため、参照用の rpc が追加されることはありません。</span><span class="sxs-lookup"><span data-stu-id="91988-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="91988-116">ただし、これによりエントリ id が長くなり、2つのエントリ id が等しいかどうかを判断するために**compareentryids**メソッドを使用する必要があるシナリオが増えます。</span><span class="sxs-lookup"><span data-stu-id="91988-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="91988-117">PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) プロパティは、microsoft Outlook 2002 (microsoft Office XP) および以前のバージョンで使用されていた Exchange Server エントリ ID の古い形式にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="91988-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="91988-118">これにより、スペースを節約したり、エントリ id が等しいかどうかを判断するために必要な**compareentryids**呼び出しの数を減らしたりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="91988-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="91988-119">古いエントリ id を使用してメールボックスを開くと、参照が必要な場合に追加の rpc が発生する可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="91988-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="91988-120">キャッシュモードで PR_STORE_ENTRYID_EMSMDB_V1 プロパティにアクセスするには、MAPI_NO_CACHE フラグと[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを使用してキャッシュをバイパスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="91988-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="91988-121">**PR_STORE_ENTRYID_EMSMDB_V1**が使用できない場合は、コードを PR_STORE_ENTRYID に戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="91988-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="91988-122">PR_STORE_ENTRYID_EMSMDB_V1 プロパティをサポートしているのは、outlook 2003 ~ Microsoft outlook 2013 のみです。</span><span class="sxs-lookup"><span data-stu-id="91988-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="91988-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="91988-123">See also</span></span>



[<span data-ttu-id="91988-124">PidTagStoreEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91988-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="91988-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="91988-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91988-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91988-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91988-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="91988-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91988-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="91988-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

