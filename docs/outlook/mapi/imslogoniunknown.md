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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428880"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="23199-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23199-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="23199-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23199-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23199-105">メッセージ ストア ログオン オブジェクト内のリソースにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="23199-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23199-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="23199-106">Header file:</span></span>  <br/> |<span data-ttu-id="23199-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="23199-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="23199-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="23199-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="23199-109">メッセージ ストアログオン オブジェクト</span><span class="sxs-lookup"><span data-stu-id="23199-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="23199-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="23199-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="23199-111">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="23199-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="23199-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="23199-112">Called by:</span></span>  <br/> |<span data-ttu-id="23199-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="23199-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="23199-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="23199-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="23199-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="23199-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="23199-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="23199-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="23199-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="23199-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="23199-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="23199-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="23199-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="23199-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="23199-120">メッセージ ストア オブジェクト [に対して](mapierror.md) 発生した最後のエラーに関する情報を含む MAPIERROR 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="23199-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="23199-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="23199-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="23199-122">メッセージ ストア プロバイダーをログオフします。</span><span class="sxs-lookup"><span data-stu-id="23199-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="23199-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="23199-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="23199-124">フォルダーまたはメッセージ オブジェクトを開き、オブジェクトへのポインターを返して、さらにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="23199-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="23199-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="23199-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="23199-126">2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="23199-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="23199-127">アドバイス</span><span class="sxs-lookup"><span data-stu-id="23199-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="23199-128">メッセージ ストア内の変更に関する通知のために、メッセージ ストア プロバイダーにオブジェクトを登録します。</span><span class="sxs-lookup"><span data-stu-id="23199-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="23199-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="23199-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="23199-130">**IMSLogon::Advise** メソッドの呼び出しを使用して、以前に確立されたメッセージ ストアの変更の通知に対するオブジェクトの登録を削除します。</span><span class="sxs-lookup"><span data-stu-id="23199-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="23199-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="23199-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="23199-132">状態オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="23199-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23199-133">注釈</span><span class="sxs-lookup"><span data-stu-id="23199-133">Remarks</span></span>

<span data-ttu-id="23199-134">メッセージ ストア ログオン オブジェクトは、MAPI が直接呼び出す開いているメッセージ ストア プロバイダーの一部です。</span><span class="sxs-lookup"><span data-stu-id="23199-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="23199-135">MAPI が呼び出すメッセージ ストア ログオン オブジェクトと、クライアント アプリケーションが呼び出すメッセージ ストア オブジェクトとの間には、1 対 1 の対応があります。ログオンオブジェクトとストア オブジェクトは、2 つのインターフェイスを公開する 1 つのオブジェクトと考えて使用できます。</span><span class="sxs-lookup"><span data-stu-id="23199-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="23199-136">2 つのオブジェクトは一緒に作成され、一緒に解放されます。</span><span class="sxs-lookup"><span data-stu-id="23199-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23199-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="23199-137">See also</span></span>



[<span data-ttu-id="23199-138">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="23199-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

