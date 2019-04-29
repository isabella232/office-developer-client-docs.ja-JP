---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5b10f744e3033aab63820e4cd5e414f4c01c27cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410617"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="7e68e-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="7e68e-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="7e68e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e68e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e68e-105">表示順序に従って、次または前のメッセージをアクティブにします。</span><span class="sxs-lookup"><span data-stu-id="7e68e-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="7e68e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7e68e-106">Parameters</span></span>

<span data-ttu-id="7e68e-107">_uldir_</span><span class="sxs-lookup"><span data-stu-id="7e68e-107">_ulDir_</span></span>
  
> <span data-ttu-id="7e68e-108">順番アクティブ化するメッセージに関する情報を提供するステータスフラグ。</span><span class="sxs-lookup"><span data-stu-id="7e68e-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="7e68e-109">有効なフラグの設定は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7e68e-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="7e68e-110">VCDIR_CATEGORY: ビューアーでは、ビューの別のカテゴリにあるメッセージをアクティブ化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e68e-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="7e68e-111">アクティブにするメッセージは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7e68e-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="7e68e-112">このフラグが VCDIR_NEXT の場合は、次のビューカテゴリ\*\*\*\* の最初のメッセージ。</span><span class="sxs-lookup"><span data-stu-id="7e68e-112">The first message in the next view category if this flag is **OR**ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="7e68e-113">このフラグが VCDIR_PREV で、前のカテゴリが展開さ\*\*\*\* れている場合、前のビューカテゴリの最後のメッセージ。</span><span class="sxs-lookup"><span data-stu-id="7e68e-113">The last message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="7e68e-114">このフラグが VCDIR_PREV で、前のカテゴリが展開さ\*\*\*\* れていない場合、前のビューカテゴリの最初のメッセージ。</span><span class="sxs-lookup"><span data-stu-id="7e68e-114">The first message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="7e68e-115">この場合、前のカテゴリは自動拡張を行います。</span><span class="sxs-lookup"><span data-stu-id="7e68e-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="7e68e-116">VCDIR_DELETE: 現在のメッセージが削除されているため、閲覧者は次または前のメッセージをアクティブにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e68e-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="7e68e-117">VCDIR_MOVE: 現在のメッセージが移動されたため、閲覧者は次または前のメッセージをアクティブにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e68e-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="7e68e-118">VCDIR_NEXT: 閲覧者は、表示順序で次のメッセージをアクティブ化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e68e-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="7e68e-119">VCDIR_PREV: 閲覧者は、表示順序で前のメッセージをアクティブ化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e68e-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="7e68e-120">VCDIR_UNREAD: 閲覧者は、表示順序で、次または前の未読メッセージをアクティブにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e68e-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="7e68e-121">_prcposrect_</span><span class="sxs-lookup"><span data-stu-id="7e68e-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="7e68e-122">順番アクティブ化されたメッセージの表示に使用されるウィンドウのサイズと位置を含む Windows **RECT**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7e68e-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7e68e-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="7e68e-123">Return value</span></span>

<span data-ttu-id="7e68e-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e68e-124">S_OK</span></span> 
  
> <span data-ttu-id="7e68e-125">メッセージが正常にアクティブ化されました。</span><span class="sxs-lookup"><span data-stu-id="7e68e-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="7e68e-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="7e68e-126">S_FALSE</span></span> 
  
> <span data-ttu-id="7e68e-127">メッセージは正常にアクティブ化されましたが、プロセスで別の種類のフォームが開かれました。</span><span class="sxs-lookup"><span data-stu-id="7e68e-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7e68e-128">注釈</span><span class="sxs-lookup"><span data-stu-id="7e68e-128">Remarks</span></span>

<span data-ttu-id="7e68e-129">Form オブジェクトは、 **imapiviewcontext:: ActivateNext**メソッドを呼び出して、ユーザーに表示されるメッセージを変更します。</span><span class="sxs-lookup"><span data-stu-id="7e68e-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="7e68e-130">_uldir_パラメーターで渡される値は、アクティブ化する必要があるメッセージと、場合によっては理由を示します。</span><span class="sxs-lookup"><span data-stu-id="7e68e-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="7e68e-131">VCDIR_NEXT および VCDIR_PREVIOUS の各フラグは、ビュー内で**次**または**前**のコマンドを選択したユーザーにそれぞれ対応します。</span><span class="sxs-lookup"><span data-stu-id="7e68e-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="7e68e-132">通常、これらの操作は、フォームビューアーのメッセージの一覧で1つ上または下のメッセージを移動することに対応します。</span><span class="sxs-lookup"><span data-stu-id="7e68e-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="7e68e-133">VCDIR_DELETE および VCDIR_MOVE フラグは、それぞれ[IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md)メソッドと[IMAPIMessageSite:: MoveMessage](imapimessagesite-movemessage.md)メソッドによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="7e68e-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="7e68e-134">これらのメソッドの実装は、適切な方向で**ActivateNext**を呼び出し、 **ActivateNext**呼び出しが失敗しなかった場合にメッセージに対して要求された操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="7e68e-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="7e68e-135">通常、フォームビューアーを使用すると、ユーザーはメッセージリスト内で移動する方向を指定できます。</span><span class="sxs-lookup"><span data-stu-id="7e68e-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7e68e-136">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="7e68e-136">Notes to implementers</span></span>

<span data-ttu-id="7e68e-137">[imapiviewcontext:: ActivateNext](imapiviewcontext-activatenext.md)の実装により、 _uldir_の値に応じて、フォルダー内の次のメッセージまたは前のメッセージが作成されます (現在のメッセージ)。</span><span class="sxs-lookup"><span data-stu-id="7e68e-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="7e68e-138">**ActivateNext**が戻ると、 [IMAPIMessageSite:: GetMessage](imapimessagesite-getmessage.md)を呼び出して、新しくアクティブ化されたメッセージへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="7e68e-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7e68e-139">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7e68e-139">Notes to callers</span></span>

<span data-ttu-id="7e68e-140">**ActivateNext**が S_FALSE を返す場合、または現在のメッセージが存在しない場合は、通常のシャットダウン手順を実行します。これには、フォームの[imapiform:: shutdownform](imapiform-shutdownform.md)メソッドの呼び出しが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e68e-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="7e68e-141">次または前のメッセージが表示された場合は、 _prcposrect_パラメーターで渡されたウィンドウ四角形を使用して表示します。</span><span class="sxs-lookup"><span data-stu-id="7e68e-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7e68e-142">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="7e68e-142">MFCMAPI reference</span></span>

<span data-ttu-id="7e68e-143">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e68e-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7e68e-144">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="7e68e-144">**File**</span></span>|<span data-ttu-id="7e68e-145">**関数**</span><span class="sxs-lookup"><span data-stu-id="7e68e-145">**Function**</span></span>|<span data-ttu-id="7e68e-146">**コメント**</span><span class="sxs-lookup"><span data-stu-id="7e68e-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7e68e-147">MyMAPIFormViewer</span><span class="sxs-lookup"><span data-stu-id="7e68e-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="7e68e-148">cmymapiformviewer:: ActivateNext</span><span class="sxs-lookup"><span data-stu-id="7e68e-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="7e68e-149">mfcmapi は、この関数に**imapiviewcontext:: ActivateNext**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="7e68e-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7e68e-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="7e68e-150">See also</span></span>

- [<span data-ttu-id="7e68e-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="7e68e-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="7e68e-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e68e-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- <span data-ttu-id="7e68e-153">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="7e68e-153">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

