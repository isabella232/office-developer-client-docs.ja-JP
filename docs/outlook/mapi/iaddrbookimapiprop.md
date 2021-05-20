---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da71e9dd5f2fc20bb1daf528f4466ea29507bf06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429825"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="1d07f-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1d07f-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="1d07f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d07f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d07f-105">MAPI アドレス帳へのアクセスをサポートし、一般的なダイアログ ボックスの表示などの操作が含まれます。コンテナー、メッセージング ユーザー、配布リストを開く。名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1d07f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1d07f-106">Header file:</span></span>  <br/> |<span data-ttu-id="1d07f-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="1d07f-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="1d07f-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="1d07f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="1d07f-109">アドレス帳オブジェクト</span><span class="sxs-lookup"><span data-stu-id="1d07f-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="1d07f-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="1d07f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="1d07f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="1d07f-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="1d07f-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="1d07f-112">Called by:</span></span>  <br/> |<span data-ttu-id="1d07f-113">クライアント アプリケーション、サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1d07f-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="1d07f-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="1d07f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1d07f-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="1d07f-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="1d07f-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="1d07f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="1d07f-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="1d07f-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="1d07f-118">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="1d07f-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="1d07f-119">書き込み不可</span><span class="sxs-lookup"><span data-stu-id="1d07f-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1d07f-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="1d07f-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1d07f-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="1d07f-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="1d07f-122">アドレス帳エントリを開き、エントリへのアクセスに使用できるインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="1d07f-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="1d07f-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="1d07f-124">特定のアドレス帳プロバイダーに属する 2 つのエントリ識別子を比較して、同じアドレス帳オブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="1d07f-125">アドバイス</span><span class="sxs-lookup"><span data-stu-id="1d07f-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="1d07f-126">アドレス帳内の 1 つ以上のエントリに対する変更に関する通知を受信するクライアントまたはサービス プロバイダーを登録します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="1d07f-127">Unadvise</span><span class="sxs-lookup"><span data-stu-id="1d07f-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="1d07f-128">アドレス帳エントリに対して以前に確立された通知登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="1d07f-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="1d07f-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="1d07f-130">1 回のアドレスのエントリ識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="1d07f-131">NewEntry</span><span class="sxs-lookup"><span data-stu-id="1d07f-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="1d07f-132">アドレス帳コンテナーまたは送信メッセージの受信者リストに新しい受信者を追加します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="1d07f-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="1d07f-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="1d07f-134">名前解決を実行し、受信者リストの受信者にエントリ識別子を割り当てる。</span><span class="sxs-lookup"><span data-stu-id="1d07f-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="1d07f-135">Address</span><span class="sxs-lookup"><span data-stu-id="1d07f-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="1d07f-136">[アドレスOutlook] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="1d07f-137">詳細</span><span class="sxs-lookup"><span data-stu-id="1d07f-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="1d07f-138">特定のアドレス帳エントリに関する詳細を表示するダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="1d07f-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="1d07f-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="1d07f-140">*サポートされていないか、文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="1d07f-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="1d07f-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="1d07f-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="1d07f-142">*サポートされていないか、文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="1d07f-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="1d07f-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="1d07f-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="1d07f-144">個人用アドレス帳 (PAB) として指定されているコンテナーのエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="1d07f-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="1d07f-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="1d07f-146">特定のコンテナーを個人用アドレス帳 (PAB) として指定します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="1d07f-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="1d07f-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="1d07f-148">最初のアドレス帳コンテナーのエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="1d07f-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="1d07f-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="1d07f-150">指定したコンテナーを、最初に使用可能にした既定のアドレス帳コンテナーとして確立します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="1d07f-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="1d07f-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="1d07f-152">ResolveName メソッドによって開始された名前解決プロセスに含めるコンテナーのエントリ識別子の順序付きリスト [を返](iaddrbook-resolvename.md) します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="1d07f-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="1d07f-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="1d07f-154">名前解決プロセスに使用するプロファイル内の新しい検索パスを設定します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="1d07f-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="1d07f-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="1d07f-156">メッセージング システムで後で使用する受信者リストを準備します。</span><span class="sxs-lookup"><span data-stu-id="1d07f-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d07f-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d07f-157">See also</span></span>



[<span data-ttu-id="1d07f-158">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="1d07f-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

