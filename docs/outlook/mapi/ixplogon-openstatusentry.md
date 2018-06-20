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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0e96c0b99f0a5f7511ed59b483ab9409eafad882
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801249"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="b7ce9-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="b7ce9-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="b7ce9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7ce9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7ce9-105">トランスポート プロバイダーの状態のオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="b7ce9-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="b7ce9-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b7ce9-106">Parameters</span></span>

 <span data-ttu-id="b7ce9-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b7ce9-107">_lpInterface_</span></span>
  
> <span data-ttu-id="b7ce9-108">[in]トランスポート ログオン オブジェクトのインターフェイス id (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b7ce9-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="b7ce9-109">[IMAPIStatus](imapistatusimapiprop.md)インターフェイスを返します NULL を渡すことです。</span><span class="sxs-lookup"><span data-stu-id="b7ce9-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="b7ce9-110">_LpInterface_パラメーターは、オブジェクトのインターフェイスの識別子を設定することも。</span><span class="sxs-lookup"><span data-stu-id="b7ce9-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="b7ce9-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b7ce9-111">_ulFlags_</span></span>
  
> <span data-ttu-id="b7ce9-112">[in]状態オブジェクトを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="b7ce9-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="b7ce9-113">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="b7ce9-113">The following flag can be set:</span></span>
    
<span data-ttu-id="b7ce9-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b7ce9-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="b7ce9-115">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="b7ce9-115">Requests read/write permission.</span></span> <span data-ttu-id="b7ce9-116">デフォルトのインタ フェースは、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="b7ce9-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="b7ce9-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="b7ce9-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="b7ce9-118">[out]開かれたオブジェクトの型へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b7ce9-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="b7ce9-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="b7ce9-119">_lppEntry_</span></span>
  
> <span data-ttu-id="b7ce9-120">[out]開かれた状態のオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b7ce9-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b7ce9-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b7ce9-121">Return value</span></span>

<span data-ttu-id="b7ce9-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7ce9-122">S_OK</span></span> 
  
> <span data-ttu-id="b7ce9-123">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="b7ce9-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7ce9-124">備考</span><span class="sxs-lookup"><span data-stu-id="b7ce9-124">Remarks</span></span>

<span data-ttu-id="b7ce9-125">MAPI スプーラーは、クライアント アプリケーションは、トランスポート プロバイダーの状態のテーブルの行のエントリ id の**OpenEntry**メソッドを呼び出すときに、 **IXPLogon::OpenStatusEntry**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b7ce9-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="b7ce9-126">**OpenStatusEntry**は、この特定のトランスポート プロバイダーへのログオンに関連付けられている**IMAPIStatus**インターフェイスを持つオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="b7ce9-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="b7ce9-127">(たとえば、 [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドを使用してログオン セッションを再構成するか、[を使用してログオン セッションの状態を検証するために**IMAPIStatus**メソッドを呼び出すクライアント アプリケーションを有効にするのにはこのオブジェクトを使用してIMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッド)。</span><span class="sxs-lookup"><span data-stu-id="b7ce9-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b7ce9-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7ce9-128">See also</span></span>



[<span data-ttu-id="b7ce9-129">IMAPIStatus: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b7ce9-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="b7ce9-130">IXPLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7ce9-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

