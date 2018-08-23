---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e061808c57f25f881cc17fa5251e46ed5d524acd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801199"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="0d982-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0d982-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="0d982-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d982-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d982-105">最後のエラーに関する情報を拡張します。</span><span class="sxs-lookup"><span data-stu-id="0d982-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="0d982-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d982-106">Parameters</span></span>

 <span data-ttu-id="0d982-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="0d982-107">_hResult_</span></span>
  
>  <span data-ttu-id="0d982-108">[in]エラー コードです。</span><span class="sxs-lookup"><span data-stu-id="0d982-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="0d982-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0d982-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="0d982-110">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="0d982-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="0d982-111">0 でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="0d982-111">This must be 0.</span></span> 
    
 <span data-ttu-id="0d982-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="0d982-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="0d982-113">[out]エラーに関する拡張情報を格納する**MAPIERROR**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0d982-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="0d982-114">**LPMAPIERROR**の型の定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d982-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0d982-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d982-115">See also</span></span>



[<span data-ttu-id="0d982-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="0d982-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="0d982-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="0d982-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

