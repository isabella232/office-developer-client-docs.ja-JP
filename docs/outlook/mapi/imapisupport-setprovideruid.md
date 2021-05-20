---
title: IMAPISupportSetProviderUID
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
# <a name="imapisupportsetprovideruid"></a><span data-ttu-id="73c43-103">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="73c43-103">IMAPISupport::SetProviderUID</span></span>

  
  
<span data-ttu-id="73c43-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73c43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73c43-105">サービス プロバイダーを [一意に表す MAPIUID](mapiuid.md) 構造体を登録します。</span><span class="sxs-lookup"><span data-stu-id="73c43-105">Registers a [MAPIUID](mapiuid.md) structure that uniquely represents the service provider.</span></span> 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="73c43-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="73c43-106">Parameters</span></span>

 <span data-ttu-id="73c43-107">_lpProviderID_</span><span class="sxs-lookup"><span data-stu-id="73c43-107">_lpProviderID_</span></span>
  
> <span data-ttu-id="73c43-108">[in]アドレス帳またはメッセージ ストア プロバイダーを識別する **MAPIUID** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="73c43-108">[in] A pointer to the **MAPIUID** structure that identifies the address book or message store provider.</span></span> 
    
 <span data-ttu-id="73c43-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="73c43-109">_ulFlags_</span></span>
  
> <span data-ttu-id="73c43-110">予約済み。は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="73c43-110">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="73c43-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="73c43-111">Return value</span></span>

<span data-ttu-id="73c43-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="73c43-112">S_OK</span></span> 
  
> <span data-ttu-id="73c43-113">**MAPIUID 構造** が正常に登録されました。</span><span class="sxs-lookup"><span data-stu-id="73c43-113">The **MAPIUID** structure was successfully registered.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="73c43-114">注釈</span><span class="sxs-lookup"><span data-stu-id="73c43-114">Remarks</span></span>

<span data-ttu-id="73c43-115">**IMAPISupport::SetProviderUID** メソッドは、アドレス帳およびメッセージ ストア プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="73c43-115">The **IMAPISupport::SetProviderUID** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="73c43-116">これらのプロバイダーは **SetProviderUID** を呼び出して _、lpProviderID_ によって指される **MAPIUID** 構造で説明されている一意の識別子を登録します。</span><span class="sxs-lookup"><span data-stu-id="73c43-116">These providers call **SetProviderUID** to register a unique identifier described in the **MAPIUID** structure that is pointed to by  _lpProviderID_.</span></span> <span data-ttu-id="73c43-117">プロバイダーは、この識別子を作成するエントリ識別子のすべてに含まれます。</span><span class="sxs-lookup"><span data-stu-id="73c43-117">Providers include this identifier in all of the entry identifiers that they create.</span></span> 
  
<span data-ttu-id="73c43-118">MAPI は **、MAPI スプーラー** に送信メッセージを送信するときに MAPIUID 構造を使用し、クライアント要求を処理する適切なプロバイダーを決定します。</span><span class="sxs-lookup"><span data-stu-id="73c43-118">MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests.</span></span> <span data-ttu-id="73c43-119">たとえば、クライアントが [IMAPISession::OpenEntry](imapisession-openentry.md) メソッドを呼び出す場合、MAPI はエントリ識別子の **MAPIUID** 部分を調べ、それを **SetProviderUID** に渡したプロバイダーにマップし、そのプロバイダーの **OpenEntry** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="73c43-119">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method, MAPI examines the **MAPIUID** portion of the entry identifier, maps it to the provider that passed it to **SetProviderUID**, and calls that provider's **OpenEntry**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="73c43-120">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="73c43-120">Notes to callers</span></span>

<span data-ttu-id="73c43-121">**ログオン時に SetProviderUID** を呼び出して **、MAPIUID 構造を登録** します。</span><span class="sxs-lookup"><span data-stu-id="73c43-121">Call **SetProviderUID** at logon time to register your **MAPIUID** structure.</span></span> <span data-ttu-id="73c43-122">MAPI を使用すると、アドレス帳とメッセージ ストア プロバイダーは複数の識別子を登録できます。</span><span class="sxs-lookup"><span data-stu-id="73c43-122">MAPI allows address book and message store providers to register multiple identifiers.</span></span> <span data-ttu-id="73c43-123">**SetProviderUID** を複数呼び出す場合は **、MAPIUID** が重複している場合でも、常に **MAPIUID** 構造体をプロバイダーの MAPIUID 構造体のセットに追加します。</span><span class="sxs-lookup"><span data-stu-id="73c43-123">When you make multiple calls to **SetProviderUID**, it always adds the **MAPIUID** structure to the provider's set of **MAPIUID** structures, even if the **MAPIUID** is a duplicate.</span></span> <span data-ttu-id="73c43-124">**SetProviderUID は** **MAPIUID を削除できません**。</span><span class="sxs-lookup"><span data-stu-id="73c43-124">**SetProviderUID** cannot remove a **MAPIUID**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73c43-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="73c43-125">See also</span></span>



[<span data-ttu-id="73c43-126">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="73c43-126">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="73c43-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="73c43-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

