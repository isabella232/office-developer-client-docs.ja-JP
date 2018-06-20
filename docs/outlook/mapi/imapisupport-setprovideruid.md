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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2182ec71c54c81e9a43a34973e005292ddccdfff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800792"
---
# <a name="imapisupportsetprovideruid"></a><span data-ttu-id="b0028-103">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="b0028-103">IMAPISupport::SetProviderUID</span></span>

  
  
<span data-ttu-id="b0028-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0028-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0028-105">サービス プロバイダーを一意に表す[MAPIUID](mapiuid.md)構造体を登録します。</span><span class="sxs-lookup"><span data-stu-id="b0028-105">Registers a [MAPIUID](mapiuid.md) structure that uniquely represents the service provider.</span></span> 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b0028-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b0028-106">Parameters</span></span>

 <span data-ttu-id="b0028-107">_lpProviderID_</span><span class="sxs-lookup"><span data-stu-id="b0028-107">_lpProviderID_</span></span>
  
> <span data-ttu-id="b0028-108">[in]アドレス帳またはメッセージ ストア プロバイダーを識別する**MAPIUID**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b0028-108">[in] A pointer to the **MAPIUID** structure that identifies the address book or message store provider.</span></span> 
    
 <span data-ttu-id="b0028-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b0028-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b0028-110">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0028-110">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b0028-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b0028-111">Return value</span></span>

<span data-ttu-id="b0028-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0028-112">S_OK</span></span> 
  
> <span data-ttu-id="b0028-113">**MAPIUID**構造体は正常に登録されました。</span><span class="sxs-lookup"><span data-stu-id="b0028-113">The **MAPIUID** structure was successfully registered.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b0028-114">備考</span><span class="sxs-lookup"><span data-stu-id="b0028-114">Remarks</span></span>

<span data-ttu-id="b0028-115">アドレス帳、メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::SetProviderUID**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="b0028-115">The **IMAPISupport::SetProviderUID** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="b0028-116">これらのプロバイダーは、 _lpProviderID_に設定されている**MAPIUID**構造体で記載されている一意の識別子を登録するのには**SetProviderUID**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b0028-116">These providers call **SetProviderUID** to register a unique identifier described in the **MAPIUID** structure that is pointed to by  _lpProviderID_.</span></span> <span data-ttu-id="b0028-117">プロバイダーには、すべてのエントリの識別子を作成するのにこの識別子が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b0028-117">Providers include this identifier in all of the entry identifiers that they create.</span></span> 
  
<span data-ttu-id="b0028-118">MAPI は、MAPI スプーラーを無効にし、クライアントの要求を処理するための適切なプロバイダーを確認するのには送信メッセージを送信するときに、 **MAPIUID**構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="b0028-118">MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests.</span></span> <span data-ttu-id="b0028-119">たとえば、クライアントは、 [IMAPISession::OpenEntry](imapisession-openentry.md)メソッドを呼び出すと、MAPI、 **MAPIUID**の部分のエントリ id を調べ、 **SetProviderUID**に渡されることと、そのプロバイダーの**OpenEntry**を呼び出すためのプロバイダーにマップ.</span><span class="sxs-lookup"><span data-stu-id="b0028-119">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method, MAPI examines the **MAPIUID** portion of the entry identifier, maps it to the provider that passed it to **SetProviderUID**, and calls that provider's **OpenEntry**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b0028-120">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b0028-120">Notes to callers</span></span>

<span data-ttu-id="b0028-121">**MAPIUID**構造体を登録するのにはログオン時に**SetProviderUID**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b0028-121">Call **SetProviderUID** at logon time to register your **MAPIUID** structure.</span></span> <span data-ttu-id="b0028-122">MAPI では、複数の識別子を登録するのには、アドレス帳、メッセージ ストア プロバイダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b0028-122">MAPI allows address book and message store providers to register multiple identifiers.</span></span> <span data-ttu-id="b0028-123">**SetProviderUID**に複数の呼び出しの際に、常に**MAPIUID**構造体に追加プロバイダーのセットを**MAPIUID**構造体の**MAPIUID**は、重複している場合でも。</span><span class="sxs-lookup"><span data-stu-id="b0028-123">When you make multiple calls to **SetProviderUID**, it always adds the **MAPIUID** structure to the provider's set of **MAPIUID** structures, even if the **MAPIUID** is a duplicate.</span></span> <span data-ttu-id="b0028-124">**SetProviderUID**は、 **MAPIUID**を削除できません。</span><span class="sxs-lookup"><span data-stu-id="b0028-124">**SetProviderUID** cannot remove a **MAPIUID**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b0028-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0028-125">See also</span></span>



[<span data-ttu-id="b0028-126">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="b0028-126">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="b0028-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0028-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

