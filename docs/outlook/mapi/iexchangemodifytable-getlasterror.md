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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f0d2ad118346dd06788af972b64b10d6f6f6d0fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594293"
---
# <a name="iexchangemodifytablegetlasterror"></a><span data-ttu-id="c1d0e-103">IExchangeModifyTable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c1d0e-103">IExchangeModifyTable::GetLastError</span></span>

  
  
<span data-ttu-id="c1d0e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1d0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1d0e-105">Table オブジェクトには、最後に発生したエラーに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="c1d0e-105">Returns information about the last error that occurred in a table object.</span></span>
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a><span data-ttu-id="c1d0e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c1d0e-106">Parameters</span></span>

 <span data-ttu-id="c1d0e-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="c1d0e-107">_hResult_</span></span>
  
> <span data-ttu-id="c1d0e-108">[in]失敗したメソッドからの戻り値です。</span><span class="sxs-lookup"><span data-stu-id="c1d0e-108">[in] The return value from the method that failed.</span></span>
    
 <span data-ttu-id="c1d0e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c1d0e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c1d0e-110">[in]使用しないとは、0 (ゼロ) に設定します。</span><span class="sxs-lookup"><span data-stu-id="c1d0e-110">[in] Not used, set to 0 (zero).</span></span>
    
 <span data-ttu-id="c1d0e-111">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="c1d0e-111">_lppMAPIError_</span></span>
  
> <span data-ttu-id="c1d0e-112">[out]Table オブジェクトに対して発生した最後のエラーに関する情報を格納する MAPI [MAPIERROR](mapierror.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c1d0e-112">[out] Points to a MAPI [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for a table object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c1d0e-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1d0e-113">See also</span></span>



[<span data-ttu-id="c1d0e-114">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1d0e-114">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="c1d0e-115">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="c1d0e-115">MAPIERROR</span></span>](mapierror.md)


<span data-ttu-id="c1d0e-116">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c1d0e-116">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

