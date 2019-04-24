---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351192"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="147d1-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="147d1-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="147d1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="147d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="147d1-105">フォームの登録を管理して、閲覧者の変更に関する通知を受信します。</span><span class="sxs-lookup"><span data-stu-id="147d1-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="147d1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="147d1-106">Parameters</span></span>

 <span data-ttu-id="147d1-107">_pmvns_</span><span class="sxs-lookup"><span data-stu-id="147d1-107">_pmvns_</span></span>
  
> <span data-ttu-id="147d1-108">順番フォームアドバイズシンクオブジェクトまたは NULL へのポインター。</span><span class="sxs-lookup"><span data-stu-id="147d1-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="147d1-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="147d1-109">Return value</span></span>

<span data-ttu-id="147d1-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="147d1-110">S_OK</span></span> 
  
> <span data-ttu-id="147d1-111">フォーム通知の登録または取り消しに成功しました。</span><span class="sxs-lookup"><span data-stu-id="147d1-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="147d1-112">解説</span><span class="sxs-lookup"><span data-stu-id="147d1-112">Remarks</span></span>

<span data-ttu-id="147d1-113">form オブジェクトは**imapiviewcontext:: SetAdviseSink**メソッドを呼び出して、フォームビューアーの変更について学習するか、前に登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="147d1-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="147d1-114">_pmvns_が NULL に設定されている場合、フォームは登録をキャンセルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="147d1-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="147d1-115">_pmvns_が有効な form アドバイズシンクを指している場合、フォームは将来の通知の登録を希望します。</span><span class="sxs-lookup"><span data-stu-id="147d1-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="147d1-116">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="147d1-116">Notes to implementers</span></span>

<span data-ttu-id="147d1-117">**SetAdviseSink**にフォームアドバイズシンクポインターが含まれている場合は、別の**SetAdviseSink**呼び出しが行われてから、通知が取り消されるまで、そのポインターへの参照を保持します。</span><span class="sxs-lookup"><span data-stu-id="147d1-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="147d1-118">viewer で変更が発生したとき、および新しいメッセージを読み込むときに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="147d1-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="147d1-119">詳細については、「[フォーム通知の送信と受信](sending-and-receiving-form-notifications.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="147d1-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="147d1-120">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="147d1-120">MFCMAPI reference</span></span>

<span data-ttu-id="147d1-121">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="147d1-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="147d1-122">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="147d1-122">**File**</span></span>|<span data-ttu-id="147d1-123">**関数**</span><span class="sxs-lookup"><span data-stu-id="147d1-123">**Function**</span></span>|<span data-ttu-id="147d1-124">**コメント**</span><span class="sxs-lookup"><span data-stu-id="147d1-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="147d1-125">MyMAPIFormViewer</span><span class="sxs-lookup"><span data-stu-id="147d1-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="147d1-126">cmymapiformviewer:: SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="147d1-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="147d1-127">mfcmapi は、この関数に**imapiviewcontext:: SetAdviseSink**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="147d1-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="147d1-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="147d1-128">See also</span></span>



<span data-ttu-id="147d1-129">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="147d1-129">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

