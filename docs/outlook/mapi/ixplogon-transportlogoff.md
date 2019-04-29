---
title: IXPLogonTransportLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 78b4feeca263035b9c90184f10edd294e6cd7b10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417862"
---
# <a name="ixplogontransportlogoff"></a><span data-ttu-id="9f4cb-103">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="9f4cb-103">IXPLogon::TransportLogoff</span></span>

  
  
<span data-ttu-id="9f4cb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f4cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f4cb-105">ログオフプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="9f4cb-105">Initiates the logoff process.</span></span> 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9f4cb-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9f4cb-106">Parameters</span></span>

 <span data-ttu-id="9f4cb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9f4cb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9f4cb-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="9f4cb-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f4cb-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="9f4cb-109">Return value</span></span>

<span data-ttu-id="9f4cb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f4cb-110">S_OK</span></span> 
  
> <span data-ttu-id="9f4cb-111">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="9f4cb-111">The call succeeded and returned the expected value or values.</span></span> <span data-ttu-id="9f4cb-112">S_OK 以外のものが返された場合、プロバイダーはログオフされます。</span><span class="sxs-lookup"><span data-stu-id="9f4cb-112">If anything other than S_OK is returned, the provider is logged off.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f4cb-113">注釈</span><span class="sxs-lookup"><span data-stu-id="9f4cb-113">Remarks</span></span>

<span data-ttu-id="9f4cb-114">MAPI スプーラーは**IXPLogon:: transportlogoff**メソッドを呼び出して、特定のユーザーのトランスポートプロバイダセッションを終了します。</span><span class="sxs-lookup"><span data-stu-id="9f4cb-114">The MAPI spooler calls the **IXPLogon::TransportLogoff** method to terminate a transport provider session for a particular user.</span></span> <span data-ttu-id="9f4cb-115">**transportlogoff**を呼び出す前に、MAPI スプーラーは、 [IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドで渡されたこのセッションについて、サポートされているメッセージアドレスの種類に関するデータをすべて破棄します。</span><span class="sxs-lookup"><span data-stu-id="9f4cb-115">Before calling **TransportLogoff**, the MAPI spooler discards any data about supported messaging address types for this session passed in the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9f4cb-116">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="9f4cb-116">Notes to implementers</span></span>

<span data-ttu-id="9f4cb-117">トランスポートプロバイダーは、いつでも**transportlogoff**への通話を承諾するように準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f4cb-117">The transport provider should be prepared to accept a call to **TransportLogoff** at any time.</span></span> <span data-ttu-id="9f4cb-118">メッセージが処理中の場合、プロバイダーは送信プロセスを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f4cb-118">If a message is in process, the provider should stop the sending process.</span></span> 
  
<span data-ttu-id="9f4cb-119">トランスポートプロバイダーは、現在のセッションに割り当てられているすべてのリソースを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f4cb-119">The transport provider should release all resources allocated for its current session.</span></span> <span data-ttu-id="9f4cb-120">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用してこのセッションのメモリを割り当てている場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用してメモリを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f4cb-120">If it has allocated any memory for this session with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, it should free the memory by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="9f4cb-121">[IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドへの呼び出しを満たすためにトランスポートプロバイダーによって割り当てられたメモリは、この時点では安全にリリースできます。</span><span class="sxs-lookup"><span data-stu-id="9f4cb-121">Any memory allocated by the transport provider to satisfy calls to the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method can be safely released at this time.</span></span> 
  
<span data-ttu-id="9f4cb-122">通常、 **transportlogoff**呼び出しの完了時に、プロバイダーは、 [imapisupport:: makeinvalid](imapisupport-makeinvalid.md)メソッドを呼び出して、そのサポートオブジェクトを解放することによって、最初にログオンオブジェクトを無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f4cb-122">Usually, on completing a **TransportLogoff** call, a provider should first invalidate its logon object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method and then release its support object.</span></span> <span data-ttu-id="9f4cb-123">サポートオブジェクトが解放されると、MAPI スプーラーはプロバイダーオブジェクト自体を解放することができるため、プロバイダーの**transportlogoff**の実装では、support オブジェクトを最後に解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f4cb-123">The provider's implementation of **TransportLogoff** should release the support object last, because when the support object is released, the MAPI spooler can also release the provider object itself.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f4cb-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="9f4cb-124">See also</span></span>



[<span data-ttu-id="9f4cb-125">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="9f4cb-125">IMAPISupport::MakeInvalid</span></span>](imapisupport-makeinvalid.md)
  
[<span data-ttu-id="9f4cb-126">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="9f4cb-126">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="9f4cb-127">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="9f4cb-127">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="9f4cb-128">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="9f4cb-128">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="9f4cb-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9f4cb-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="9f4cb-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f4cb-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

