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
ms.openlocfilehash: f45b070464fe1b3c177088ff6aa3295f961d45f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592592"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="f2eb1-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f2eb1-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="f2eb1-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2eb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2eb1-105">最後のエラーに関する情報を拡張します。</span><span class="sxs-lookup"><span data-stu-id="f2eb1-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="f2eb1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f2eb1-106">Parameters</span></span>

 <span data-ttu-id="f2eb1-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="f2eb1-107">_hResult_</span></span>
  
>  <span data-ttu-id="f2eb1-108">[in]エラー コードです。</span><span class="sxs-lookup"><span data-stu-id="f2eb1-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="f2eb1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f2eb1-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="f2eb1-110">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="f2eb1-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="f2eb1-111">0 でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f2eb1-111">This must be 0.</span></span> 
    
 <span data-ttu-id="f2eb1-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="f2eb1-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="f2eb1-113">[out]エラーに関する拡張情報を格納する**MAPIERROR**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f2eb1-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="f2eb1-114">**LPMAPIERROR**の型の定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2eb1-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f2eb1-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2eb1-115">See also</span></span>



[<span data-ttu-id="f2eb1-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="f2eb1-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="f2eb1-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="f2eb1-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

