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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4421fcde6ccd2f2ac6245927d9d5d63ddc5200af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573517"
---
# <a name="iablogon--iunknown"></a><span data-ttu-id="35cf7-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35cf7-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="35cf7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35cf7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35cf7-105">アドレス帳プロバイダー内のリソースをアクセスします。</span><span class="sxs-lookup"><span data-stu-id="35cf7-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35cf7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="35cf7-106">Header file:</span></span>  <br/> |<span data-ttu-id="35cf7-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="35cf7-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="35cf7-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="35cf7-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="35cf7-109">アドレス帳ログオン オブジェクト</span><span class="sxs-lookup"><span data-stu-id="35cf7-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="35cf7-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="35cf7-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="35cf7-111">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="35cf7-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="35cf7-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="35cf7-112">Called by:</span></span>  <br/> |<span data-ttu-id="35cf7-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="35cf7-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="35cf7-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="35cf7-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="35cf7-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="35cf7-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="35cf7-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="35cf7-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="35cf7-117">LPABLOGON</span><span class="sxs-lookup"><span data-stu-id="35cf7-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="35cf7-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="35cf7-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="35cf7-119">発生しました</span><span class="sxs-lookup"><span data-stu-id="35cf7-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="35cf7-120">以前のアドレス帳プロバイダーのエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="35cf7-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="35cf7-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="35cf7-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="35cf7-122">ログオフ処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="35cf7-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="35cf7-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="35cf7-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="35cf7-124">コンテナー、ユーザー、または配布リストにメッセージを開き、さらにアクセスを提供するインターフェイスの実装にポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="35cf7-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="35cf7-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="35cf7-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="35cf7-126">同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="35cf7-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="35cf7-127">アドバイス</span><span class="sxs-lookup"><span data-stu-id="35cf7-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="35cf7-128">コンテナー、ユーザー、または配布リストをメッセージに影響を与える特定のイベントの通知を受け取る呼び出し元を登録します。</span><span class="sxs-lookup"><span data-stu-id="35cf7-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="35cf7-129">アドバイズ中止します。</span><span class="sxs-lookup"><span data-stu-id="35cf7-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="35cf7-130">**アドバイズ**メソッドへの呼び出しで以前設定された通知をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="35cf7-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="35cf7-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="35cf7-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="35cf7-132">プロバイダーの状態のオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="35cf7-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="35cf7-133">OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="35cf7-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="35cf7-134">ホストのアドレス帳プロバイダーに存在するデータが含まれている受信者のエントリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="35cf7-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="35cf7-135">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="35cf7-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="35cf7-136">送信メッセージの受信者の一覧に追加する受信者を作成するための 1 回限りのテンプレートのテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="35cf7-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="35cf7-137">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="35cf7-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="35cf7-138">メッセージング システムによって後で使用できる受信者のリストを準備します。</span><span class="sxs-lookup"><span data-stu-id="35cf7-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35cf7-139">注釈</span><span class="sxs-lookup"><span data-stu-id="35cf7-139">Remarks</span></span>

<span data-ttu-id="35cf7-140">**IABLogon**インターフェイスのメソッドの詳細については、[実装するサービス プロバイダーへのログオン](implementing-service-provider-logon.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="35cf7-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="35cf7-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="35cf7-141">See also</span></span>



[<span data-ttu-id="35cf7-142">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="35cf7-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

