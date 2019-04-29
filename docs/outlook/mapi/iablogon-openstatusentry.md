---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 22f98e52444b17c383737bffd1685df0fb7ba8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410785"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="936c5-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="936c5-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="936c5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="936c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="936c5-105">プロバイダーの状態オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="936c5-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="936c5-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="936c5-106">Parameters</span></span>

 <span data-ttu-id="936c5-107">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="936c5-107">_lpInterface_</span></span>
  
> <span data-ttu-id="936c5-108">順番status オブジェクトへのアクセスに使用する必要があるインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="936c5-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="936c5-109">NULL を渡すと、オブジェクトの標準インターフェイス、 [imapistatus: imapistatus](imapistatusimapiprop.md)が返されます。</span><span class="sxs-lookup"><span data-stu-id="936c5-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="936c5-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="936c5-110">_ulFlags_</span></span>
  
> <span data-ttu-id="936c5-111">順番status オブジェクトが開かれる方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="936c5-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="936c5-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="936c5-112">The following flag can be set:</span></span>
    
<span data-ttu-id="936c5-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="936c5-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="936c5-114">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="936c5-114">Requests read/write permission.</span></span> <span data-ttu-id="936c5-115">既定では、オブジェクトは読み取り専用アクセスで開かれ、呼び出し元は読み取り/書き込みアクセス許可が与えられていると想定することはできません。</span><span class="sxs-lookup"><span data-stu-id="936c5-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="936c5-116">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="936c5-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="936c5-117">読み上げ開かれているオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="936c5-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="936c5-118">_lppentry_</span><span class="sxs-lookup"><span data-stu-id="936c5-118">_lppEntry_</span></span>
  
> <span data-ttu-id="936c5-119">読み上げ開かれているオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="936c5-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="936c5-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="936c5-120">Return value</span></span>

<span data-ttu-id="936c5-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="936c5-121">S_OK</span></span> 
  
> <span data-ttu-id="936c5-122">呼び出しが成功し、状態オブジェクトが開かれています。</span><span class="sxs-lookup"><span data-stu-id="936c5-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="936c5-123">注釈</span><span class="sxs-lookup"><span data-stu-id="936c5-123">Remarks</span></span>

<span data-ttu-id="936c5-124">アドレス帳プロバイダーは、状態オブジェクトへのアクセスを許可するために**openstatusentry**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="936c5-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="936c5-125">少なくとも[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドをサポートする状態オブジェクトを実装するには、すべてのアドレス帳プロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="936c5-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="936c5-126">詳細については、「 [Status オブジェクトの実装](status-object-implementation.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="936c5-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="936c5-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="936c5-127">See also</span></span>



[<span data-ttu-id="936c5-128">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="936c5-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="936c5-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="936c5-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="936c5-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="936c5-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="936c5-131">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="936c5-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

