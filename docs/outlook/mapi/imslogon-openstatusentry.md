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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348700"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="a49fc-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="a49fc-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="a49fc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a49fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a49fc-105">status オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="a49fc-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="a49fc-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a49fc-106">Parameters</span></span>

 <span data-ttu-id="a49fc-107">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="a49fc-107">_lpInterface_</span></span>
  
> <span data-ttu-id="a49fc-108">順番開く状態オブジェクトのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a49fc-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="a49fc-109">NULL を渡すと、オブジェクトの標準インターフェイスが返されます (この場合は[imapistatus](imapistatusimapiprop.md)インターフェイス)。</span><span class="sxs-lookup"><span data-stu-id="a49fc-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="a49fc-110">_lpinterface_パラメーターは、オブジェクトの適切なインターフェイスの識別子に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="a49fc-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="a49fc-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a49fc-111">_ulFlags_</span></span>
  
> <span data-ttu-id="a49fc-112">順番status オブジェクトが開かれる方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a49fc-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="a49fc-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a49fc-113">The following flag can be set:</span></span>
    
<span data-ttu-id="a49fc-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a49fc-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="a49fc-115">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="a49fc-115">Requests read/write permission.</span></span> <span data-ttu-id="a49fc-116">既定では、オブジェクトは読み取り専用のアクセス許可で作成され、読み取り/書き込みアクセス許可が与えられているという前提でクライアントアプリケーションを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="a49fc-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="a49fc-117">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="a49fc-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="a49fc-118">読み上げ開かれているオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a49fc-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="a49fc-119">_lppentry_</span><span class="sxs-lookup"><span data-stu-id="a49fc-119">_lppEntry_</span></span>
  
> <span data-ttu-id="a49fc-120">読み上げ開かれているオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a49fc-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a49fc-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="a49fc-121">Return value</span></span>

<span data-ttu-id="a49fc-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a49fc-122">S_OK</span></span> 
  
> <span data-ttu-id="a49fc-123">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a49fc-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a49fc-124">解説</span><span class="sxs-lookup"><span data-stu-id="a49fc-124">Remarks</span></span>

<span data-ttu-id="a49fc-125">メッセージストアプロバイダーは、status オブジェクトを開くために**IMSLogon:: openstatusentry**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="a49fc-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="a49fc-126">この状態オブジェクトは、クライアントが[imapistatus](imapistatusimapiprop.md)メソッドを呼び出せるようにするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a49fc-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="a49fc-127">たとえば、クライアントは[imapistatus:: settingsdialog](imapistatus-settingsdialog.md)メソッドを使用して、メッセージストアログオンセッションまたは[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドを再構成し、メッセージストアログオンセッションの状態を検証することができます。</span><span class="sxs-lookup"><span data-stu-id="a49fc-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a49fc-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="a49fc-128">See also</span></span>



[<span data-ttu-id="a49fc-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a49fc-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="a49fc-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="a49fc-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="a49fc-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="a49fc-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="a49fc-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a49fc-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

