---
title: idistlist IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350891"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="c168f-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c168f-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="c168f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c168f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c168f-105">変更可能なアドレス帳コンテナー内の配布リストへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="c168f-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="c168f-106">**idistlist**では、名前解決を実行するだけでなく、配布リストの作成、コピー、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c168f-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c168f-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c168f-107">Header file:</span></span>  <br/> |<span data-ttu-id="c168f-108">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c168f-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c168f-109">公開者:</span><span class="sxs-lookup"><span data-stu-id="c168f-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="c168f-110">配布リストオブジェクト</span><span class="sxs-lookup"><span data-stu-id="c168f-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="c168f-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="c168f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="c168f-112">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c168f-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="c168f-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="c168f-113">Called by:</span></span>  <br/> |<span data-ttu-id="c168f-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="c168f-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="c168f-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="c168f-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c168f-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="c168f-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="c168f-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="c168f-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="c168f-118">lpdistlist</span><span class="sxs-lookup"><span data-stu-id="c168f-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="c168f-119">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="c168f-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="c168f-120">一括</span><span class="sxs-lookup"><span data-stu-id="c168f-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c168f-121">v の順序</span><span class="sxs-lookup"><span data-stu-id="c168f-121">Vtable order</span></span>

<span data-ttu-id="c168f-122">このインターフェイスには一意のメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="c168f-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="c168f-123">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="c168f-123">**Required properties**</span></span>|<span data-ttu-id="c168f-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="c168f-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c168f-125">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c168f-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c168f-126">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="c168f-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="c168f-127">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c168f-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c168f-128">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="c168f-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="c168f-129">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c168f-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c168f-130">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="c168f-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="c168f-131">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c168f-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c168f-132">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="c168f-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="c168f-133">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c168f-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c168f-134">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="c168f-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c168f-135">解説</span><span class="sxs-lookup"><span data-stu-id="c168f-135">Remarks</span></span>

<span data-ttu-id="c168f-136">**idistlist**インターフェイスは[IMAPIContainer](imapicontainerimapiprop.md)から継承され、アドレス帳コンテナーと同じメソッドを含みます。</span><span class="sxs-lookup"><span data-stu-id="c168f-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="c168f-137">そのため、 **idistlist**インターフェイスのメソッドは[IABContainer](iabcontainerimapicontainer.md)インターフェイスのメソッドと同じなので、ここでは複製されません。</span><span class="sxs-lookup"><span data-stu-id="c168f-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="c168f-138">**idistlist**を実装する配布リストまたはオブジェクトは、メッセージングユーザーオブジェクトまたは個々の受信者のコレクションです。</span><span class="sxs-lookup"><span data-stu-id="c168f-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="c168f-139">配布リストは、すべてのメッセージングユーザーオブジェクト、または一部のメッセージングユーザーと一部の配布リストで構成できます。</span><span class="sxs-lookup"><span data-stu-id="c168f-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="c168f-140">通常、配布リストには次の2つの種類があります。</span><span class="sxs-lookup"><span data-stu-id="c168f-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="c168f-141">基礎となるメッセージングシステムによって展開された配布リスト。</span><span class="sxs-lookup"><span data-stu-id="c168f-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="c168f-142">この種類のリストには、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) という住所があり、個別の受信者と同じように処理されます。</span><span class="sxs-lookup"><span data-stu-id="c168f-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="c168f-143">ローカルコンテナーに存在し、クライアントアプリケーションによって拡張された配布リスト。</span><span class="sxs-lookup"><span data-stu-id="c168f-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="c168f-144">オプションの配布リストのプロパティは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c168f-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="c168f-145">**PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c168f-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="c168f-146">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c168f-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="c168f-147">**PR_DETAILS_TABLE**([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c168f-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="c168f-148">**PR_ADDRTYPE**は必須ですが、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) は必須ではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c168f-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="c168f-149">これは、電子メールアドレスのない配布リストでもメッセージを受信できるが、そのメンバーリストを展開する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="c168f-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="c168f-150">**PR_ADDRTYPE**プロパティが mapipdl に設定されている場合、MAPI は拡張を実行します。</span><span class="sxs-lookup"><span data-stu-id="c168f-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="c168f-151">**PR_ADDRTYPE**が mapipdl 以外の値の場合は、トランスポートプロバイダーが拡張を実行します。</span><span class="sxs-lookup"><span data-stu-id="c168f-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="c168f-152">**idistlist**メソッドの使用方法の詳細については、 **IABContainer**の parallel メソッドの参照エントリを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c168f-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c168f-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="c168f-153">See also</span></span>



[<span data-ttu-id="c168f-154">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="c168f-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

