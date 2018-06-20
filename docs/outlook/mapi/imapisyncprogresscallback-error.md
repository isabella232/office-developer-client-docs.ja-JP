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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9dc368e6502bbb14cf42f6bc5a08fd2893f98bf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800803"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="8316a-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="8316a-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="8316a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8316a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8316a-105">[送受信] ダイアログ ボックスに表示される詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="8316a-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="8316a-106">同期中にエラーが発生する場合、ストア プロバイダーは、この関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8316a-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="8316a-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8316a-107">Parameters</span></span>

 <span data-ttu-id="8316a-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="8316a-108">**hResult**</span></span>
  
> <span data-ttu-id="8316a-109">警告またはエラーの HRESULT。</span><span class="sxs-lookup"><span data-stu-id="8316a-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="8316a-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="8316a-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="8316a-111">表示されるエラーに関連付けられている文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8316a-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8316a-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="8316a-112">Return value</span></span>

<span data-ttu-id="8316a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8316a-113">S_OK</span></span> 
  
> <span data-ttu-id="8316a-114">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="8316a-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8316a-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="8316a-115">See also</span></span>



[<span data-ttu-id="8316a-116">IMAPISyncProgressCallback: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8316a-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

