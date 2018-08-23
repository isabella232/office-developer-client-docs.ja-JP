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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cb9a2ba72ee9fd9c45aefe9d0797930a4871404a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579285"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="7cf2f-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="7cf2f-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="7cf2f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cf2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cf2f-105">プロバイダーの状態のオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="7cf2f-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="7cf2f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7cf2f-106">Parameters</span></span>

 <span data-ttu-id="7cf2f-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7cf2f-107">_lpInterface_</span></span>
  
> <span data-ttu-id="7cf2f-108">[in]状態オブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7cf2f-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="7cf2f-109">オブジェクトの標準のインターフェイスを返します NULL を渡す[IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="7cf2f-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="7cf2f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7cf2f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="7cf2f-111">[in]状態オブジェクトを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="7cf2f-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="7cf2f-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="7cf2f-112">The following flag can be set:</span></span>
    
<span data-ttu-id="7cf2f-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7cf2f-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="7cf2f-114">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="7cf2f-114">Requests read/write permission.</span></span> <span data-ttu-id="7cf2f-115">既定では、読み取り専用のアクセス権を持つオブジェクトが開いているし、呼び出し元の読み取り/書き込み権限が付与されていると仮定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cf2f-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="7cf2f-116">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="7cf2f-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="7cf2f-117">[out]開かれたオブジェクトの型へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7cf2f-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="7cf2f-118">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="7cf2f-118">_lppEntry_</span></span>
  
> <span data-ttu-id="7cf2f-119">[out]開かれたオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7cf2f-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7cf2f-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="7cf2f-120">Return value</span></span>

<span data-ttu-id="7cf2f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="7cf2f-121">S_OK</span></span> 
  
> <span data-ttu-id="7cf2f-122">呼び出しが成功し、状態オブジェクトが開かれています。</span><span class="sxs-lookup"><span data-stu-id="7cf2f-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7cf2f-123">注釈</span><span class="sxs-lookup"><span data-stu-id="7cf2f-123">Remarks</span></span>

<span data-ttu-id="7cf2f-124">アドレス帳プロバイダーは、その状態のオブジェクトへのアクセスを許可する**OpenStatusEntry**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="7cf2f-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="7cf2f-125">すべてのアドレス帳プロバイダーは、最低限、 [IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドがサポートする状態オブジェクトを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cf2f-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="7cf2f-126">詳細については、[状態オブジェクトの実装](status-object-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cf2f-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7cf2f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="7cf2f-127">See also</span></span>



[<span data-ttu-id="7cf2f-128">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7cf2f-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="7cf2f-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="7cf2f-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="7cf2f-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="7cf2f-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="7cf2f-131">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7cf2f-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

