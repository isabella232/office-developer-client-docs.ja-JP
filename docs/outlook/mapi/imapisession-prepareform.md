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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393237"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="4249b-103">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="4249b-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="4249b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4249b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4249b-105">メッセージにアクセスする[IMAPISession::ShowForm](imapisession-showform.md)メソッドを使用する数値のトークンを作成します。</span><span class="sxs-lookup"><span data-stu-id="4249b-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="4249b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4249b-106">Parameters</span></span>

 <span data-ttu-id="4249b-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4249b-107">_lpInterface_</span></span>
  
> <span data-ttu-id="4249b-108">[in]メッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4249b-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="4249b-109">使用されている標準的なインタ フェース、または[IMessage](imessageimapiprop.md)、 **null**の結果を渡しています。</span><span class="sxs-lookup"><span data-stu-id="4249b-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="4249b-110">_LpInterface_パラメーターは、 **null**または IID_IMessage である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4249b-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="4249b-111">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="4249b-111">_lpMessage_</span></span>
  
> <span data-ttu-id="4249b-112">[in]フォームに表示されるメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4249b-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="4249b-113">_lpulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="4249b-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="4249b-114">[out]_LpMessage_が指すメッセージにアクセスするのには、 **IMAPISession::ShowForm**メソッドで使用されるメッセージのトークンへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="4249b-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4249b-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="4249b-115">Return value</span></span>

<span data-ttu-id="4249b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4249b-116">S_OK</span></span> 
  
> <span data-ttu-id="4249b-117">フォームの準備が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="4249b-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4249b-118">備考</span><span class="sxs-lookup"><span data-stu-id="4249b-118">Remarks</span></span>

<span data-ttu-id="4249b-119">**IMAPISession::PrepareForm**メソッドでは、 _lpMessage_パラメーターで指定されたメッセージのメッセージのトークンを作成し、メッセージの[IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4249b-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="4249b-120">このトークンは、 **IMAPISession::ShowForm**に、 _ulMessageToken_パラメーターに渡されます。</span><span class="sxs-lookup"><span data-stu-id="4249b-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4249b-121">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4249b-121">Notes to callers</span></span>

<span data-ttu-id="4249b-122">**PrepareForm**への呼び出しが成功した場合が指す_lpMessage_ **ShowForm**を呼び出す前に、[リ ス](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)のメソッドを呼び出すことによってメッセージを離します。</span><span class="sxs-lookup"><span data-stu-id="4249b-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="4249b-123">**ShowForm**を呼び出す前に、メッセージを解放に失敗には、メモリ リークが発生します。</span><span class="sxs-lookup"><span data-stu-id="4249b-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4249b-124">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="4249b-124">MFCMAPI reference</span></span>

<span data-ttu-id="4249b-125">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4249b-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4249b-126">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="4249b-126">**File**</span></span>|<span data-ttu-id="4249b-127">**関数**</span><span class="sxs-lookup"><span data-stu-id="4249b-127">**Function**</span></span>|<span data-ttu-id="4249b-128">**コメント**</span><span class="sxs-lookup"><span data-stu-id="4249b-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4249b-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="4249b-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="4249b-130">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="4249b-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="4249b-131">MFCMAPI では、モーダル形式でメッセージを表示するのには、 **IMAPISession::ShowForm**、 **IMAPISession::PrepareForm**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="4249b-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4249b-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="4249b-132">See also</span></span>



[<span data-ttu-id="4249b-133">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="4249b-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="4249b-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4249b-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="4249b-135">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="4249b-135">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

