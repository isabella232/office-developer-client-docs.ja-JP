---
title: imapisupportsetprovideruid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a60ac0d7ab139f77aea87080e1ce37fee870e97b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437540"
---
# <a name="imapisupportsetprovideruid"></a><span data-ttu-id="57b57-103">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="57b57-103">IMAPISupport::SetProviderUID</span></span>

  
  
<span data-ttu-id="57b57-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57b57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57b57-105">サービスプロバイダーを一意に表す[MAPIUID](mapiuid.md)構造体を登録します。</span><span class="sxs-lookup"><span data-stu-id="57b57-105">Registers a [MAPIUID](mapiuid.md) structure that uniquely represents the service provider.</span></span> 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="57b57-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="57b57-106">Parameters</span></span>

 <span data-ttu-id="57b57-107">_lpproviderid_</span><span class="sxs-lookup"><span data-stu-id="57b57-107">_lpProviderID_</span></span>
  
> <span data-ttu-id="57b57-108">順番アドレス帳またはメッセージストアプロバイダーを識別する**MAPIUID**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="57b57-108">[in] A pointer to the **MAPIUID** structure that identifies the address book or message store provider.</span></span> 
    
 <span data-ttu-id="57b57-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="57b57-109">_ulFlags_</span></span>
  
> <span data-ttu-id="57b57-110">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="57b57-110">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="57b57-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="57b57-111">Return value</span></span>

<span data-ttu-id="57b57-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="57b57-112">S_OK</span></span> 
  
> <span data-ttu-id="57b57-113">**MAPIUID**構造が正常に登録されました。</span><span class="sxs-lookup"><span data-stu-id="57b57-113">The **MAPIUID** structure was successfully registered.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="57b57-114">注釈</span><span class="sxs-lookup"><span data-stu-id="57b57-114">Remarks</span></span>

<span data-ttu-id="57b57-115">**imapisupport:: setprovideruid**メソッドは、アドレス帳とメッセージストアプロバイダーのサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="57b57-115">The **IMAPISupport::SetProviderUID** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="57b57-116">これらのプロバイダーは、 **setprovideruid**を呼び出して、 _lpproviderid_によって参照されている**MAPIUID**構造体で記述された一意の識別子を登録します。</span><span class="sxs-lookup"><span data-stu-id="57b57-116">These providers call **SetProviderUID** to register a unique identifier described in the **MAPIUID** structure that is pointed to by  _lpProviderID_.</span></span> <span data-ttu-id="57b57-117">プロバイダーには、作成するすべてのエントリ識別子にこの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="57b57-117">Providers include this identifier in all of the entry identifiers that they create.</span></span> 
  
<span data-ttu-id="57b57-118">mapi は、 **MAPIUID**構造を使用して mapi スプーラーに送信メッセージを送信し、クライアント要求を処理するための適切なプロバイダーを決定します。</span><span class="sxs-lookup"><span data-stu-id="57b57-118">MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests.</span></span> <span data-ttu-id="57b57-119">たとえば、クライアントが[imapisession:: openentry](imapisession-openentry.md)メソッドを呼び出すと、MAPI はエントリ識別子の**MAPIUID**部分を調べ、それを**setprovideruid**に渡されたプロバイダーにマップし、そのプロバイダーの**openentry**を呼び出します。.</span><span class="sxs-lookup"><span data-stu-id="57b57-119">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method, MAPI examines the **MAPIUID** portion of the entry identifier, maps it to the provider that passed it to **SetProviderUID**, and calls that provider's **OpenEntry**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="57b57-120">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="57b57-120">Notes to callers</span></span>

<span data-ttu-id="57b57-121">**MAPIUID**構造を登録するには、ログオン時に**setprovideruid**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57b57-121">Call **SetProviderUID** at logon time to register your **MAPIUID** structure.</span></span> <span data-ttu-id="57b57-122">MAPI では、アドレス帳とメッセージストアプロバイダーが複数の識別子を登録できます。</span><span class="sxs-lookup"><span data-stu-id="57b57-122">MAPI allows address book and message store providers to register multiple identifiers.</span></span> <span data-ttu-id="57b57-123">**setprovideruid**に対して複数の呼び出しを行うと、 **MAPIUID**が重複している場合でも、プロバイダーの**MAPIUID**構造のセットには常に**MAPIUID**構造が追加されます。</span><span class="sxs-lookup"><span data-stu-id="57b57-123">When you make multiple calls to **SetProviderUID**, it always adds the **MAPIUID** structure to the provider's set of **MAPIUID** structures, even if the **MAPIUID** is a duplicate.</span></span> <span data-ttu-id="57b57-124">**setprovideruid**は**MAPIUID**を削除できません。</span><span class="sxs-lookup"><span data-stu-id="57b57-124">**SetProviderUID** cannot remove a **MAPIUID**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="57b57-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="57b57-125">See also</span></span>



[<span data-ttu-id="57b57-126">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="57b57-126">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="57b57-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="57b57-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

