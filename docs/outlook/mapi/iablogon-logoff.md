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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e441e84e0bddff2e5a989849dbcf593320340d2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800350"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="c19d0-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="c19d0-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="c19d0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c19d0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c19d0-105">ログオフ処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="c19d0-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c19d0-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="c19d0-106">Parameters</span></span>

 <span data-ttu-id="c19d0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c19d0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c19d0-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="c19d0-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c19d0-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c19d0-109">Return value</span></span>

<span data-ttu-id="c19d0-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c19d0-110">S_OK</span></span> 
  
> <span data-ttu-id="c19d0-111">ログオフ処理が正常に開始されました。</span><span class="sxs-lookup"><span data-stu-id="c19d0-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c19d0-112">備考</span><span class="sxs-lookup"><span data-stu-id="c19d0-112">Remarks</span></span>

<span data-ttu-id="c19d0-113">ログオフ処理は通常、クライアントがセッションを終了するのには[IMAPISession::Logoff](imapisession-logoff.md)メソッドを呼び出すときに起動します。</span><span class="sxs-lookup"><span data-stu-id="c19d0-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="c19d0-114">MAPI は、ログオフ処理を開始するのには、各アドレス帳プロバイダーの**IABLogon::Logoff**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c19d0-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="c19d0-115">**IABLogon::Logoff**メソッドは、次のこと。</span><span class="sxs-lookup"><span data-stu-id="c19d0-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="c19d0-116">サブオブジェクトまたは状態オブジェクトなど、すべての開いているオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="c19d0-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="c19d0-117">プロバイダーのサポートのオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="c19d0-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="c19d0-118">アドレス帳プロバイダーのログオフ処理の詳細については、[シャット ダウン、サービス ・ プロバイダー](shutting-down-a-service-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c19d0-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c19d0-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="c19d0-119">See also</span></span>



[<span data-ttu-id="c19d0-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="c19d0-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="c19d0-121">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c19d0-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

