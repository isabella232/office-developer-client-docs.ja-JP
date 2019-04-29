---
title: IAddrBook imapiprop
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
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="e297d-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e297d-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="e297d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e297d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e297d-105">MAPI アドレス帳へのアクセスをサポートし、コモンダイアログボックスを表示するなどの操作を含みます。コンテナー、メッセージングユーザー、および配布リストを開きます。名前解決を実行する。</span><span class="sxs-lookup"><span data-stu-id="e297d-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e297d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e297d-106">Header file:</span></span>  <br/> |<span data-ttu-id="e297d-107">mapix</span><span class="sxs-lookup"><span data-stu-id="e297d-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="e297d-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="e297d-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="e297d-109">アドレス帳オブジェクト</span><span class="sxs-lookup"><span data-stu-id="e297d-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="e297d-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="e297d-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e297d-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="e297d-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="e297d-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e297d-112">Called by:</span></span>  <br/> |<span data-ttu-id="e297d-113">クライアントアプリケーション、サービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="e297d-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="e297d-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="e297d-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e297d-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="e297d-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="e297d-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="e297d-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="e297d-117">lpadrbook</span><span class="sxs-lookup"><span data-stu-id="e297d-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="e297d-118">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="e297d-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="e297d-119">書き込み不可</span><span class="sxs-lookup"><span data-stu-id="e297d-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e297d-120">v の順序</span><span class="sxs-lookup"><span data-stu-id="e297d-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e297d-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="e297d-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="e297d-122">アドレス帳エントリを開き、エントリへのアクセスに使用できるインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="e297d-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="e297d-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="e297d-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="e297d-124">特定のアドレス帳プロバイダーに属する2つのエントリ識別子を比較して、同じアドレス帳オブジェクトを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="e297d-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="e297d-125">助言</span><span class="sxs-lookup"><span data-stu-id="e297d-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="e297d-126">クライアントまたはサービスプロバイダーに、アドレス帳の1つまたは複数のエントリの変更に関する通知を受信するように登録します。</span><span class="sxs-lookup"><span data-stu-id="e297d-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="e297d-127">アドバイズ</span><span class="sxs-lookup"><span data-stu-id="e297d-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="e297d-128">以前にアドレス帳エントリに対して設定された通知登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="e297d-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="e297d-129">createoneoff</span><span class="sxs-lookup"><span data-stu-id="e297d-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="e297d-130">1回限りのアドレスのエントリ id を作成します。</span><span class="sxs-lookup"><span data-stu-id="e297d-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="e297d-131">newentry</span><span class="sxs-lookup"><span data-stu-id="e297d-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="e297d-132">新しい受信者をアドレス帳コンテナーまたは送信メッセージの受信者リストに追加します。</span><span class="sxs-lookup"><span data-stu-id="e297d-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="e297d-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="e297d-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="e297d-134">名前解決を実行し、受信者リスト内の受信者にエントリ識別子を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e297d-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="e297d-135">住所</span><span class="sxs-lookup"><span data-stu-id="e297d-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="e297d-136">[Outlook アドレス帳] ダイアログボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="e297d-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="e297d-137">詳細</span><span class="sxs-lookup"><span data-stu-id="e297d-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="e297d-138">特定のアドレス帳エントリの詳細を表示するダイアログボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="e297d-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="e297d-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="e297d-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="e297d-140">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="e297d-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="e297d-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="e297d-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="e297d-142">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="e297d-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="e297d-143">getpab</span><span class="sxs-lookup"><span data-stu-id="e297d-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="e297d-144">個人用アドレス帳 (PAB) として指定されているコンテナーのエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="e297d-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="e297d-145">setpab</span><span class="sxs-lookup"><span data-stu-id="e297d-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="e297d-146">特定のコンテナーを個人用アドレス帳 (PAB) として指定します。</span><span class="sxs-lookup"><span data-stu-id="e297d-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="e297d-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="e297d-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="e297d-148">最初のアドレス帳コンテナーのエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="e297d-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="e297d-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="e297d-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="e297d-150">指定したコンテナーを、最初に使用可能にする既定のアドレス帳コンテナーとして確立します。</span><span class="sxs-lookup"><span data-stu-id="e297d-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="e297d-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="e297d-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="e297d-152">[ResolveName](iaddrbook-resolvename.md)メソッドによって開始された名前解決プロセスに含まれるコンテナーのエントリ id の順序付きリストを返します。</span><span class="sxs-lookup"><span data-stu-id="e297d-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="e297d-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="e297d-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="e297d-154">名前解決プロセスで使用されるプロファイルに新しい検索パスを設定します。</span><span class="sxs-lookup"><span data-stu-id="e297d-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="e297d-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="e297d-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="e297d-156">メッセージングシステムで後で使用するために、受信者リストを準備します。</span><span class="sxs-lookup"><span data-stu-id="e297d-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e297d-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="e297d-157">See also</span></span>



[<span data-ttu-id="e297d-158">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="e297d-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

