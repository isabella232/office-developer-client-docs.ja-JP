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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435902"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="47b5c-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="47b5c-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="47b5c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47b5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47b5c-105">トランスポート プロバイダーの状態オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="47b5c-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="47b5c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="47b5c-106">Parameters</span></span>

 <span data-ttu-id="47b5c-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="47b5c-107">_lpInterface_</span></span>
  
> <span data-ttu-id="47b5c-108">[in]トランスポート ログオン オブジェクトのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="47b5c-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="47b5c-109">NULL を渡すと [、IMAPIStatus インターフェイスが返](imapistatusimapiprop.md) されます。</span><span class="sxs-lookup"><span data-stu-id="47b5c-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="47b5c-110">_lpInterface パラメーター_ は、オブジェクトのインターフェイスの識別子に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="47b5c-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="47b5c-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="47b5c-111">_ulFlags_</span></span>
  
> <span data-ttu-id="47b5c-112">[in]status オブジェクトの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="47b5c-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="47b5c-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="47b5c-113">The following flag can be set:</span></span>
    
<span data-ttu-id="47b5c-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="47b5c-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="47b5c-115">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="47b5c-115">Requests read/write permission.</span></span> <span data-ttu-id="47b5c-116">既定のインターフェイスは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="47b5c-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="47b5c-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="47b5c-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="47b5c-118">[out]開いたオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="47b5c-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="47b5c-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="47b5c-119">_lppEntry_</span></span>
  
> <span data-ttu-id="47b5c-120">[out]開いた状態オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="47b5c-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47b5c-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="47b5c-121">Return value</span></span>

<span data-ttu-id="47b5c-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="47b5c-122">S_OK</span></span> 
  
> <span data-ttu-id="47b5c-123">呼び出しは成功し、予期される値または値を返しました。</span><span class="sxs-lookup"><span data-stu-id="47b5c-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47b5c-124">注釈</span><span class="sxs-lookup"><span data-stu-id="47b5c-124">Remarks</span></span>

<span data-ttu-id="47b5c-125">MAPI スプーラーは、クライアント アプリケーションがトランスポート プロバイダーの状態テーブル行のエントリ識別子の **OpenEntry** メソッドを呼び出す場合に **、IXPLogon::OpenStatusEntry** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="47b5c-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="47b5c-126">**OpenStatusEntry は、** この特定のトランスポート プロバイダーログオンに関連付けられた **IMAPIStatus** インターフェイスを持つオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="47b5c-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="47b5c-127">次に、このオブジェクトを使用して、クライアント アプリケーションが **IMAPIStatus** メソッドを呼び出す (たとえば [、IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) メソッドを使用してログオン セッションを再構成したり [、IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドを使用してログオン セッションの状態を検証したりするために使用されます)。</span><span class="sxs-lookup"><span data-stu-id="47b5c-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47b5c-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="47b5c-128">See also</span></span>



[<span data-ttu-id="47b5c-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="47b5c-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="47b5c-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47b5c-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

