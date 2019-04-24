---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d9e09de1064a0ae034bb3618f0e5b3719a82c163
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356029"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="4ad49-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="4ad49-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="4ad49-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ad49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ad49-105">トランスポートプロバイダーの状態オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="4ad49-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="4ad49-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4ad49-106">Parameters</span></span>

 <span data-ttu-id="4ad49-107">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="4ad49-107">_lpInterface_</span></span>
  
> <span data-ttu-id="4ad49-108">順番トランスポートログオンオブジェクトのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4ad49-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="4ad49-109">NULL を渡すと、 [imapistatus](imapistatusimapiprop.md)インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="4ad49-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="4ad49-110">_lpinterface_パラメーターは、オブジェクトのインターフェイスの識別子に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="4ad49-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="4ad49-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4ad49-111">_ulFlags_</span></span>
  
> <span data-ttu-id="4ad49-112">順番status オブジェクトが開かれる方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="4ad49-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="4ad49-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4ad49-113">The following flag can be set:</span></span>
    
<span data-ttu-id="4ad49-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="4ad49-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="4ad49-115">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="4ad49-115">Requests read/write permission.</span></span> <span data-ttu-id="4ad49-116">既定のインターフェイスは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="4ad49-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="4ad49-117">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="4ad49-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="4ad49-118">読み上げ開かれているオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4ad49-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="4ad49-119">_lppentry_</span><span class="sxs-lookup"><span data-stu-id="4ad49-119">_lppEntry_</span></span>
  
> <span data-ttu-id="4ad49-120">読み上げ開かれた状態オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4ad49-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4ad49-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="4ad49-121">Return value</span></span>

<span data-ttu-id="4ad49-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="4ad49-122">S_OK</span></span> 
  
> <span data-ttu-id="4ad49-123">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="4ad49-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4ad49-124">解説</span><span class="sxs-lookup"><span data-stu-id="4ad49-124">Remarks</span></span>

<span data-ttu-id="4ad49-125">クライアントアプリケーションがトランスポートプロバイダーの状態テーブルの行のエントリ id に対して**openentry**メソッドを呼び出すと、MAPI スプーラーは**IXPLogon:: openstatusentry**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4ad49-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="4ad49-126">**openstatusentry**この特定のトランスポートプロバイダーログオンに関連付けられている**imapistatus**インターフェイスを持つオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="4ad49-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="4ad49-127">次に、このオブジェクトを使用して、クライアントアプリケーションが**imapistatus**メソッドを呼び出すことができるようにします (たとえば、 [imapistatus:: settingsdialog](imapistatus-settingsdialog.md)メソッドを使用してログオンセッションを再構成する場合、またはを使用[してログオンセッションの状態を確認する場合など)。imapistatus:: validatestate](imapistatus-validatestate.md)メソッド)。</span><span class="sxs-lookup"><span data-stu-id="4ad49-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4ad49-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ad49-128">See also</span></span>



[<span data-ttu-id="4ad49-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4ad49-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="4ad49-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4ad49-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

