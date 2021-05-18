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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f50c0eb9e3af68e206eaa5bcc51cefa923c30f72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413179"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="fa3a2-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="fa3a2-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="fa3a2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa3a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa3a2-105">状態オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="fa3a2-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="fa3a2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fa3a2-106">Parameters</span></span>

 <span data-ttu-id="fa3a2-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="fa3a2-107">_lpInterface_</span></span>
  
> <span data-ttu-id="fa3a2-108">[in]status オブジェクトを開くインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fa3a2-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="fa3a2-109">NULL を渡す場合は、オブジェクトの標準インターフェイスが返されます (この場合は [IMAPIStatus](imapistatusimapiprop.md) インターフェイス)。</span><span class="sxs-lookup"><span data-stu-id="fa3a2-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="fa3a2-110">_lpInterface パラメーター_ は、オブジェクトの適切なインターフェイスの識別子に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="fa3a2-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="fa3a2-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fa3a2-111">_ulFlags_</span></span>
  
> <span data-ttu-id="fa3a2-112">[in]status オブジェクトの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="fa3a2-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="fa3a2-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="fa3a2-113">The following flag can be set:</span></span>
    
<span data-ttu-id="fa3a2-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="fa3a2-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="fa3a2-115">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="fa3a2-115">Requests read/write permission.</span></span> <span data-ttu-id="fa3a2-116">既定では、オブジェクトは読み取り専用のアクセス許可で作成され、クライアント アプリケーションは、読み取り/書き込みアクセス許可が付与されているという前提で動作しません。</span><span class="sxs-lookup"><span data-stu-id="fa3a2-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="fa3a2-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="fa3a2-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="fa3a2-118">[out]開いたオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fa3a2-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="fa3a2-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="fa3a2-119">_lppEntry_</span></span>
  
> <span data-ttu-id="fa3a2-120">[out]開いたオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fa3a2-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fa3a2-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="fa3a2-121">Return value</span></span>

<span data-ttu-id="fa3a2-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa3a2-122">S_OK</span></span> 
  
> <span data-ttu-id="fa3a2-123">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="fa3a2-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa3a2-124">注釈</span><span class="sxs-lookup"><span data-stu-id="fa3a2-124">Remarks</span></span>

<span data-ttu-id="fa3a2-125">メッセージ ストア プロバイダーは、状態オブジェクトを開く **IMSLogon::OpenStatusEntry** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="fa3a2-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="fa3a2-126">この状態オブジェクトは、クライアントが [IMAPIStatus メソッドを呼び出すのを有効に](imapistatusimapiprop.md) するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa3a2-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="fa3a2-127">たとえば、クライアントは [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) メソッドを使用してメッセージ ストア ログオン セッションを再構成したり [、IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドを使用してメッセージ ストア ログオン セッションの状態を検証できます。</span><span class="sxs-lookup"><span data-stu-id="fa3a2-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa3a2-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa3a2-128">See also</span></span>



[<span data-ttu-id="fa3a2-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fa3a2-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="fa3a2-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="fa3a2-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="fa3a2-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="fa3a2-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="fa3a2-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa3a2-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

