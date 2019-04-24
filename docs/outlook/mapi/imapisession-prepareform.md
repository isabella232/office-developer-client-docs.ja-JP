---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335766"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="ba8fc-103">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="ba8fc-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="ba8fc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba8fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba8fc-105">[imapisession:: showform](imapisession-showform.md)メソッドがメッセージにアクセスするために使用する数値トークンを作成します。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="ba8fc-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ba8fc-106">Parameters</span></span>

 <span data-ttu-id="ba8fc-107">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="ba8fc-107">_lpInterface_</span></span>
  
> <span data-ttu-id="ba8fc-108">順番メッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="ba8fc-109">標準インターフェイスまたは[IMessage](imessageimapiprop.md)で**null**結果が渡されています。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="ba8fc-110">_lpinterface_パラメーターは、 **null**または IID_IMessage である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="ba8fc-111">_lpmessage_</span><span class="sxs-lookup"><span data-stu-id="ba8fc-111">_lpMessage_</span></span>
  
> <span data-ttu-id="ba8fc-112">順番フォームに表示されるメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="ba8fc-113">_lアウト messagetoken_</span><span class="sxs-lookup"><span data-stu-id="ba8fc-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="ba8fc-114">読み上げ_lpmessage_によって参照されるメッセージにアクセスするために**imapisession:: showform**メソッドによって使用されるメッセージトークンへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ba8fc-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="ba8fc-115">Return value</span></span>

<span data-ttu-id="ba8fc-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ba8fc-116">S_OK</span></span> 
  
> <span data-ttu-id="ba8fc-117">フォームの準備が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba8fc-118">解説</span><span class="sxs-lookup"><span data-stu-id="ba8fc-118">Remarks</span></span>

<span data-ttu-id="ba8fc-119">**imapisession::P repareform**メソッドは、 _lpmessage_パラメーターによって示されるメッセージのメッセージトークンを作成し、メッセージの[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="ba8fc-120">このトークンは、 _ulmessagetoken_パラメーターで**imapisession:: showform**に渡されます。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ba8fc-121">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ba8fc-121">Notes to callers</span></span>

<span data-ttu-id="ba8fc-122">**PrepareForm**の呼び出しが成功した場合は、 **showform**を呼び出す前に[IUnknown:: release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出して、 _lpmessage_に示されているメッセージを解放します。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="ba8fc-123">**showform**を呼び出す前にメッセージを解放しないと、メモリリークが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ba8fc-124">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="ba8fc-124">MFCMAPI reference</span></span>

<span data-ttu-id="ba8fc-125">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ba8fc-126">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="ba8fc-126">**File**</span></span>|<span data-ttu-id="ba8fc-127">**関数**</span><span class="sxs-lookup"><span data-stu-id="ba8fc-127">**Function**</span></span>|<span data-ttu-id="ba8fc-128">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ba8fc-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba8fc-129">MAPIFormFunctions</span><span class="sxs-lookup"><span data-stu-id="ba8fc-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ba8fc-130">openmessagemodal</span><span class="sxs-lookup"><span data-stu-id="ba8fc-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="ba8fc-131">mfcmapi は、imapisession: **:P repareform**メソッドを**imapisession:: showform**と共に使用して、モーダルフォームにメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba8fc-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="ba8fc-132">See also</span></span>



[<span data-ttu-id="ba8fc-133">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="ba8fc-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="ba8fc-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba8fc-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="ba8fc-135">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ba8fc-135">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

