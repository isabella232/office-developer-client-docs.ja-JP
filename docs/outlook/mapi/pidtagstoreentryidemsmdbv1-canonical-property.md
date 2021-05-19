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
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a><span data-ttu-id="5d675-103">PidTagStoreEntryIdEmsmdbV1 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5d675-103">PidTagStoreEntryIdEmsmdbV1 Canonical Property</span></span>

  
  
<span data-ttu-id="5d675-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d675-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d675-105">Microsoft Exchange Server 2010 または Exchange Server 2013 メッセージ ストアのエントリ識別子の古いスタイル (Microsoft Outlook 2002 以前のバージョン) が含まれる。</span><span class="sxs-lookup"><span data-stu-id="5d675-105">Contains the old style (Microsoft Outlook 2002 and earlier versions) of the entry identifier of a Microsoft Exchange Server 2010 or Exchange Server 2013 message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d675-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5d675-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d675-107">PR_STORE_ENTRYID_EMSMDB_V1</span><span class="sxs-lookup"><span data-stu-id="5d675-107">PR_STORE_ENTRYID_EMSMDB_V1</span></span>  <br/> |
|<span data-ttu-id="5d675-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5d675-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d675-109">0x65F60102</span><span class="sxs-lookup"><span data-stu-id="5d675-109">0x65F60102</span></span>  <br/> |
|<span data-ttu-id="5d675-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5d675-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d675-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5d675-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5d675-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5d675-112">Area:</span></span>  <br/> |<span data-ttu-id="5d675-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="5d675-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d675-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5d675-114">Remarks</span></span>

<span data-ttu-id="5d675-115">Microsoft Outlook 2003 から、サーバー FQDN はエントリの ID に統合され、参照用の RPC が追加されるのを回避しました。</span><span class="sxs-lookup"><span data-stu-id="5d675-115">Starting with Microsoft Outlook 2003, the server FQDNs were integrated into the entry IDs, thereby avoiding additional RPCs for referrals.</span></span> <span data-ttu-id="5d675-116">ただし、これによりエントリの ID が長くなり、2 つのエントリの ID が同等かどうかを判断するために **CompareEntryIDs** メソッドを使用する必要があるシナリオが多くなります。</span><span class="sxs-lookup"><span data-stu-id="5d675-116">However, this makes entry IDs longer and introduces more scenarios where the **CompareEntryIDs** method must be used to determine whether two entry IDs are equivalent.</span></span> <span data-ttu-id="5d675-117">PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) プロパティは、Microsoft Outlook 2002 (Microsoft Office XP) および以前のバージョンで使用されている Exchange Server エントリ ID の古い形式にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="5d675-117">The PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) property accesses the older format of the Exchange Server entry ID used by Microsoft Outlook 2002 (Microsoft Office XP) and earlier versions.</span></span> <span data-ttu-id="5d675-118">これにより、スペースを節約し、エントリの ID が等しいかどうかを判断するために必要な **CompareEntryIDs** 呼び出しの数も削減できます。</span><span class="sxs-lookup"><span data-stu-id="5d675-118">This can save space and also reduce the number of **CompareEntryIDs** calls needed to determine when entry IDs are equivalent.</span></span> <span data-ttu-id="5d675-119">古いエントリの ID を使用してメールボックスを開く場合、参照が必要な場合は、追加の RPC が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="5d675-119">Note that using the older entry IDs to open a mailbox may incur some additional RPCs if a referral is required.</span></span> 
  
<span data-ttu-id="5d675-120">キャッシュ モードで PR_STORE_ENTRYID_EMSMDB_V1 プロパティにアクセスするには [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドで MAPI_NO_CACHE フラグを使用してキャッシュをバイパスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d675-120">To access the PR_STORE_ENTRYID_EMSMDB_V1 property while in cached mode, you must bypass the cache using the MAPI_NO_CACHE flag with the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="5d675-121">この **PR_STORE_ENTRYID_EMSMDB_V1** 使用できない場合は、コードは自動的にPR_STORE_ENTRYID。</span><span class="sxs-lookup"><span data-stu-id="5d675-121">If **PR_STORE_ENTRYID_EMSMDB_V1** isn't available, the code should fall back to PR_STORE_ENTRYID.</span></span> <span data-ttu-id="5d675-122">2003 Outlook 2003 Microsoft Outlook 2013プロパティPR_STORE_ENTRYID_EMSMDB_V1します。</span><span class="sxs-lookup"><span data-stu-id="5d675-122">Only Outlook 2003 through Microsoft Outlook 2013 support the PR_STORE_ENTRYID_EMSMDB_V1 property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d675-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d675-123">See also</span></span>



[<span data-ttu-id="5d675-124">PidTagStoreEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5d675-124">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="5d675-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5d675-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d675-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5d675-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d675-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5d675-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d675-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5d675-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

