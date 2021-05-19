---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 80010ca19999ba519f051e914f02f240abb524e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424932"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="f8051-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="f8051-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="f8051-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8051-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8051-105">[送受信] ダイアログに表示される詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="f8051-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="f8051-106">同期中にエラーが発生した場合、ストア プロバイダーは、この関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f8051-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="f8051-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8051-107">Parameters</span></span>

 <span data-ttu-id="f8051-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="f8051-108">**hResult**</span></span>
  
> <span data-ttu-id="f8051-109">エラーまたは警告の HRESULT。</span><span class="sxs-lookup"><span data-stu-id="f8051-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="f8051-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="f8051-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="f8051-111">表示するエラーに関連付けられた文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f8051-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f8051-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8051-112">Return value</span></span>

<span data-ttu-id="f8051-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8051-113">S_OK</span></span> 
  
> <span data-ttu-id="f8051-114">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="f8051-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8051-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8051-115">See also</span></span>



[<span data-ttu-id="f8051-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8051-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

