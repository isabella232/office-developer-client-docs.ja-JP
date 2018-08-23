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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 44bc6de420953bd665bd3caa336b76b15c1effd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579460"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="5b0e5-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5b0e5-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="5b0e5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b0e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b0e5-105">MAPI アドレス帳へのアクセスをサポートし、一般的なダイアログ ボックスを表示するなどの操作が含まれていますコンテナーでは、メッセージングのユーザー、および配布を開くの一覧が表示されます。名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b0e5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5b0e5-106">Header file:</span></span>  <br/> |<span data-ttu-id="5b0e5-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="5b0e5-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="5b0e5-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="5b0e5-109">アドレス帳オブジェクト</span><span class="sxs-lookup"><span data-stu-id="5b0e5-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="5b0e5-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="5b0e5-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="5b0e5-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="5b0e5-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-112">Called by:</span></span>  <br/> |<span data-ttu-id="5b0e5-113">クライアント アプリケーション、サービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="5b0e5-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="5b0e5-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5b0e5-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="5b0e5-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="5b0e5-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="5b0e5-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="5b0e5-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="5b0e5-118">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="5b0e5-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="5b0e5-119">書き込み禁止</span><span class="sxs-lookup"><span data-stu-id="5b0e5-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5b0e5-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="5b0e5-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5b0e5-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="5b0e5-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="5b0e5-122">アドレス帳エントリを開き、エントリにアクセスするために使用するインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="5b0e5-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="5b0e5-124">同じアドレス帳オブジェクトを参照しているかどうかを判断するのには、特定のアドレス帳プロバイダーに属している 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-125">アドバイス</span><span class="sxs-lookup"><span data-stu-id="5b0e5-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="5b0e5-126">アドレス帳の 1 つまたは複数のエントリへの変更に関する通知を受信するクライアントまたはサービス プロバイダーを登録します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-127">アドバイズ中止します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="5b0e5-128">アドレス帳エントリを以前に確立された通知の登録をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="5b0e5-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="5b0e5-130">一時アドレスのエントリ id を作成します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-131">NewEntry</span><span class="sxs-lookup"><span data-stu-id="5b0e5-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="5b0e5-132">アドレス帳コンテナー、または送信メッセージの受信者の一覧には、新しい受信者を追加します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="5b0e5-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="5b0e5-134">宛先リスト内の受信者にエントリの識別子を割り当て、名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-135">住所</span><span class="sxs-lookup"><span data-stu-id="5b0e5-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="5b0e5-136">Outlook アドレス帳] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-137">詳細</span><span class="sxs-lookup"><span data-stu-id="5b0e5-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="5b0e5-138">特定のアドレス帳のエントリに関する詳細情報を表示するダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="5b0e5-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="5b0e5-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="5b0e5-140">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="5b0e5-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="5b0e5-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="5b0e5-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="5b0e5-142">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="5b0e5-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="5b0e5-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="5b0e5-144">個人用アドレス帳 (PAB) として指定されているコンテナーのエントリの識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="5b0e5-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="5b0e5-146">個人用アドレス帳 (PAB) には、特定のコンテナーを指定します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="5b0e5-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="5b0e5-148">初期のアドレス帳コンテナーのエントリの識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="5b0e5-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="5b0e5-150">既定のアドレス帳コンテナーとして最初に利用可能にするには、指定したコンテナーを確立します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="5b0e5-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="5b0e5-152">[ResolveName](iaddrbook-resolvename.md)メソッドによって開始された名前解決の処理に含まれるコンテナーのエントリ id の順序付きリストを返します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="5b0e5-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="5b0e5-154">名前解決の処理に使用されるプロファイルに新しい検索パスを設定します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="5b0e5-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="5b0e5-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="5b0e5-156">メッセージング システムによって後で使用できる受信者のリストを準備します。</span><span class="sxs-lookup"><span data-stu-id="5b0e5-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b0e5-157">関連項目</span><span class="sxs-lookup"><span data-stu-id="5b0e5-157">See also</span></span>



[<span data-ttu-id="5b0e5-158">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5b0e5-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

