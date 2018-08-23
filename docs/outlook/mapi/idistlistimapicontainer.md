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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7fee3c84d6a4d4a94397f5197f45637b0c7dd2be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800433"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="b6759-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b6759-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="b6759-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6759-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6759-105">本コンテナーの変更可能なアドレスでの配布リストへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b6759-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="b6759-106">**IDistList**は、作成、コピー、および名前解決を実行するだけでなく、配布リストを削除できます。</span><span class="sxs-lookup"><span data-stu-id="b6759-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6759-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b6759-107">Header file:</span></span>  <br/> |<span data-ttu-id="b6759-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6759-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b6759-109">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="b6759-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="b6759-110">配布リスト オブジェクト</span><span class="sxs-lookup"><span data-stu-id="b6759-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="b6759-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="b6759-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="b6759-112">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="b6759-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="b6759-113">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b6759-113">Called by:</span></span>  <br/> |<span data-ttu-id="b6759-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="b6759-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="b6759-115">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="b6759-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b6759-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="b6759-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="b6759-117">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="b6759-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="b6759-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="b6759-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="b6759-119">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="b6759-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="b6759-120">トランザクション処理</span><span class="sxs-lookup"><span data-stu-id="b6759-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b6759-121">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="b6759-121">Vtable order</span></span>

<span data-ttu-id="b6759-122">このインターフェイスには、固有のメソッドがありません。</span><span class="sxs-lookup"><span data-stu-id="b6759-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="b6759-123">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="b6759-123">**Required properties**</span></span>|<span data-ttu-id="b6759-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="b6759-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b6759-125">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6759-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b6759-126">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="b6759-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="b6759-127">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6759-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b6759-128">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="b6759-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="b6759-129">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6759-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b6759-130">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="b6759-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="b6759-131">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6759-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b6759-132">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="b6759-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="b6759-133">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6759-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b6759-134">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="b6759-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6759-135">注釈</span><span class="sxs-lookup"><span data-stu-id="b6759-135">Remarks</span></span>

<span data-ttu-id="b6759-136">**IDistList**インターフェイスは、 [IMAPIContainer](imapicontainerimapiprop.md)を継承し、アドレス帳コンテナーと同じメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b6759-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="b6759-137">したがって、 **IDistList**インターフェイスのメソッドは、[これにより](iabcontainerimapicontainer.md)インタ フェースのものと同一であるため、これらが重複していないここでは。</span><span class="sxs-lookup"><span data-stu-id="b6759-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="b6759-138">配布リストまたは**IDistList**を実装するオブジェクトは、メッセージングのユーザー オブジェクトまたは個々 の受信者のコレクションです。</span><span class="sxs-lookup"><span data-stu-id="b6759-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="b6759-139">配布リストは、メッセージのすべてのユーザー オブジェクトまたはいくつかのメッセージングのユーザーといくつかの配布リストで構成されます。</span><span class="sxs-lookup"><span data-stu-id="b6759-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="b6759-140">通常は、配布リストの 2 つの種類があります。</span><span class="sxs-lookup"><span data-stu-id="b6759-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="b6759-141">基になるメッセージング システムによって展開される配布リストです。</span><span class="sxs-lookup"><span data-stu-id="b6759-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="b6759-142">この種類の一覧のアドレス、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) には、個々 の受信者の場合と同じに扱われます。</span><span class="sxs-lookup"><span data-stu-id="b6759-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="b6759-143">ローカル コンテナー内に存在し、クライアント アプリケーションが展開されている配布リストです。</span><span class="sxs-lookup"><span data-stu-id="b6759-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="b6759-144">省略可能な配布リストのプロパティを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="b6759-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="b6759-145">**PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6759-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="b6759-146">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6759-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="b6759-147">**PR_DETAILS_TABLE**([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6759-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="b6759-148">**PR_ADDRTYPE**が必要ですが、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) ではないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b6759-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="b6759-149">電子メール アドレス、配布リストは、メッセージを受信もできますが、[メンバー] ボックスの一覧を展開する必要があるためにです。</span><span class="sxs-lookup"><span data-stu-id="b6759-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="b6759-150">**PR_ADDRTYPE**プロパティは、MAPIPDL に設定されている場合、MAPI は、拡張を実行します。</span><span class="sxs-lookup"><span data-stu-id="b6759-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="b6759-151">**PR_ADDRTYPE**が MAPIPDL 以外の値の場合は、トランスポート プロバイダーは、拡張を実行します。</span><span class="sxs-lookup"><span data-stu-id="b6759-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="b6759-152">**IDistList**メソッドを使用する方法の詳細については、**これにより**の並列メソッドの参照のエントリを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6759-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b6759-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6759-153">See also</span></span>



[<span data-ttu-id="b6759-154">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b6759-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

