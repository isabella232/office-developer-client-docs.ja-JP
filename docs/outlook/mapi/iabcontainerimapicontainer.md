---
title: IABContainer IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348959"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="5fd04-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5fd04-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="5fd04-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fd04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fd04-105">アドレス帳コンテナーへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="5fd04-105">Provides access to address book containers.</span></span> <span data-ttu-id="5fd04-106">MAPI およびクライアントアプリケーションは、 **IABContainer**のメソッドを呼び出して、名前の解決を行い、受信者の作成、コピー、および削除を行います。</span><span class="sxs-lookup"><span data-stu-id="5fd04-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fd04-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5fd04-107">Header file:</span></span>  <br/> |<span data-ttu-id="5fd04-108">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5fd04-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5fd04-109">公開者:</span><span class="sxs-lookup"><span data-stu-id="5fd04-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="5fd04-110">アドレス帳のコンテナーオブジェクト</span><span class="sxs-lookup"><span data-stu-id="5fd04-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="5fd04-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="5fd04-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="5fd04-112">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="5fd04-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="5fd04-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5fd04-113">Called by:</span></span>  <br/> |<span data-ttu-id="5fd04-114">MAPI およびクライアントアプリケーション</span><span class="sxs-lookup"><span data-stu-id="5fd04-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="5fd04-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="5fd04-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5fd04-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="5fd04-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="5fd04-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="5fd04-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="5fd04-118">lpabcont</span><span class="sxs-lookup"><span data-stu-id="5fd04-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="5fd04-119">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="5fd04-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="5fd04-120">一括</span><span class="sxs-lookup"><span data-stu-id="5fd04-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5fd04-121">v の順序</span><span class="sxs-lookup"><span data-stu-id="5fd04-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5fd04-122">createentry</span><span class="sxs-lookup"><span data-stu-id="5fd04-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="5fd04-123">新しいエントリを作成します。これは、メッセージングユーザー、配布リスト、または別のコンテナーにすることができます。</span><span class="sxs-lookup"><span data-stu-id="5fd04-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="5fd04-124">copyentries</span><span class="sxs-lookup"><span data-stu-id="5fd04-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="5fd04-125">1つまたは複数のエントリ (通常はメッセージングユーザーまたは配布リスト) をコピーします。</span><span class="sxs-lookup"><span data-stu-id="5fd04-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="5fd04-126">「spaudit.deleteentries</span><span class="sxs-lookup"><span data-stu-id="5fd04-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="5fd04-127">1つ以上のエントリ (通常、メッセージングユーザー、配布リスト、またはその他のコンテナー) を削除します。</span><span class="sxs-lookup"><span data-stu-id="5fd04-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="5fd04-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="5fd04-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="5fd04-129">1つまたは複数の受信者エントリの名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="5fd04-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="5fd04-130">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="5fd04-130">**Required properties**</span></span>|<span data-ttu-id="5fd04-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="5fd04-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5fd04-132">**PR_CONTAINER_FLAGS**([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5fd04-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5fd04-133">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5fd04-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="5fd04-134">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5fd04-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5fd04-135">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="5fd04-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="5fd04-136">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5fd04-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5fd04-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5fd04-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="5fd04-138">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5fd04-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5fd04-139">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5fd04-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="5fd04-140">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5fd04-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5fd04-141">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5fd04-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="5fd04-142">**省略可能なプロパティ**</span><span class="sxs-lookup"><span data-stu-id="5fd04-142">**Optional properties**</span></span>|<span data-ttu-id="5fd04-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="5fd04-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5fd04-144">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5fd04-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5fd04-145">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5fd04-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="5fd04-146">**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5fd04-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5fd04-147">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5fd04-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="5fd04-148">**PR_DEF_CREATE_DL**([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5fd04-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5fd04-149">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5fd04-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="5fd04-150">**PR_DEF_CREATE_MAILUSER**([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5fd04-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5fd04-151">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5fd04-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="5fd04-152">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5fd04-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5fd04-153">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="5fd04-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5fd04-154">解説</span><span class="sxs-lookup"><span data-stu-id="5fd04-154">Remarks</span></span>

<span data-ttu-id="5fd04-155">**IABContainer**インターフェイスは、 [IMAPIContainer: imapiprop](imapicontainerimapiprop.md)および[imapiprop: iunknown](imapipropiunknown.md)インターフェイスを介して、 [iunknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)インターフェイスから間接的に継承されます。</span><span class="sxs-lookup"><span data-stu-id="5fd04-155">The **IABContainer** interface inherits indirectly from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="5fd04-156">アドレス帳プロバイダーは**IABContainer**インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="5fd04-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="5fd04-157">アドレス帳コンテナーには、任意の数のメッセージングユーザーオブジェクト、配布リスト、およびその他のアドレス帳コンテナーを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5fd04-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="5fd04-158">他のコンテナーと同様に、クライアントまたはサービスプロバイダーは、アドレス帳コンテナーを使用して、そのエントリの1つを開くか、階層テーブルまたは contents テーブルを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="5fd04-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="5fd04-159">また、アドレス帳コンテナーは、プロバイダーによって、エントリの追加、削除、または変更を行うことができる、名前解決を提供します。</span><span class="sxs-lookup"><span data-stu-id="5fd04-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="5fd04-160">MAPI は、他のコンテナーからコピーされたエントリを保持する個人用アドレス帳 (PAB) と呼ばれる特別なアドレス帳コンテナーを定義します。</span><span class="sxs-lookup"><span data-stu-id="5fd04-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="5fd04-161">PAB は常に変更可能です。</span><span class="sxs-lookup"><span data-stu-id="5fd04-161">A PAB is always modifiable.</span></span> <span data-ttu-id="5fd04-162">通常、ユーザーは、最も頻繁に通信する受信者を指定するエントリを PAB に設定します。</span><span class="sxs-lookup"><span data-stu-id="5fd04-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="5fd04-163">また、PAB は、アドレス帳コンテナーの一部ではない、一時アドレスと新しい受信者を保持することもできます。</span><span class="sxs-lookup"><span data-stu-id="5fd04-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5fd04-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="5fd04-164">See also</span></span>

- [<span data-ttu-id="5fd04-165">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="5fd04-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

