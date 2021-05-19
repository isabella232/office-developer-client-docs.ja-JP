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
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="77fc9-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="77fc9-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="77fc9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77fc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77fc9-105">ビューの順序で次または前のメッセージをアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="77fc9-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="77fc9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="77fc9-106">Parameters</span></span>

<span data-ttu-id="77fc9-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="77fc9-107">_ulDir_</span></span>
  
> <span data-ttu-id="77fc9-108">[in]アクティブ化するメッセージに関する情報を示す状態フラグ。</span><span class="sxs-lookup"><span data-stu-id="77fc9-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="77fc9-109">有効なフラグ設定は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="77fc9-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="77fc9-110">VCDIR_CATEGORY: ビューアーは、ビューの別のカテゴリでメッセージをアクティブ化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77fc9-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="77fc9-111">アクティブ化するメッセージは次の場合です。</span><span class="sxs-lookup"><span data-stu-id="77fc9-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="77fc9-112">このフラグが OR の場合は、次のビュー カテゴリの最初のVCDIR_NEXT。</span><span class="sxs-lookup"><span data-stu-id="77fc9-112">The first message in the next view category if this flag is **OR** ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="77fc9-113">前のビュー カテゴリの最後のメッセージ (このフラグが **OR** で、前のVCDIR_PREVが展開されている場合。</span><span class="sxs-lookup"><span data-stu-id="77fc9-113">The last message in the previous view category if this flag is **OR** ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="77fc9-114">前のビュー カテゴリの最初のメッセージ (このフラグが **OR** で、前のVCDIR_PREVが展開されていない場合。</span><span class="sxs-lookup"><span data-stu-id="77fc9-114">The first message in the previous view category if this flag is **OR** ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="77fc9-115">この場合、前のカテゴリは自動的に展開されます。</span><span class="sxs-lookup"><span data-stu-id="77fc9-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="77fc9-116">VCDIR_DELETE: 現在のメッセージが削除されたため、ビューアーは次または前のメッセージをアクティブにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="77fc9-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="77fc9-117">VCDIR_MOVE: 現在のメッセージが移動されたため、ビューアーは次または前のメッセージをアクティブにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="77fc9-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="77fc9-118">VCDIR_NEXT: ビューアーは、ビューの順序で次のメッセージをアクティブにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="77fc9-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="77fc9-119">VCDIR_PREV: ビューアーは、ビューの順序で前のメッセージをアクティブにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="77fc9-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="77fc9-120">VCDIR_UNREAD: ビューアーは、ビューの順序で次または前の未読メッセージをアクティブにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="77fc9-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="77fc9-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="77fc9-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="77fc9-122">[in]アクティブ化されたWindows表示するウィンドウのサイズと位置を含む **RECT** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="77fc9-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="77fc9-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="77fc9-123">Return value</span></span>

<span data-ttu-id="77fc9-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="77fc9-124">S_OK</span></span> 
  
> <span data-ttu-id="77fc9-125">メッセージが正常にアクティブ化されました。</span><span class="sxs-lookup"><span data-stu-id="77fc9-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="77fc9-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="77fc9-126">S_FALSE</span></span> 
  
> <span data-ttu-id="77fc9-127">メッセージは正常にアクティブ化されましたが、プロセスで別の種類のフォームが開かされました。</span><span class="sxs-lookup"><span data-stu-id="77fc9-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77fc9-128">注釈</span><span class="sxs-lookup"><span data-stu-id="77fc9-128">Remarks</span></span>

<span data-ttu-id="77fc9-129">フォーム オブジェクトは **IMAPIViewContext::ActivateNext** メソッドを呼び出して、ユーザーに表示されるメッセージを変更します。</span><span class="sxs-lookup"><span data-stu-id="77fc9-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="77fc9-130">_ulDir_ パラメーターで渡される値は、アクティブ化するメッセージと、場合によっては理由を示します。</span><span class="sxs-lookup"><span data-stu-id="77fc9-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="77fc9-131">このVCDIR_NEXTおよびVCDIR_PREVIOUSは、ビューで [**次** へ] または [前へ] コマンドをそれぞれ選択したユーザーに対応します。</span><span class="sxs-lookup"><span data-stu-id="77fc9-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="77fc9-132">通常、これらの操作は、フォーム ビューアーのメッセージの一覧で 1 つのメッセージを上下に移動する操作に対応します。</span><span class="sxs-lookup"><span data-stu-id="77fc9-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="77fc9-133">このVCDIR_DELETEおよびVCDIR_MOVEフラグは [、IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) メソッドと [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) メソッドによってそれぞれ設定されます。</span><span class="sxs-lookup"><span data-stu-id="77fc9-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="77fc9-134">これらのメソッドの実装では **、ActivateNext** を適切な方向に呼び出し **、ActivateNext** 呼び出しが失敗しなかった場合は、メッセージに対して要求された操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="77fc9-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="77fc9-135">通常、フォーム ビューアーを使用すると、ユーザーはメッセージ リスト内を移動する方向を指定できます。</span><span class="sxs-lookup"><span data-stu-id="77fc9-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="77fc9-136">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="77fc9-136">Notes to implementers</span></span>

<span data-ttu-id="77fc9-137">[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)の実装では _、ulDir_ の値に応じて、フォルダー内の次または前のメッセージが現在のメッセージになります。</span><span class="sxs-lookup"><span data-stu-id="77fc9-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="77fc9-138">**ActivateNext が返** された後 [、IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md)を呼び出して、新しくアクティブ化されたメッセージへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="77fc9-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="77fc9-139">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="77fc9-139">Notes to callers</span></span>

<span data-ttu-id="77fc9-140">**ActivateNext** が S_FALSE を返す場合、または現在のメッセージが存在しない場合は、フォームの [IMAPIForm::ShutdownForm](imapiform-shutdownform.md)メソッドの呼び出しを含む通常のシャットダウン手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="77fc9-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="77fc9-141">次または前のメッセージが表示される場合は  _、prcPosRect_ パラメーターで渡されたウィンドウ四角形を使用して表示します。</span><span class="sxs-lookup"><span data-stu-id="77fc9-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="77fc9-142">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="77fc9-142">MFCMAPI reference</span></span>

<span data-ttu-id="77fc9-143">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77fc9-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="77fc9-144">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="77fc9-144">**File**</span></span>|<span data-ttu-id="77fc9-145">**関数**</span><span class="sxs-lookup"><span data-stu-id="77fc9-145">**Function**</span></span>|<span data-ttu-id="77fc9-146">**コメント**</span><span class="sxs-lookup"><span data-stu-id="77fc9-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="77fc9-147">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="77fc9-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="77fc9-148">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="77fc9-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="77fc9-149">MFCMAPI は、 **この関数に IMAPIViewContext::ActivateNext メソッド** を実装します。</span><span class="sxs-lookup"><span data-stu-id="77fc9-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77fc9-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="77fc9-150">See also</span></span>

- [<span data-ttu-id="77fc9-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="77fc9-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="77fc9-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="77fc9-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- <span data-ttu-id="77fc9-153">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="77fc9-153">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

