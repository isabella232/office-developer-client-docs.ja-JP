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
# <a name="imslogon--iunknown"></a><span data-ttu-id="083b2-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="083b2-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="083b2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="083b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="083b2-105">メッセージストアのログオンオブジェクト内のリソースにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="083b2-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="083b2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="083b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="083b2-107">Mapispi</span><span class="sxs-lookup"><span data-stu-id="083b2-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="083b2-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="083b2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="083b2-109">メッセージストアのログオンオブジェクト</span><span class="sxs-lookup"><span data-stu-id="083b2-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="083b2-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="083b2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="083b2-111">メッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="083b2-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="083b2-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="083b2-112">Called by:</span></span>  <br/> |<span data-ttu-id="083b2-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="083b2-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="083b2-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="083b2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="083b2-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="083b2-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="083b2-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="083b2-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="083b2-117">lpmslogon</span><span class="sxs-lookup"><span data-stu-id="083b2-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="083b2-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="083b2-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="083b2-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="083b2-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="083b2-120">メッセージストアオブジェクトに対して発生した最後のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="083b2-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="083b2-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="083b2-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="083b2-122">メッセージストアプロバイダーからログオフします。</span><span class="sxs-lookup"><span data-stu-id="083b2-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="083b2-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="083b2-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="083b2-124">folder オブジェクトまたは message オブジェクトを開き、オブジェクトへのポインターを返します。これにより、さらにアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="083b2-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="083b2-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="083b2-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="083b2-126">2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="083b2-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="083b2-127">助言</span><span class="sxs-lookup"><span data-stu-id="083b2-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="083b2-128">メッセージストアの変更について通知するために、オブジェクトをメッセージストアプロバイダーに登録します。</span><span class="sxs-lookup"><span data-stu-id="083b2-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="083b2-129">アドバイズ</span><span class="sxs-lookup"><span data-stu-id="083b2-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="083b2-130">**IMSLogon:: Advise**メソッドの呼び出しを使用して、以前に作成されたメッセージストア変更の通知用のオブジェクトの登録を削除します。</span><span class="sxs-lookup"><span data-stu-id="083b2-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="083b2-131">openstatusentry</span><span class="sxs-lookup"><span data-stu-id="083b2-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="083b2-132">status オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="083b2-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="083b2-133">注釈</span><span class="sxs-lookup"><span data-stu-id="083b2-133">Remarks</span></span>

<span data-ttu-id="083b2-134">メッセージストアのログオンオブジェクトは、MAPI が直接呼び出す、開いているメッセージストアプロバイダーの一部です。</span><span class="sxs-lookup"><span data-stu-id="083b2-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="083b2-135">MAPI が呼び出すメッセージストアのログオンオブジェクトと、クライアントアプリケーションが呼び出すメッセージストアオブジェクトとの間には、1対1の対応があります。ログオンおよびストアオブジェクトは、2つのインターフェイスを公開する1つのオブジェクトと考えることができます。</span><span class="sxs-lookup"><span data-stu-id="083b2-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="083b2-136">2つのオブジェクトが一緒に作成され、一緒に解放されます。</span><span class="sxs-lookup"><span data-stu-id="083b2-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="083b2-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="083b2-137">See also</span></span>



[<span data-ttu-id="083b2-138">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="083b2-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

