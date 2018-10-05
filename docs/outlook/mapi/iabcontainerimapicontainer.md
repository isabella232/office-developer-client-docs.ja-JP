---
title: これにより IMAPIContainer
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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392187"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="34105-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="34105-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="34105-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34105-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34105-105">アドレス帳コンテナーへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="34105-105">Provides access to address book containers.</span></span> <span data-ttu-id="34105-106">MAPI およびクライアント アプリケーションの名前解決を実行しを作成するのには次のようにコピーして、**これにより**メソッドを呼び出すし、受信者を削除します。</span><span class="sxs-lookup"><span data-stu-id="34105-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34105-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="34105-107">Header file:</span></span>  <br/> |<span data-ttu-id="34105-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34105-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="34105-109">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="34105-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="34105-110">アドレス帳コンテナー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="34105-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="34105-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="34105-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="34105-112">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="34105-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="34105-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="34105-113">Called by:</span></span>  <br/> |<span data-ttu-id="34105-114">MAPI クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="34105-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="34105-115">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="34105-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="34105-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="34105-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="34105-117">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="34105-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="34105-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="34105-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="34105-119">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="34105-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="34105-120">トランザクション処理</span><span class="sxs-lookup"><span data-stu-id="34105-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="34105-121">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="34105-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="34105-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="34105-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="34105-123">メッセージングのユーザー、配布リスト、または別のコンテナーにすることができますが、新しいエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="34105-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="34105-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="34105-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="34105-125">1 つまたは複数のエントリ、メッセージを通常のユーザーまたは配布リストにコピーします。</span><span class="sxs-lookup"><span data-stu-id="34105-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="34105-126">DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="34105-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="34105-127">一般ユーザー、配布リスト、またはその他のコンテナーをメッセージング、1 つまたは複数のエントリを削除します。</span><span class="sxs-lookup"><span data-stu-id="34105-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="34105-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="34105-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="34105-129">1 つまたは複数の受信者のエントリの名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="34105-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="34105-130">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="34105-130">**Required properties**</span></span>|<span data-ttu-id="34105-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="34105-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="34105-132">**PR_CONTAINER_FLAGS**([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34105-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34105-133">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="34105-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="34105-134">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34105-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34105-135">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="34105-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="34105-136">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34105-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34105-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="34105-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="34105-138">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34105-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34105-139">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="34105-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="34105-140">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34105-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34105-141">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="34105-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="34105-142">**省略可能なプロパティ**</span><span class="sxs-lookup"><span data-stu-id="34105-142">**Optional properties**</span></span>|<span data-ttu-id="34105-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="34105-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="34105-144">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34105-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34105-145">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="34105-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="34105-146">**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34105-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34105-147">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="34105-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="34105-148">**PR_DEF_CREATE_DL**([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34105-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34105-149">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="34105-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="34105-150">**PR_DEF_CREATE_MAILUSER**([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34105-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34105-151">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="34105-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="34105-152">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34105-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34105-153">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="34105-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34105-154">備考</span><span class="sxs-lookup"><span data-stu-id="34105-154">Remarks</span></span>

<span data-ttu-id="34105-155">**これにより**インターフェイス継承しない直接[IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)インターフェイスを通じて、 [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)と[IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="34105-155">The **IABContainer** interface inherits indirectly from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="34105-156">アドレス帳プロバイダーは、**これにより**インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="34105-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="34105-157">メッセージングのユーザー オブジェクト、配布リスト、およびその他のアドレス帳コンテナーの任意の数は、アドレス帳コンテナー内に存在できます。</span><span class="sxs-lookup"><span data-stu-id="34105-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="34105-158">同様に任意のコンテナーでは、クライアントまたはサービス プロバイダーを使用できます、アドレス帳コンテナーを開くには、エントリのいずれか、または階層のテーブルまたはテーブルの内容を取得します。</span><span class="sxs-lookup"><span data-stu-id="34105-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="34105-159">アドレス帳コンテナーも名前解決を提供し、削除、またはエントリを変更する機能を追加するには、プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="34105-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="34105-160">MAPI では、他のコンテナーからコピーしたエントリを保持する個人用アドレス帳 (PAB) と呼ばれる特別なアドレス帳コンテナーを定義します。</span><span class="sxs-lookup"><span data-stu-id="34105-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="34105-161">個人用アドレス帳は、常に変更できます。</span><span class="sxs-lookup"><span data-stu-id="34105-161">A PAB is always modifiable.</span></span> <span data-ttu-id="34105-162">ユーザーは、通常、最も頻繁に通信する受信者を指定するエントリを含む、個人用アドレス帳を設定します。</span><span class="sxs-lookup"><span data-stu-id="34105-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="34105-163">個人用アドレス帳も保持できる一時アドレスと受信者の新しいされていない任意のアドレス帳コンテナーの一部です。</span><span class="sxs-lookup"><span data-stu-id="34105-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="34105-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="34105-164">See also</span></span>

- [<span data-ttu-id="34105-165">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="34105-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

