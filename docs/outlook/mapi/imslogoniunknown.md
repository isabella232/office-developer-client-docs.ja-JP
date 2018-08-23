---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 013903f36bf648c4aed194c88104e7dd981b199f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563941"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="a9258-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9258-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="a9258-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9258-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9258-105">メッセージへのアクセスのリソースでは、ログオン オブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="a9258-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9258-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a9258-106">Header file:</span></span>  <br/> |<span data-ttu-id="a9258-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="a9258-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="a9258-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="a9258-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="a9258-109">メッセージ ストアのログオン オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a9258-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="a9258-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="a9258-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="a9258-111">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a9258-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="a9258-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a9258-112">Called by:</span></span>  <br/> |<span data-ttu-id="a9258-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="a9258-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="a9258-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="a9258-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a9258-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="a9258-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="a9258-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="a9258-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="a9258-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="a9258-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a9258-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="a9258-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a9258-119">発生しました</span><span class="sxs-lookup"><span data-stu-id="a9258-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="a9258-120">メッセージ ストアのオブジェクトに対して発生した最後のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="a9258-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="a9258-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="a9258-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="a9258-122">メッセージをログでは、プロバイダーを格納します。</span><span class="sxs-lookup"><span data-stu-id="a9258-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="a9258-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="a9258-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="a9258-124">フォルダーまたはメッセージのオブジェクトを開くし、さらにアクセスを提供するオブジェクトへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="a9258-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="a9258-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="a9258-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="a9258-126">同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="a9258-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="a9258-127">アドバイス</span><span class="sxs-lookup"><span data-stu-id="a9258-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="a9258-128">メッセージ ・ ストア内の変更についての通知のメッセージ ストア プロバイダー オブジェクトに登録します。</span><span class="sxs-lookup"><span data-stu-id="a9258-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="a9258-129">アドバイズ中止します。</span><span class="sxs-lookup"><span data-stu-id="a9258-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="a9258-130">**IMSLogon::Advise**メソッドへの呼び出しを使用して、以前に確立されたメッセージ ストアの変更を通知するためのオブジェクトの登録を削除します。</span><span class="sxs-lookup"><span data-stu-id="a9258-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="a9258-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="a9258-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="a9258-132">状態オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9258-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9258-133">注釈</span><span class="sxs-lookup"><span data-stu-id="a9258-133">Remarks</span></span>

<span data-ttu-id="a9258-134">メッセージ ストアのログオン オブジェクトは、MAPI を直接呼び出す、開いているメッセージ ストア プロバイダーの一部です。</span><span class="sxs-lookup"><span data-stu-id="a9258-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="a9258-135">MAPI 呼び出しとメッセージは、クライアント アプリケーションは、次の呼び出しはオブジェクトを格納するメッセージ ストア ログオン オブジェクトが 1 対 1 対応ログオンと思われるし、2 つのインターフェイスを公開する 1 つのオブジェクトとしてオブジェクトを格納できます。</span><span class="sxs-lookup"><span data-stu-id="a9258-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="a9258-136">2 つのオブジェクトは、同時解放と連携して作成されます。</span><span class="sxs-lookup"><span data-stu-id="a9258-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9258-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9258-137">See also</span></span>



[<span data-ttu-id="a9258-138">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a9258-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

