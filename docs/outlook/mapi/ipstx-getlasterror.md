---
title: ipstxgetlasterror
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1d0fb16ba63548a44dba3920670c0e65f8c700a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315100"
---
# <a name="ipstxgetlasterror"></a><span data-ttu-id="988cd-103">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="988cd-103">IPSTX::GetLastError</span></span>

  
  
<span data-ttu-id="988cd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="988cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="988cd-105">最新のエラーに関する拡張情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="988cd-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="988cd-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="988cd-106">Parameters</span></span>

 <span data-ttu-id="988cd-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="988cd-107">_hResult_</span></span>
  
>  <span data-ttu-id="988cd-108">順番エラーコード。</span><span class="sxs-lookup"><span data-stu-id="988cd-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="988cd-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="988cd-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="988cd-110">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="988cd-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="988cd-111">これは0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="988cd-111">This must be 0.</span></span> 
    
 <span data-ttu-id="988cd-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="988cd-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="988cd-113">読み上げエラーの拡張情報を含む**MAPIERROR**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="988cd-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="988cd-114">**LPMAPIERROR**の型定義については、「mapidefs.h」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="988cd-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="988cd-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="988cd-115">See also</span></span>



[<span data-ttu-id="988cd-116">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="988cd-116">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="988cd-117">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="988cd-117">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

