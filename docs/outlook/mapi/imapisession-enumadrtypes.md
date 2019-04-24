---
title: imapisessionenumadrtypes
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3b2e41c4b1bfc4879717df0c73bbcd45a724ca60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338438"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="94500-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="94500-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="94500-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94500-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94500-105">現在は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="94500-105">Deprecated.</span></span> <span data-ttu-id="94500-106">セッション内のすべてのトランスポートプロバイダーで処理できるアドレスの種類を返します。</span><span class="sxs-lookup"><span data-stu-id="94500-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="94500-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="94500-107">Parameters</span></span>

 <span data-ttu-id="94500-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="94500-108">_ulFlags_</span></span>
  
> <span data-ttu-id="94500-109">順番返されるアドレスの種類の形式を示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="94500-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="94500-110">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="94500-110">The following flag can be set:</span></span>
    
<span data-ttu-id="94500-111">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="94500-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="94500-112">アドレスの種類は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="94500-112">The address types are in Unicode format.</span></span> <span data-ttu-id="94500-113">MAPI_UNICODE フラグが設定されていない場合、アドレスの種類は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="94500-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="94500-114">_lpcAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="94500-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="94500-115">読み上げ_lpppszadrtypes_パラメーターが指すアドレスの種類の数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="94500-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="94500-116">_lpppszadrtypes_</span><span class="sxs-lookup"><span data-stu-id="94500-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="94500-117">読み上げアドレスの種類へのポインターの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="94500-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="94500-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="94500-118">Return value</span></span>

<span data-ttu-id="94500-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="94500-119">S_OK</span></span> 
  
> <span data-ttu-id="94500-120">アドレスの種類が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="94500-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="94500-121">解説</span><span class="sxs-lookup"><span data-stu-id="94500-121">Remarks</span></span>

<span data-ttu-id="94500-122">**imapisession:: enumadrtypes**メソッドは、セッション内のすべてのアクティブなトランスポートプロバイダーによって処理できるアドレスの種類の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="94500-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="94500-123">現在読み込まれていないトランスポートプロバイダーのアドレスの種類は、一覧に含まれていません。</span><span class="sxs-lookup"><span data-stu-id="94500-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="94500-124">トランスポートプロバイダーは、MAPI が[IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すときに、1つまたは複数のアドレスの種類を処理するように登録します。</span><span class="sxs-lookup"><span data-stu-id="94500-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="94500-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="94500-125">Notes to callers</span></span>

<span data-ttu-id="94500-126">[MAPIFreeBuffer](mapifreebuffer.md)を呼び出して、 _lpppszadrtypes_パラメーターで指定された文字列配列を解放します。</span><span class="sxs-lookup"><span data-stu-id="94500-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94500-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="94500-127">See also</span></span>



[<span data-ttu-id="94500-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="94500-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="94500-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="94500-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="94500-130">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="94500-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

