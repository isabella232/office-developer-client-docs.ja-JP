---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fc8615fcd984623ae9c17c45fb7b51a4498a723b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431079"
---
# <a name="iablogon--iunknown"></a><span data-ttu-id="54126-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54126-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="54126-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54126-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54126-105">アドレス帳プロバイダーのリソースにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="54126-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54126-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="54126-106">Header file:</span></span>  <br/> |<span data-ttu-id="54126-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="54126-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="54126-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="54126-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="54126-109">アドレス帳ログオン オブジェクト</span><span class="sxs-lookup"><span data-stu-id="54126-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="54126-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="54126-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="54126-111">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="54126-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="54126-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="54126-112">Called by:</span></span>  <br/> |<span data-ttu-id="54126-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="54126-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="54126-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="54126-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="54126-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="54126-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="54126-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="54126-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="54126-117">LPABLOGON</span><span class="sxs-lookup"><span data-stu-id="54126-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="54126-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="54126-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="54126-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="54126-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="54126-120">以前のアドレス [帳プロバイダー エラー](mapierror.md) に関する情報を含む MAPIERROR 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="54126-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="54126-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="54126-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="54126-122">ログオフ プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="54126-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="54126-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="54126-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="54126-124">コンテナー、メッセージング ユーザー、または配布リストを開き、インターフェイス実装へのポインターを返して、さらにアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="54126-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="54126-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="54126-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="54126-126">2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="54126-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="54126-127">アドバイス</span><span class="sxs-lookup"><span data-stu-id="54126-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="54126-128">コンテナー、メッセージング ユーザー、または配布リストに影響を与える指定されたイベントの通知を受け取る呼び出し元を登録します。</span><span class="sxs-lookup"><span data-stu-id="54126-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="54126-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="54126-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="54126-130">Advise メソッドの呼び出しで以前に設定された通知を **取り消** します。</span><span class="sxs-lookup"><span data-stu-id="54126-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="54126-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="54126-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="54126-132">プロバイダーの状態オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="54126-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="54126-133">OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="54126-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="54126-134">ホスト アドレス帳プロバイダーに存在するデータを含む受信者エントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="54126-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="54126-135">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="54126-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="54126-136">送信メッセージの受信者リストに追加する受信者を作成するための一時テンプレートのテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="54126-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="54126-137">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="54126-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="54126-138">メッセージング システムで後で使用する受信者リストを準備します。</span><span class="sxs-lookup"><span data-stu-id="54126-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54126-139">注釈</span><span class="sxs-lookup"><span data-stu-id="54126-139">Remarks</span></span>

<span data-ttu-id="54126-140">**IABLogon** インターフェイスのメソッドの一般的な情報については、「Service Provider Logon の実装 [」を参照してください](implementing-service-provider-logon.md)。</span><span class="sxs-lookup"><span data-stu-id="54126-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="54126-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="54126-141">See also</span></span>



[<span data-ttu-id="54126-142">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="54126-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

