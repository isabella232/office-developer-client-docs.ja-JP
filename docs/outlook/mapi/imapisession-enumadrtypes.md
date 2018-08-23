---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 050068b542616d1ad4d133b289aba46db2888519
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587818"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="1a0c7-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="1a0c7-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="1a0c7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a0c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a0c7-105">現在は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="1a0c7-105">Deprecated.</span></span> <span data-ttu-id="1a0c7-106">セッション内のすべてのトランスポート プロバイダーによって処理可能なアドレスの種類を返します。</span><span class="sxs-lookup"><span data-stu-id="1a0c7-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="1a0c7-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="1a0c7-107">Parameters</span></span>

 <span data-ttu-id="1a0c7-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1a0c7-108">_ulFlags_</span></span>
  
> <span data-ttu-id="1a0c7-109">[in]返されるアドレスの種類の形式を示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="1a0c7-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="1a0c7-110">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1a0c7-110">The following flag can be set:</span></span>
    
<span data-ttu-id="1a0c7-111">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1a0c7-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1a0c7-112">Unicode 形式では、アドレスの種類です。</span><span class="sxs-lookup"><span data-stu-id="1a0c7-112">The address types are in Unicode format.</span></span> <span data-ttu-id="1a0c7-113">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のアドレスの種類です。</span><span class="sxs-lookup"><span data-stu-id="1a0c7-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="1a0c7-114">_lpcAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="1a0c7-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="1a0c7-115">[out]_LpppszAdrTypes_パラメーターが指すアドレスの種類の数へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="1a0c7-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="1a0c7-116">_lpppszAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="1a0c7-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="1a0c7-117">[out]アドレスの種類へのポインターの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1a0c7-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a0c7-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1a0c7-118">Return value</span></span>

<span data-ttu-id="1a0c7-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a0c7-119">S_OK</span></span> 
  
> <span data-ttu-id="1a0c7-120">アドレスの種類が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="1a0c7-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a0c7-121">注釈</span><span class="sxs-lookup"><span data-stu-id="1a0c7-121">Remarks</span></span>

<span data-ttu-id="1a0c7-122">**IMAPISession::EnumAdrTypes**メソッドは、セッション内のすべてのアクティブなトランスポート プロバイダーによって処理可能なアドレスの種類のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="1a0c7-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="1a0c7-123">現在読み込まれていないトランスポート プロバイダーのアドレスの種類は、一覧には含まれません。</span><span class="sxs-lookup"><span data-stu-id="1a0c7-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="1a0c7-124">MAPI は、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すと、1 つまたは複数のアドレスの種類を処理するトランスポート プロバイダーを登録します。</span><span class="sxs-lookup"><span data-stu-id="1a0c7-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1a0c7-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="1a0c7-125">Notes to callers</span></span>

<span data-ttu-id="1a0c7-126">_LpppszAdrTypes_パラメーターが指す文字列の配列を解放するのには[MAPIFreeBuffer](mapifreebuffer.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1a0c7-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a0c7-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a0c7-127">See also</span></span>



[<span data-ttu-id="1a0c7-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="1a0c7-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="1a0c7-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1a0c7-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1a0c7-130">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a0c7-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

