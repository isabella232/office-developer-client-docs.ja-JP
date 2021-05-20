---
title: IDistList IMAPIContainer
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431548"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="27462-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="27462-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="27462-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27462-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27462-105">変更可能なアドレス帳コンテナー内の配布リストへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="27462-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="27462-106">**IDistList は** 、名前解決の実行に加えて、配布リストを作成、コピー、および削除できます。</span><span class="sxs-lookup"><span data-stu-id="27462-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27462-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="27462-107">Header file:</span></span>  <br/> |<span data-ttu-id="27462-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27462-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="27462-109">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="27462-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="27462-110">配布リスト オブジェクト</span><span class="sxs-lookup"><span data-stu-id="27462-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="27462-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="27462-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="27462-112">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="27462-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="27462-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="27462-113">Called by:</span></span>  <br/> |<span data-ttu-id="27462-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="27462-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="27462-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="27462-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="27462-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="27462-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="27462-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="27462-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="27462-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="27462-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="27462-119">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="27462-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="27462-120">Transacted</span><span class="sxs-lookup"><span data-stu-id="27462-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="27462-121">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="27462-121">Vtable order</span></span>

<span data-ttu-id="27462-122">このインターフェイスには、一意のメソッドが含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="27462-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="27462-123">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="27462-123">**Required properties**</span></span>|<span data-ttu-id="27462-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="27462-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="27462-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="27462-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="27462-126">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="27462-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="27462-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="27462-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="27462-128">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="27462-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="27462-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="27462-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="27462-130">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="27462-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="27462-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="27462-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="27462-132">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="27462-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="27462-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="27462-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="27462-134">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="27462-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27462-135">注釈</span><span class="sxs-lookup"><span data-stu-id="27462-135">Remarks</span></span>

<span data-ttu-id="27462-136">**IDistList インターフェイスは** [IMAPIContainer](imapicontainerimapiprop.md)から継承され、アドレス帳コンテナーと同じメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="27462-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="27462-137">したがって **、IDistList** インターフェイスのメソッドは [IABContainer](iabcontainerimapicontainer.md) インターフェイスのメソッドと同じであるため、ここでは重複されません。</span><span class="sxs-lookup"><span data-stu-id="27462-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="27462-138">**IDistList** を実装する配布リストまたはオブジェクトは、メッセージング ユーザー オブジェクトまたは個々の受信者のコレクションです。</span><span class="sxs-lookup"><span data-stu-id="27462-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="27462-139">配布リストは、すべてのメッセージング ユーザー オブジェクト、または一部のメッセージング ユーザーと一部の配布リストで構成できます。</span><span class="sxs-lookup"><span data-stu-id="27462-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="27462-140">通常、配布リストには次の 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="27462-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="27462-141">基になるメッセージング システムによって展開される配布リスト。</span><span class="sxs-lookup"><span data-stu-id="27462-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="27462-142">この種類のリストには、アドレス PR_EMAIL_ADDRESS **(** [PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)が含まれるので、個々の受信者と同じように扱います。</span><span class="sxs-lookup"><span data-stu-id="27462-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="27462-143">ローカル コンテナー内に存在し、クライアント アプリケーションによって展開される配布リスト。</span><span class="sxs-lookup"><span data-stu-id="27462-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="27462-144">オプションの配布リスト プロパティには、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="27462-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="27462-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="27462-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="27462-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="27462-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="27462-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="27462-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="27462-148">この設定 **PR_ADDRTYPE** 必須ですが、PR_EMAIL_ADDRESS **(** [PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) は必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="27462-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="27462-149">これは、電子メール アドレスのない配布リストはメッセージを受信できますが、そのメンバー リストを展開する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="27462-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="27462-150">このプロパティ **PR_ADDRTYPE** MAPIPDL に設定されている場合、MAPI は展開を実行します。</span><span class="sxs-lookup"><span data-stu-id="27462-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="27462-151">この **PR_ADDRTYPE** MAPIPDL 以外の値である場合、トランスポート プロバイダーは拡張を実行します。</span><span class="sxs-lookup"><span data-stu-id="27462-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="27462-152">**IDistList** メソッドを使用する方法の詳細については **、IABContainer** の並列メソッドのリファレンス エントリを参照してください。</span><span class="sxs-lookup"><span data-stu-id="27462-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="27462-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="27462-153">See also</span></span>



[<span data-ttu-id="27462-154">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="27462-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

