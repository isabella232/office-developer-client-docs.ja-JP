---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416399"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="0634e-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="0634e-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="0634e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0634e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0634e-105">ログオフプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="0634e-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0634e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0634e-106">Parameters</span></span>

 <span data-ttu-id="0634e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0634e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0634e-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="0634e-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0634e-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="0634e-109">Return value</span></span>

<span data-ttu-id="0634e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0634e-110">S_OK</span></span> 
  
> <span data-ttu-id="0634e-111">ログオフプロセスが正常に開始されました。</span><span class="sxs-lookup"><span data-stu-id="0634e-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0634e-112">注釈</span><span class="sxs-lookup"><span data-stu-id="0634e-112">Remarks</span></span>

<span data-ttu-id="0634e-113">ログオフプロセスは、通常、クライアントが[imapisession:: logoff](imapisession-logoff.md)メソッドを呼び出してセッションを終了するときに開始されます。</span><span class="sxs-lookup"><span data-stu-id="0634e-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="0634e-114">次に、MAPI は各アドレス帳プロバイダーの**IABLogon:: logoff**メソッドを呼び出して、ログオフプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="0634e-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="0634e-115">**IABLogon:: Logoff**メソッドは、次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="0634e-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="0634e-116">すべてのオブジェクトを解放します (任意のオブジェクト、または status オブジェクトなど)。</span><span class="sxs-lookup"><span data-stu-id="0634e-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="0634e-117">プロバイダーのサポートオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="0634e-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="0634e-118">アドレス帳プロバイダーのログオフプロセスの詳細については、「[サービスプロバイダーをシャットダウンする](shutting-down-a-service-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0634e-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0634e-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="0634e-119">See also</span></span>



[<span data-ttu-id="0634e-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="0634e-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="0634e-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0634e-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

