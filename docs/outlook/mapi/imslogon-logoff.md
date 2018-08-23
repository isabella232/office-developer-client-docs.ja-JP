---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e72c947a6e0d4052d3335c3e3cfaf5ffb94da669
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593005"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="e5e19-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="e5e19-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="e5e19-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5e19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5e19-105">メッセージをログでは、プロバイダーを格納します。</span><span class="sxs-lookup"><span data-stu-id="e5e19-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e5e19-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e5e19-106">Parameters</span></span>

 <span data-ttu-id="e5e19-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="e5e19-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="e5e19-108">[in]予約されています。0 へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5e19-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e5e19-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e5e19-109">Return value</span></span>

<span data-ttu-id="e5e19-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5e19-110">S_OK</span></span> 
  
> <span data-ttu-id="e5e19-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e5e19-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e5e19-112">����</span><span class="sxs-lookup"><span data-stu-id="e5e19-112">Remarks</span></span>

<span data-ttu-id="e5e19-113">メッセージ ストア プロバイダーは、メッセージ ストア プロバイダーを強制的にシャット ダウンするのには**IMSLogon::Logoff**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="e5e19-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="e5e19-114">**IMSLogon::Logoff**は、次の状況で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e5e19-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="e5e19-115">MAPI は、クライアント、 [IMAPISession::Logoff](imapisession-logoff.md)メソッドを呼び出した後ログオフ中にします。</span><span class="sxs-lookup"><span data-stu-id="e5e19-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="e5e19-116">MAPI メッセージ ストア プロバイダーは、ログ中にします。</span><span class="sxs-lookup"><span data-stu-id="e5e19-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="e5e19-117">MAPI のサポート オブジェクト、 [IMsgStore::StoreLogoff](imsgstore-storelogoff.md)または**IUnknown を処理している間、メッセージ ストア プロバイダーを作成するの[](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)メソッドの処理の一部として**IMSLogon::Logoff**がここと呼ばれます。リリース**メッセージ ストアのオブジェクトに対するメソッド呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="e5e19-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e5e19-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5e19-118">See also</span></span>



[<span data-ttu-id="e5e19-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="e5e19-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="e5e19-120">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5e19-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="e5e19-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="e5e19-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="e5e19-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="e5e19-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="e5e19-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e5e19-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e5e19-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5e19-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

