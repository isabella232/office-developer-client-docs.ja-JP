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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 826863e30ae39d3c8d523bd2dff84731bcf16971
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800528"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="1b4c7-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="1b4c7-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="1b4c7-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b4c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b4c7-105">[IMAPIForm::Advise](imapiform-advise.md)を呼び出すことによって確立されていたフォーム ビューアーを使用して通知の登録をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="1b4c7-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="1b4c7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1b4c7-106">Parameters</span></span>

 <span data-ttu-id="1b4c7-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="1b4c7-107">_ulConnection_</span></span>
  
> <span data-ttu-id="1b4c7-108">[in]キャンセルする通知の登録を識別する接続の数です。</span><span class="sxs-lookup"><span data-stu-id="1b4c7-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b4c7-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1b4c7-109">Return value</span></span>

<span data-ttu-id="1b4c7-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b4c7-110">S_OK</span></span> 
  
> <span data-ttu-id="1b4c7-111">登録が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="1b4c7-111">The registration was canceled.</span></span>
    
<span data-ttu-id="1b4c7-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1b4c7-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="1b4c7-113">_UlConnection_パラメーターに渡される接続数は、有効な登録を表していません。</span><span class="sxs-lookup"><span data-stu-id="1b4c7-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1b4c7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1b4c7-114">Remarks</span></span>

<span data-ttu-id="1b4c7-115">フォームの閲覧者は、 **IMAPIForm::Advise**メソッドを呼び出すことによって最初に確立したことを示す通知の登録をキャンセルする**IMAPIForm::Unadvise**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1b4c7-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1b4c7-116">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="1b4c7-116">Notes to implementers</span></span>

<span data-ttu-id="1b4c7-117">破棄するがフォーム ビューアーのビューを保持しているポインターは、その[が](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出して、シンクを案内します。</span><span class="sxs-lookup"><span data-stu-id="1b4c7-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="1b4c7-118">一般に、**リリース**と呼ばれる**Unadvise**の呼び出し中にします。</span><span class="sxs-lookup"><span data-stu-id="1b4c7-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="1b4c7-119">ただし、 [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md)メソッドのいずれかのプロセスでは、別のスレッド ビューのシンクをアドバイス、 **IMAPIViewAdviseSink**メソッドが戻るまでに**リリース**の呼び出しを遅延します。</span><span class="sxs-lookup"><span data-stu-id="1b4c7-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1b4c7-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b4c7-120">See also</span></span>



[<span data-ttu-id="1b4c7-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="1b4c7-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="1b4c7-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b4c7-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="1b4c7-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b4c7-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

