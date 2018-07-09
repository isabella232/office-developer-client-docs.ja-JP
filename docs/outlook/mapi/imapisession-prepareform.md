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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 026a120406b714a50a9191e4761021693a250b94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800696"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="bf6cb-103">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="bf6cb-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="bf6cb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf6cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf6cb-105">メッセージにアクセスする[IMAPISession::ShowForm](imapisession-showform.md)メソッドを使用する数値のトークンを作成します。</span><span class="sxs-lookup"><span data-stu-id="bf6cb-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="bf6cb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="bf6cb-106">Parameters</span></span>

 <span data-ttu-id="bf6cb-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="bf6cb-107">_lpInterface_</span></span>
  
> <span data-ttu-id="bf6cb-108">[in]メッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bf6cb-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="bf6cb-109">使用されている標準的なインタ フェース、または[IMessage](imessageimapiprop.md)、 **null**の結果を渡しています。</span><span class="sxs-lookup"><span data-stu-id="bf6cb-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="bf6cb-110">_LpInterface_パラメーターは、 **null**または IID_IMessage である必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf6cb-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="bf6cb-111">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="bf6cb-111">_lpMessage_</span></span>
  
> <span data-ttu-id="bf6cb-112">[in]フォームに表示されるメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bf6cb-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="bf6cb-113">_lpulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="bf6cb-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="bf6cb-114">[out]_LpMessage_が指すメッセージにアクセスするのには、 **IMAPISession::ShowForm**メソッドで使用されるメッセージのトークンへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="bf6cb-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bf6cb-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="bf6cb-115">Return value</span></span>

<span data-ttu-id="bf6cb-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf6cb-116">S_OK</span></span> 
  
> <span data-ttu-id="bf6cb-117">フォームの準備が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="bf6cb-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf6cb-118">備考</span><span class="sxs-lookup"><span data-stu-id="bf6cb-118">Remarks</span></span>

<span data-ttu-id="bf6cb-119">**IMAPISession::PrepareForm**メソッドでは、 _lpMessage_パラメーターで指定されたメッセージのメッセージのトークンを作成し、メッセージの[IUnknown::AddRef](http://msdn.microsoft.com/ja-jp/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bf6cb-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](http://msdn.microsoft.com/ja-jp/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="bf6cb-120">このトークンは、 **IMAPISession::ShowForm**に、 _ulMessageToken_パラメーターに渡されます。</span><span class="sxs-lookup"><span data-stu-id="bf6cb-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bf6cb-121">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="bf6cb-121">Notes to callers</span></span>

<span data-ttu-id="bf6cb-122">**PrepareForm**への呼び出しが成功した場合が指す_lpMessage_ **ShowForm**を呼び出す前に、[リ ス](http://msdn.microsoft.com/ja-jp/library/ms682317%28v=VS.85%29.aspx)のメソッドを呼び出すことによってメッセージを離します。</span><span class="sxs-lookup"><span data-stu-id="bf6cb-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](http://msdn.microsoft.com/ja-jp/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="bf6cb-123">**ShowForm**を呼び出す前に、メッセージを解放に失敗には、メモリ リークが発生します。</span><span class="sxs-lookup"><span data-stu-id="bf6cb-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bf6cb-124">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="bf6cb-124">MFCMAPI reference</span></span>

<span data-ttu-id="bf6cb-125">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="bf6cb-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bf6cb-126">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="bf6cb-126">**File**</span></span>|<span data-ttu-id="bf6cb-127">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="bf6cb-127">**Function**</span></span>|<span data-ttu-id="bf6cb-128">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="bf6cb-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf6cb-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="bf6cb-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="bf6cb-130">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="bf6cb-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="bf6cb-131">MFCMAPI では、モーダル形式でメッセージを表示するのには、 **IMAPISession::ShowForm**、 **IMAPISession::PrepareForm**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="bf6cb-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf6cb-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf6cb-132">See also</span></span>



[<span data-ttu-id="bf6cb-133">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="bf6cb-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="bf6cb-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bf6cb-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="bf6cb-135">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="bf6cb-135">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

