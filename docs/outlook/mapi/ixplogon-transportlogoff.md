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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 195f2d718428eb8bb618fc982488c276d8a536da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801268"
---
# <a name="ixplogontransportlogoff"></a><span data-ttu-id="c2d17-103">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="c2d17-103">IXPLogon::TransportLogoff</span></span>

  
  
<span data-ttu-id="c2d17-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c2d17-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2d17-105">ログオフ処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="c2d17-105">Initiates the logoff process.</span></span> 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c2d17-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="c2d17-106">Parameters</span></span>

 <span data-ttu-id="c2d17-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c2d17-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c2d17-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="c2d17-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c2d17-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c2d17-109">Return value</span></span>

<span data-ttu-id="c2d17-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2d17-110">S_OK</span></span> 
  
> <span data-ttu-id="c2d17-111">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="c2d17-111">The call succeeded and returned the expected value or values.</span></span> <span data-ttu-id="c2d17-112">以外 S_OK が返された場合、プロバイダーがログオフされます。</span><span class="sxs-lookup"><span data-stu-id="c2d17-112">If anything other than S_OK is returned, the provider is logged off.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2d17-113">備考</span><span class="sxs-lookup"><span data-stu-id="c2d17-113">Remarks</span></span>

<span data-ttu-id="c2d17-114">MAPI スプーラーは、特定のユーザー用のトランスポート プロバイダー セッションを終了する**IXPLogon::TransportLogoff**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c2d17-114">The MAPI spooler calls the **IXPLogon::TransportLogoff** method to terminate a transport provider session for a particular user.</span></span> <span data-ttu-id="c2d17-115">**TransportLogoff**を呼び出す前に、MAPI スプーラーは、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドに渡されたこのセッションでサポートされているメッセージング アドレスの種類に関するデータを破棄します。</span><span class="sxs-lookup"><span data-stu-id="c2d17-115">Before calling **TransportLogoff**, the MAPI spooler discards any data about supported messaging address types for this session passed in the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c2d17-116">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="c2d17-116">Notes to implementers</span></span>

<span data-ttu-id="c2d17-117">トランスポート プロバイダーは、いつでも**TransportLogoff**への呼び出しを受け入れるように準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2d17-117">The transport provider should be prepared to accept a call to **TransportLogoff** at any time.</span></span> <span data-ttu-id="c2d17-118">メッセージは、プロセスでは、プロバイダーは送信プロセスを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2d17-118">If a message is in process, the provider should stop the sending process.</span></span> 
  
<span data-ttu-id="c2d17-119">トランスポート プロバイダーが現在のセッションに割り当てられているすべてのリソースを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2d17-119">The transport provider should release all resources allocated for its current session.</span></span> <span data-ttu-id="c2d17-120">場合は[MAPIAllocateBuffer](mapiallocatebuffer.md)関数では、このセッションで、すべてのメモリを割り当てられて、 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用してメモリを解放してする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2d17-120">If it has allocated any memory for this session with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, it should free the memory by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="c2d17-121">この時点で、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドの呼び出しを満たすためにトランスポート プロバイダーによって割り当てられたメモリを安全に解放できます。</span><span class="sxs-lookup"><span data-stu-id="c2d17-121">Any memory allocated by the transport provider to satisfy calls to the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method can be safely released at this time.</span></span> 
  
<span data-ttu-id="c2d17-122">通常、 **TransportLogoff**の呼び出しを完了するには、プロバイダー [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)メソッドを呼び出して、最初のログオン オブジェクトを無効にしてくださいのサポート オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="c2d17-122">Usually, on completing a **TransportLogoff** call, a provider should first invalidate its logon object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method and then release its support object.</span></span> <span data-ttu-id="c2d17-123">サポート オブジェクトが解放されると、MAPI スプーラー プロバイダー オブジェクト自体にもリリースできますので、 **TransportLogoff**のプロバイダーの実装はサポート オブジェクトを最後に、開放しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c2d17-123">The provider's implementation of **TransportLogoff** should release the support object last, because when the support object is released, the MAPI spooler can also release the provider object itself.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2d17-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="c2d17-124">See also</span></span>



[<span data-ttu-id="c2d17-125">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="c2d17-125">IMAPISupport::MakeInvalid</span></span>](imapisupport-makeinvalid.md)
  
[<span data-ttu-id="c2d17-126">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="c2d17-126">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="c2d17-127">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="c2d17-127">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="c2d17-128">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c2d17-128">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="c2d17-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c2d17-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c2d17-130">IXPLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2d17-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

