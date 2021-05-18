---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321414"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="f8502-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="f8502-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="f8502-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8502-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8502-105">現在のメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="f8502-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="f8502-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8502-106">Parameters</span></span>

 <span data-ttu-id="f8502-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="f8502-107">_pViewContext_</span></span>
  
> <span data-ttu-id="f8502-108">[in]ビュー コンテキスト オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f8502-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="f8502-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="f8502-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="f8502-110">[in]現在のフォームのウィンドウ サイズと位置を含む [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f8502-110">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="f8502-111">次に表示されるフォームでは、このウィンドウの四角形も使用されます。</span><span class="sxs-lookup"><span data-stu-id="f8502-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f8502-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8502-112">Return value</span></span>

<span data-ttu-id="f8502-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8502-113">S_OK</span></span> 
  
> <span data-ttu-id="f8502-114">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="f8502-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f8502-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f8502-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f8502-116">この操作は、このメッセージ サイトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f8502-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8502-117">注釈</span><span class="sxs-lookup"><span data-stu-id="f8502-117">Remarks</span></span>

<span data-ttu-id="f8502-118">フォーム オブジェクトは **IMAPIMessageSite::D eleteMessage** メソッドを呼び出して、フォームが現在表示しているメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="f8502-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f8502-119">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f8502-119">Notes to callers</span></span>

<span data-ttu-id="f8502-120">DeleteMessage の戻り **値に** 続いて、フォーム オブジェクトは新しいメッセージを確認し、存在しない場合は自分自身を閉じなければならない。</span><span class="sxs-lookup"><span data-stu-id="f8502-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="f8502-121">**DeleteMessage** が処理されたメッセージが削除済みまたは削除済みアイテム フォルダーに移動されたかどうかを判断するために、フォーム オブジェクトは [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)メソッドを呼び出して、DELETE_IS_MOVE フラグが返されたかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="f8502-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f8502-122">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="f8502-122">Notes to implementers</span></span>

<span data-ttu-id="f8502-123">メッセージを削除した後、フォーム ビューアーの **DeleteMessage** メソッドの実装が次のメッセージに移動する場合、実装は [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) メソッドを呼び出し、実際の削除を実行する前に VCDIR_DELETE フラグを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8502-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="f8502-124">フォーム ビューアーの **DeleteMessage** の実装が削除済みメッセージ (削除済みアイテムフォルダーなど) を移動する場合、メッセージが変更された場合、そのメッセージに対する変更を保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8502-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="f8502-125">DeleteMessage の一般的な **実装では、** 次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="f8502-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="f8502-126">実装がメッセージを移動している場合は [、iPersistMessage::Save](ipersistmessage-save.md)メソッドを呼び出し、pMessage パラメーターに null を渡し _、fSameAsLoad_ パラメーターに true を渡します。 </span><span class="sxs-lookup"><span data-stu-id="f8502-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="f8502-127">このメソッドは **IMAPIViewContext::ActivateNext** メソッドを呼び出し  _、ulDir_ パラメーターに VCDIR_DELETEフラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="f8502-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="f8502-128">**ActivateNext 呼び出し** が失敗すると、その呼び出しが返されます。</span><span class="sxs-lookup"><span data-stu-id="f8502-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="f8502-129">**ActivateNext が** メソッドを返S_FALSE、IPersistMessage::HandsOffMessage メソッド [を呼び出](ipersistmessage-handsoffmessage.md)します。</span><span class="sxs-lookup"><span data-stu-id="f8502-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="f8502-130">メッセージを削除または移動します。</span><span class="sxs-lookup"><span data-stu-id="f8502-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="f8502-131">フォームのウィンドウ **で使用される RECT** 構造を取得するには [、GetWindowRect](https://msdn.microsoft.com/library/ms633519)関数Windows呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f8502-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="f8502-132">フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="f8502-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f8502-133">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="f8502-133">MFCMAPI reference</span></span>

<span data-ttu-id="f8502-134">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8502-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f8502-135">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="f8502-135">**File**</span></span>|<span data-ttu-id="f8502-136">**関数**</span><span class="sxs-lookup"><span data-stu-id="f8502-136">**Function**</span></span>|<span data-ttu-id="f8502-137">**コメント**</span><span class="sxs-lookup"><span data-stu-id="f8502-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8502-138">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="f8502-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="f8502-139">CMyMAPIFormViewer::D eleteMessage</span><span class="sxs-lookup"><span data-stu-id="f8502-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="f8502-140">実装されていません。</span><span class="sxs-lookup"><span data-stu-id="f8502-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8502-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="f8502-141">See also</span></span>



[<span data-ttu-id="f8502-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="f8502-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="f8502-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="f8502-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="f8502-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="f8502-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="f8502-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="f8502-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="f8502-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8502-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="f8502-147">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="f8502-147">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="f8502-148">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f8502-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

