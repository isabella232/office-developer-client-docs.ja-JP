---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8d5d4895e4440945896ee4f2212c5fca6da8610d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424512"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="166bb-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="166bb-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="166bb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="166bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="166bb-105">table オブジェクトで発生した最後のエラーについての情報を返します。</span><span class="sxs-lookup"><span data-stu-id="166bb-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="166bb-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="166bb-106">Parameters</span></span>

 <span data-ttu-id="166bb-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="166bb-107">_hResult_</span></span>
  
> <span data-ttu-id="166bb-108">順番エラーが発生したメソッドからの戻り値。</span><span class="sxs-lookup"><span data-stu-id="166bb-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="166bb-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="166bb-109">_ulFlags_</span></span>
  
> <span data-ttu-id="166bb-110">順番使用しない場合は 0 (ゼロ) に設定します。</span><span class="sxs-lookup"><span data-stu-id="166bb-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="166bb-111">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="166bb-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="166bb-112">読み上げtable オブジェクトで発生した最後のエラーについての情報が含まれている MAPI の[MAPIERROR](mapierror.md)構造体を指します。</span><span class="sxs-lookup"><span data-stu-id="166bb-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="166bb-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="166bb-113">See also</span></span>



[<span data-ttu-id="166bb-114">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="166bb-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="166bb-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="166bb-115">MAPIERROR</span></span>](mapierror.md)


<span data-ttu-id="166bb-116">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="166bb-116">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

