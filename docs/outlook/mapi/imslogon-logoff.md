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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348875"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="5d7c3-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="5d7c3-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="5d7c3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d7c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d7c3-105">メッセージ ストア プロバイダーをログオフします。</span><span class="sxs-lookup"><span data-stu-id="5d7c3-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5d7c3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5d7c3-106">Parameters</span></span>

 <span data-ttu-id="5d7c3-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="5d7c3-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="5d7c3-108">[in]予約済み。はゼロへのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d7c3-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5d7c3-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="5d7c3-109">Return value</span></span>

<span data-ttu-id="5d7c3-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5d7c3-110">S_OK</span></span> 
  
> <span data-ttu-id="5d7c3-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="5d7c3-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5d7c3-112">注釈</span><span class="sxs-lookup"><span data-stu-id="5d7c3-112">Remarks</span></span>

<span data-ttu-id="5d7c3-113">メッセージ ストア プロバイダーは、メッセージ ストア プロバイダーを強制的にシャットダウンする **IMSLogon::Logoff** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="5d7c3-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="5d7c3-114">**IMSLogon::Logoff は** 、次の状況で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5d7c3-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="5d7c3-115">[IMAPISession::Logoff](imapisession-logoff.md)メソッドの呼び出し後に MAPI がクライアントからログオフしている間。</span><span class="sxs-lookup"><span data-stu-id="5d7c3-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="5d7c3-116">MAPI がメッセージ ストア プロバイダーからログオフしている間。</span><span class="sxs-lookup"><span data-stu-id="5d7c3-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="5d7c3-117">この場合 **、IMSLogon::Logoff** は、メッセージ ストア オブジェクトの [IMsgStore::StoreLogoff](imsgstore-storelogoff.md)または **IUnknown::Release** メソッド呼び出しの処理中にメッセージ ストア プロバイダーが作成するサポート オブジェクトの [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを処理する MAPI の一部として呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5d7c3-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5d7c3-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d7c3-118">See also</span></span>



[<span data-ttu-id="5d7c3-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="5d7c3-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="5d7c3-120">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5d7c3-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="5d7c3-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="5d7c3-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="5d7c3-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="5d7c3-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="5d7c3-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5d7c3-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5d7c3-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5d7c3-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

