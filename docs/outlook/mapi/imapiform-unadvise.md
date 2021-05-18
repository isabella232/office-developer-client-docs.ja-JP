---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 770ceb7af98f5271baad65043e013feb353d231a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329471"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="9b6a1-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="9b6a1-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="9b6a1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b6a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b6a1-105">[IMAPIForm::Advise](imapiform-advise.md)を呼び出して以前に確立されたフォーム ビューアーを使用して通知の登録をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="9b6a1-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="9b6a1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9b6a1-106">Parameters</span></span>

 <span data-ttu-id="9b6a1-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="9b6a1-107">_ulConnection_</span></span>
  
> <span data-ttu-id="9b6a1-108">[in]取り消す通知登録を識別する接続番号。</span><span class="sxs-lookup"><span data-stu-id="9b6a1-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b6a1-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="9b6a1-109">Return value</span></span>

<span data-ttu-id="9b6a1-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b6a1-110">S_OK</span></span> 
  
> <span data-ttu-id="9b6a1-111">登録が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="9b6a1-111">The registration was canceled.</span></span>
    
<span data-ttu-id="9b6a1-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9b6a1-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="9b6a1-113">_ulConnection_ パラメーターで渡される接続番号は、有効な登録を表すではありません。</span><span class="sxs-lookup"><span data-stu-id="9b6a1-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9b6a1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9b6a1-114">Remarks</span></span>

<span data-ttu-id="9b6a1-115">フォーム ビューアーは **IMAPIForm::Unadvise** メソッドを呼び出して **、IMAPIForm::Advise** メソッドを呼び出して最初に確立した通知の登録をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="9b6a1-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9b6a1-116">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="9b6a1-116">Notes to implementers</span></span>

<span data-ttu-id="9b6a1-117">フォーム ビューアーのビューに保持しているポインターを破棄するには、 [その IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9b6a1-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="9b6a1-118">通常、 **リリースは** **Unadvise 呼び出し中に呼び出** されます。</span><span class="sxs-lookup"><span data-stu-id="9b6a1-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="9b6a1-119">ただし、別のスレッドがビューの IMAPIViewAdviseSink メソッドのいずれかを呼び出す過程にある場合は **、IMAPIViewAdviseSink** メソッドが返されるまで Release 呼び出しを遅延します。 [](imapiviewadvisesinkiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="9b6a1-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b6a1-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b6a1-120">See also</span></span>



[<span data-ttu-id="9b6a1-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="9b6a1-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="9b6a1-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b6a1-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="9b6a1-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b6a1-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

