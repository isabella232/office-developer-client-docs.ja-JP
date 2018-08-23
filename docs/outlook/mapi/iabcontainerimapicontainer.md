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
ms.openlocfilehash: 0eb6d62b64595474957415e94275d0ac52cc2b6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800331"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="6c01f-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="6c01f-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="6c01f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6c01f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6c01f-105">アドレス帳コンテナーへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="6c01f-105">Provides access to address book containers.</span></span> <span data-ttu-id="6c01f-106">MAPI およびクライアント アプリケーションの名前解決を実行しを作成するのには次のようにコピーして、**これにより**メソッドを呼び出すし、受信者を削除します。</span><span class="sxs-lookup"><span data-stu-id="6c01f-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6c01f-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6c01f-107">Header file:</span></span>  <br/> |<span data-ttu-id="6c01f-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c01f-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6c01f-109">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="6c01f-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="6c01f-110">アドレス帳コンテナー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6c01f-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="6c01f-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="6c01f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="6c01f-112">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6c01f-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="6c01f-113">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6c01f-113">Called by:</span></span>  <br/> |<span data-ttu-id="6c01f-114">MAPI クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6c01f-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="6c01f-115">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="6c01f-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6c01f-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="6c01f-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="6c01f-117">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="6c01f-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="6c01f-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="6c01f-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="6c01f-119">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="6c01f-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="6c01f-120">トランザクション処理</span><span class="sxs-lookup"><span data-stu-id="6c01f-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6c01f-121">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="6c01f-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6c01f-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="6c01f-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="6c01f-123">メッセージングのユーザー、配布リスト、または別のコンテナーにすることができますが、新しいエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="6c01f-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="6c01f-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="6c01f-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="6c01f-125">1 つまたは複数のエントリ、メッセージを通常のユーザーまたは配布リストにコピーします。</span><span class="sxs-lookup"><span data-stu-id="6c01f-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="6c01f-126">DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="6c01f-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="6c01f-127">一般ユーザー、配布リスト、またはその他のコンテナーをメッセージング、1 つまたは複数のエントリを削除します。</span><span class="sxs-lookup"><span data-stu-id="6c01f-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="6c01f-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="6c01f-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="6c01f-129">1 つまたは複数の受信者のエントリの名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="6c01f-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="6c01f-130">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="6c01f-130">**Required properties**</span></span>|<span data-ttu-id="6c01f-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="6c01f-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c01f-132">**PR_CONTAINER_FLAGS**([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c01f-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6c01f-133">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="6c01f-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="6c01f-134">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c01f-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6c01f-135">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="6c01f-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="6c01f-136">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c01f-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6c01f-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6c01f-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="6c01f-138">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c01f-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6c01f-139">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6c01f-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="6c01f-140">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c01f-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6c01f-141">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6c01f-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="6c01f-142">**省略可能なプロパティ**</span><span class="sxs-lookup"><span data-stu-id="6c01f-142">**Optional properties**</span></span>|<span data-ttu-id="6c01f-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="6c01f-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c01f-144">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c01f-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6c01f-145">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6c01f-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="6c01f-146">**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c01f-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6c01f-147">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6c01f-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="6c01f-148">**PR_DEF_CREATE_DL**([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c01f-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6c01f-149">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6c01f-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="6c01f-150">**PR_DEF_CREATE_MAILUSER**([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c01f-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6c01f-151">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6c01f-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="6c01f-152">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c01f-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6c01f-153">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6c01f-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c01f-154">注釈</span><span class="sxs-lookup"><span data-stu-id="6c01f-154">Remarks</span></span>

<span data-ttu-id="6c01f-155">**これにより**インターフェイス継承しない直接[IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx)インターフェイスを通じて、 [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)と[IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="6c01f-155">The **IABContainer** interface inherits indirectly from the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="6c01f-156">アドレス帳プロバイダーは、**これにより**インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="6c01f-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="6c01f-157">メッセージングのユーザー オブジェクト、配布リスト、およびその他のアドレス帳コンテナーの任意の数は、アドレス帳コンテナー内に存在できます。</span><span class="sxs-lookup"><span data-stu-id="6c01f-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="6c01f-158">同様に任意のコンテナーでは、クライアントまたはサービス プロバイダーを使用できます、アドレス帳コンテナーを開くには、エントリのいずれか、または階層のテーブルまたはテーブルの内容を取得します。</span><span class="sxs-lookup"><span data-stu-id="6c01f-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="6c01f-159">アドレス帳コンテナーも名前解決を提供し、削除、またはエントリを変更する機能を追加するには、プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="6c01f-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="6c01f-160">MAPI では、他のコンテナーからコピーしたエントリを保持する個人用アドレス帳 (PAB) と呼ばれる特別なアドレス帳コンテナーを定義します。</span><span class="sxs-lookup"><span data-stu-id="6c01f-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="6c01f-161">個人用アドレス帳は、常に変更できます。</span><span class="sxs-lookup"><span data-stu-id="6c01f-161">A PAB is always modifiable.</span></span> <span data-ttu-id="6c01f-162">ユーザーは、通常、最も頻繁に通信する受信者を指定するエントリを含む、個人用アドレス帳を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c01f-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="6c01f-163">個人用アドレス帳も保持できる一時アドレスと受信者の新しいされていない任意のアドレス帳コンテナーの一部です。</span><span class="sxs-lookup"><span data-stu-id="6c01f-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6c01f-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c01f-164">See also</span></span>

- [<span data-ttu-id="6c01f-165">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6c01f-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

