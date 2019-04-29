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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439290"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="5432c-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="5432c-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="5432c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5432c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5432c-105">現在は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="5432c-105">Deprecated.</span></span> <span data-ttu-id="5432c-106">セッション内のすべてのトランスポートプロバイダーで処理できるアドレスの種類を返します。</span><span class="sxs-lookup"><span data-stu-id="5432c-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="5432c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5432c-107">Parameters</span></span>

 <span data-ttu-id="5432c-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5432c-108">_ulFlags_</span></span>
  
> <span data-ttu-id="5432c-109">順番返されるアドレスの種類の形式を示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="5432c-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="5432c-110">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5432c-110">The following flag can be set:</span></span>
    
<span data-ttu-id="5432c-111">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5432c-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5432c-112">アドレスの種類は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="5432c-112">The address types are in Unicode format.</span></span> <span data-ttu-id="5432c-113">MAPI_UNICODE フラグが設定されていない場合、アドレスの種類は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="5432c-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="5432c-114">_lpcAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="5432c-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="5432c-115">読み上げ_lpppszadrtypes_パラメーターが指すアドレスの種類の数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5432c-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="5432c-116">_lpppszadrtypes_</span><span class="sxs-lookup"><span data-stu-id="5432c-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="5432c-117">読み上げアドレスの種類へのポインターの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5432c-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5432c-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="5432c-118">Return value</span></span>

<span data-ttu-id="5432c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="5432c-119">S_OK</span></span> 
  
> <span data-ttu-id="5432c-120">アドレスの種類が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="5432c-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5432c-121">注釈</span><span class="sxs-lookup"><span data-stu-id="5432c-121">Remarks</span></span>

<span data-ttu-id="5432c-122">**imapisession:: enumadrtypes**メソッドは、セッション内のすべてのアクティブなトランスポートプロバイダーによって処理できるアドレスの種類の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="5432c-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="5432c-123">現在読み込まれていないトランスポートプロバイダーのアドレスの種類は、一覧に含まれていません。</span><span class="sxs-lookup"><span data-stu-id="5432c-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="5432c-124">トランスポートプロバイダーは、MAPI が[IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すときに、1つまたは複数のアドレスの種類を処理するように登録します。</span><span class="sxs-lookup"><span data-stu-id="5432c-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5432c-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5432c-125">Notes to callers</span></span>

<span data-ttu-id="5432c-126">[MAPIFreeBuffer](mapifreebuffer.md)を呼び出して、 _lpppszadrtypes_パラメーターで指定された文字列配列を解放します。</span><span class="sxs-lookup"><span data-stu-id="5432c-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5432c-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="5432c-127">See also</span></span>



[<span data-ttu-id="5432c-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="5432c-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="5432c-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5432c-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5432c-130">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5432c-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

