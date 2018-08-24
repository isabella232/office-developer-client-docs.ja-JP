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
ms.openlocfilehash: 8cff424e3b589af292e56cef1ca19198e9c80d1f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594986"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="edcec-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="edcec-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="edcec-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edcec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edcec-105">[送受信] ダイアログ ボックスに表示される詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="edcec-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="edcec-106">同期中にエラーが発生する場合、ストア プロバイダーは、この関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="edcec-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="edcec-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edcec-107">Parameters</span></span>

 <span data-ttu-id="edcec-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="edcec-108">**hResult**</span></span>
  
> <span data-ttu-id="edcec-109">警告またはエラーの HRESULT。</span><span class="sxs-lookup"><span data-stu-id="edcec-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="edcec-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="edcec-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="edcec-111">表示されるエラーに関連付けられている文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="edcec-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="edcec-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="edcec-112">Return value</span></span>

<span data-ttu-id="edcec-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="edcec-113">S_OK</span></span> 
  
> <span data-ttu-id="edcec-114">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="edcec-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edcec-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="edcec-115">See also</span></span>



[<span data-ttu-id="edcec-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="edcec-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

