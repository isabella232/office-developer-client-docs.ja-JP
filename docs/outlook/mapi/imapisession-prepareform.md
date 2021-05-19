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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335766"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="cc652-103">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="cc652-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="cc652-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc652-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc652-105">[IMAPISession::ShowForm](imapisession-showform.md)メソッドがメッセージにアクセスするために使用する数値トークンを作成します。</span><span class="sxs-lookup"><span data-stu-id="cc652-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="cc652-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc652-106">Parameters</span></span>

 <span data-ttu-id="cc652-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="cc652-107">_lpInterface_</span></span>
  
> <span data-ttu-id="cc652-108">[in]メッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cc652-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="cc652-109">**null を渡** す場合、標準インターフェイス [(IMessage)](imessageimapiprop.md)が使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc652-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="cc652-110">_lpInterface パラメーターは_ null または **IID_IMessage。**</span><span class="sxs-lookup"><span data-stu-id="cc652-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="cc652-111">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="cc652-111">_lpMessage_</span></span>
  
> <span data-ttu-id="cc652-112">[in]フォームに表示するメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cc652-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="cc652-113">_lpulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="cc652-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="cc652-114">[out]メッセージ トークンへのポインター。 **これは、IMAPISession::ShowForm** メソッドが  _lpMessage_ で指すメッセージにアクセスするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc652-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cc652-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc652-115">Return value</span></span>

<span data-ttu-id="cc652-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc652-116">S_OK</span></span> 
  
> <span data-ttu-id="cc652-117">フォームの準備が成功しました。</span><span class="sxs-lookup"><span data-stu-id="cc652-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cc652-118">注釈</span><span class="sxs-lookup"><span data-stu-id="cc652-118">Remarks</span></span>

<span data-ttu-id="cc652-119">**IMAPISession::P repareForm** メソッドは _、lpMessage_ パラメーターが指すメッセージのメッセージ トークンを作成し、メッセージの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cc652-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="cc652-120">このトークンは  _ulMessageToken_ パラメーターで **IMAPISession::ShowForm に渡されます**。</span><span class="sxs-lookup"><span data-stu-id="cc652-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cc652-121">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="cc652-121">Notes to callers</span></span>

<span data-ttu-id="cc652-122">**PrepareForm** の呼び出しが成功した場合は **、ShowForm** を呼び出す前に [、その IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出して _lpMessage_ が指すメッセージを解放します。</span><span class="sxs-lookup"><span data-stu-id="cc652-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="cc652-123">ShowForm を呼び出す前にメッセージを解放 **すると、** メモリ リークが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cc652-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cc652-124">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="cc652-124">MFCMAPI reference</span></span>

<span data-ttu-id="cc652-125">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cc652-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cc652-126">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="cc652-126">**File**</span></span>|<span data-ttu-id="cc652-127">**関数**</span><span class="sxs-lookup"><span data-stu-id="cc652-127">**Function**</span></span>|<span data-ttu-id="cc652-128">**コメント**</span><span class="sxs-lookup"><span data-stu-id="cc652-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cc652-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="cc652-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="cc652-130">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="cc652-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="cc652-131">MFCMAPI は **IMAPISession::P repareForm** メソッドを **IMAPISession::ShowForm** と共に使用して、モーダル フォームでメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="cc652-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cc652-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="cc652-132">See also</span></span>



[<span data-ttu-id="cc652-133">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="cc652-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="cc652-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cc652-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="cc652-135">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="cc652-135">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

