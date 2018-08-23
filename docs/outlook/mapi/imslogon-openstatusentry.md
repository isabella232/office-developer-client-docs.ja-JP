---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a48d8248878c64de827bb09030073e6becba3024
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571200"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="2e2d7-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="2e2d7-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="2e2d7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e2d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e2d7-105">状態オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e2d7-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="2e2d7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2e2d7-106">Parameters</span></span>

 <span data-ttu-id="2e2d7-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="2e2d7-107">_lpInterface_</span></span>
  
> <span data-ttu-id="2e2d7-108">[in]開くには、状態オブジェクトのインターフェイス id (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2e2d7-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="2e2d7-109">NULL を渡すことを示します (ここでは、 [IMAPIStatus](imapistatusimapiprop.md)インターフェイス) オブジェクトの標準的なインターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="2e2d7-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="2e2d7-110">_LpInterface_パラメーターは、オブジェクトの適切なインターフェイスの識別子を設定することも。</span><span class="sxs-lookup"><span data-stu-id="2e2d7-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="2e2d7-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2e2d7-111">_ulFlags_</span></span>
  
> <span data-ttu-id="2e2d7-112">[in]状態オブジェクトを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="2e2d7-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="2e2d7-113">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="2e2d7-113">The following flag can be set:</span></span>
    
<span data-ttu-id="2e2d7-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="2e2d7-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="2e2d7-115">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="2e2d7-115">Requests read/write permission.</span></span> <span data-ttu-id="2e2d7-116">既定では、読み取り専用の権限を持つオブジェクトが作成およびクライアント アプリケーションは読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e2d7-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="2e2d7-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="2e2d7-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="2e2d7-118">[out]開かれたオブジェクトの型へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2e2d7-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="2e2d7-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="2e2d7-119">_lppEntry_</span></span>
  
> <span data-ttu-id="2e2d7-120">[out]開かれたオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2e2d7-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2e2d7-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="2e2d7-121">Return value</span></span>

<span data-ttu-id="2e2d7-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="2e2d7-122">S_OK</span></span> 
  
> <span data-ttu-id="2e2d7-123">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="2e2d7-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2e2d7-124">����</span><span class="sxs-lookup"><span data-stu-id="2e2d7-124">Remarks</span></span>

<span data-ttu-id="2e2d7-125">メッセージ ストア プロバイダーは、状態オブジェクトを開くには、 **IMSLogon::OpenStatusEntry**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="2e2d7-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="2e2d7-126">[IMAPIStatus](imapistatusimapiprop.md)メソッドを呼び出すクライアントを有効にするこの状態のオブジェクトを使用しています。</span><span class="sxs-lookup"><span data-stu-id="2e2d7-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="2e2d7-127">たとえば、クライアントは、メッセージ ストアのログオン セッションまたはメッセージ ストアのログオン セッションの状態を検証するために[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドを再構成するのには、 [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2e2d7-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2e2d7-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e2d7-128">See also</span></span>



[<span data-ttu-id="2e2d7-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2e2d7-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="2e2d7-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="2e2d7-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="2e2d7-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="2e2d7-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="2e2d7-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e2d7-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

