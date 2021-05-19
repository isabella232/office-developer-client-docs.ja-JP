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
# <a name="ixplogontransportlogoff"></a><span data-ttu-id="0b0cf-103">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="0b0cf-103">IXPLogon::TransportLogoff</span></span>

  
  
<span data-ttu-id="0b0cf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b0cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b0cf-105">ログオフ プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="0b0cf-105">Initiates the logoff process.</span></span> 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0b0cf-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0b0cf-106">Parameters</span></span>

 <span data-ttu-id="0b0cf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0b0cf-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0b0cf-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="0b0cf-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0b0cf-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="0b0cf-109">Return value</span></span>

<span data-ttu-id="0b0cf-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b0cf-110">S_OK</span></span> 
  
> <span data-ttu-id="0b0cf-111">呼び出しは成功し、予期される値または値を返しました。</span><span class="sxs-lookup"><span data-stu-id="0b0cf-111">The call succeeded and returned the expected value or values.</span></span> <span data-ttu-id="0b0cf-112">ユーザー以外のS_OK返された場合、プロバイダーはログオフされます。</span><span class="sxs-lookup"><span data-stu-id="0b0cf-112">If anything other than S_OK is returned, the provider is logged off.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0b0cf-113">注釈</span><span class="sxs-lookup"><span data-stu-id="0b0cf-113">Remarks</span></span>

<span data-ttu-id="0b0cf-114">MAPI スプーラーは **、IXPLogon::TransportLogoff** メソッドを呼び出して、特定のユーザーのトランスポート プロバイダー セッションを終了します。</span><span class="sxs-lookup"><span data-stu-id="0b0cf-114">The MAPI spooler calls the **IXPLogon::TransportLogoff** method to terminate a transport provider session for a particular user.</span></span> <span data-ttu-id="0b0cf-115">**TransportLogoff** を呼び出す前に、MAPI スプーラーは [、IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドで渡されたこのセッションでサポートされているメッセージング アドレスの種類に関するデータを破棄します。</span><span class="sxs-lookup"><span data-stu-id="0b0cf-115">Before calling **TransportLogoff**, the MAPI spooler discards any data about supported messaging address types for this session passed in the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0b0cf-116">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="0b0cf-116">Notes to implementers</span></span>

<span data-ttu-id="0b0cf-117">トランスポート プロバイダーは、いつでも **TransportLogoff** への呼び出しを受け入れる準備をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b0cf-117">The transport provider should be prepared to accept a call to **TransportLogoff** at any time.</span></span> <span data-ttu-id="0b0cf-118">メッセージが処理されている場合、プロバイダーは送信プロセスを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b0cf-118">If a message is in process, the provider should stop the sending process.</span></span> 
  
<span data-ttu-id="0b0cf-119">トランスポート プロバイダーは、現在のセッションに割り当てられているすべてのリソースを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b0cf-119">The transport provider should release all resources allocated for its current session.</span></span> <span data-ttu-id="0b0cf-120">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数でこのセッションにメモリが割り当てられている場合は[、MAPIFreeBuffer](mapifreebuffer.md)関数を使用してメモリを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b0cf-120">If it has allocated any memory for this session with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, it should free the memory by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="0b0cf-121">[IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドの呼び出しを満たすためにトランスポート プロバイダーによって割り当てられたメモリは、この時点で安全に解放できます。</span><span class="sxs-lookup"><span data-stu-id="0b0cf-121">Any memory allocated by the transport provider to satisfy calls to the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method can be safely released at this time.</span></span> 
  
<span data-ttu-id="0b0cf-122">通常 **、TransportLogoff** 呼び出しを完了すると、 [プロバイダーはまず IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) メソッドを呼び出してログオン オブジェクトを無効にしてから、そのサポート オブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b0cf-122">Usually, on completing a **TransportLogoff** call, a provider should first invalidate its logon object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method and then release its support object.</span></span> <span data-ttu-id="0b0cf-123">サポート オブジェクトが解放されると、MAPI スプーラーはプロバイダー オブジェクト自体を解放できるので、プロバイダーの **TransportLogoff** の実装は、サポート オブジェクトを最後に解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b0cf-123">The provider's implementation of **TransportLogoff** should release the support object last, because when the support object is released, the MAPI spooler can also release the provider object itself.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b0cf-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="0b0cf-124">See also</span></span>



[<span data-ttu-id="0b0cf-125">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="0b0cf-125">IMAPISupport::MakeInvalid</span></span>](imapisupport-makeinvalid.md)
  
[<span data-ttu-id="0b0cf-126">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="0b0cf-126">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="0b0cf-127">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="0b0cf-127">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="0b0cf-128">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="0b0cf-128">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="0b0cf-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0b0cf-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="0b0cf-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0b0cf-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

