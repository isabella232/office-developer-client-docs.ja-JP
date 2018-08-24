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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6613e4168fea6536b1df873da12f2c215be515bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588504"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="c6f84-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="c6f84-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="c6f84-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6f84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6f84-105">ビューの順序で次または前のメッセージをアクティブにします。</span><span class="sxs-lookup"><span data-stu-id="c6f84-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="c6f84-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c6f84-106">Parameters</span></span>

<span data-ttu-id="c6f84-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="c6f84-107">_ulDir_</span></span>
  
> <span data-ttu-id="c6f84-108">[in]ステータスのフラグを有効にするメッセージに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c6f84-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="c6f84-109">有効なフラグの設定は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c6f84-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="c6f84-110">VCDIR_CATEGORY: ビューアーがビューの別のカテゴリでメッセージを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c6f84-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="c6f84-111">メッセージを有効にするのには次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c6f84-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="c6f84-112">このフラグが VCDIR_NEXT で、**または**ed の場合、次のビュー カテゴリの最初のメッセージです。</span><span class="sxs-lookup"><span data-stu-id="c6f84-112">The first message in the next view category if this flag is **OR**ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="c6f84-113">前のビューのカテゴリをこのフラグが VCDIR_PREV の**OR**演算の場合、前のカテゴリの最後のメッセージを展開します。</span><span class="sxs-lookup"><span data-stu-id="c6f84-113">The last message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="c6f84-114">前のビューのカテゴリをこのフラグが VCDIR_PREV の**OR**演算の場合、前のカテゴリの最初のメッセージが展開されていません。</span><span class="sxs-lookup"><span data-stu-id="c6f84-114">The first message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="c6f84-115">ここで前の分類では、自動拡張が行われます。</span><span class="sxs-lookup"><span data-stu-id="c6f84-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="c6f84-116">VCDIR_DELETE: ビューアーがアクティブに、次または前のメッセージの現在のメッセージが削除されたためです。</span><span class="sxs-lookup"><span data-stu-id="c6f84-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="c6f84-117">VCDIR_MOVE: ビューアーがアクティブに、次または前のメッセージの現在のメッセージが移動されたためです。</span><span class="sxs-lookup"><span data-stu-id="c6f84-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="c6f84-118">VCDIR_NEXT: ビューアーが表示順序の次のメッセージを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c6f84-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="c6f84-119">VCDIR_PREV: ビューアーが表示順序で前のメッセージを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c6f84-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="c6f84-120">VCDIR_UNREAD: ビューアーが表示順序で次または前の未読メ ッ セージを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c6f84-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="c6f84-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="c6f84-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="c6f84-122">[in]Windows **RECT**へのポインターでは、アクティブ化されたメッセージの表示に使用するウィンドウの位置とサイズを含む構造体です。</span><span class="sxs-lookup"><span data-stu-id="c6f84-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c6f84-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c6f84-123">Return value</span></span>

<span data-ttu-id="c6f84-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="c6f84-124">S_OK</span></span> 
  
> <span data-ttu-id="c6f84-125">メッセージは正常にアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="c6f84-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="c6f84-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="c6f84-126">S_FALSE</span></span> 
  
> <span data-ttu-id="c6f84-127">メッセージが正常にアクティブ化されたが、プロセスで開いているフォームの別の種類です。</span><span class="sxs-lookup"><span data-stu-id="c6f84-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6f84-128">注釈</span><span class="sxs-lookup"><span data-stu-id="c6f84-128">Remarks</span></span>

<span data-ttu-id="c6f84-129">フォーム オブジェクトは、ユーザーに表示されているメッセージを変更するのには**IMAPIViewContext::ActivateNext**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c6f84-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="c6f84-130">_UlDir_パラメーターで渡された値は、どのようなメッセージがアクティブ化され、一部にする必要があることを示します、場合によってはその理由です。</span><span class="sxs-lookup"><span data-stu-id="c6f84-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="c6f84-131">VCDIR_NEXT と VCDIR_PREVIOUS のフラグは、ユーザーがビューでは、**次**または**前**のコマンドを選択すると、それぞれに対応します。</span><span class="sxs-lookup"><span data-stu-id="c6f84-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="c6f84-132">これらの操作は、通常 1 つのメッセージのメッセージ フォーム ビューアーの一覧で上下に移動するのには対応しています。</span><span class="sxs-lookup"><span data-stu-id="c6f84-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="c6f84-133">VCDIR_DELETE と VCDIR_MOVE のフラグがそれぞれの[IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md)と[IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md)メソッドによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="c6f84-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="c6f84-134">これらのメソッドの実装は適切な方向で**ActivateNext**を呼び出すし、 **ActivateNext**の呼び出しが失敗しなかった場合、メッセージで要求された操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="c6f84-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="c6f84-135">フォーム ビューアーは、通常メッセージの一覧内を移動する方向を指定するユーザーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c6f84-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c6f84-136">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="c6f84-136">Notes to implementers</span></span>

<span data-ttu-id="c6f84-137">[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)の実装は、次または前のメッセージを_ulDir_、現在のメッセージの値に応じて、フォルダーになります。</span><span class="sxs-lookup"><span data-stu-id="c6f84-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="c6f84-138">**ActivateNext**が返されると、新しくアクティブになったメッセージへのポインターを取得するのには[IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c6f84-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c6f84-139">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c6f84-139">Notes to callers</span></span>

<span data-ttu-id="c6f84-140">**ActivateNext**は S_FALSE を返す場合、または現在のメッセージが存在しない場合は、フォームの[IMAPIForm::ShutdownForm](imapiform-shutdownform.md)メソッドを呼び出す必要がありますが、通常のシャット ダウン手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c6f84-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="c6f84-141">次または前のメッセージが表示されている場合は、表示するために、 _prcPosRect_パラメーターに渡されたウィンドウの四角形を使用します。</span><span class="sxs-lookup"><span data-stu-id="c6f84-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c6f84-142">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="c6f84-142">MFCMAPI reference</span></span>

<span data-ttu-id="c6f84-143">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="c6f84-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c6f84-144">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="c6f84-144">**File**</span></span>|<span data-ttu-id="c6f84-145">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="c6f84-145">**Function**</span></span>|<span data-ttu-id="c6f84-146">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="c6f84-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c6f84-147">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="c6f84-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="c6f84-148">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="c6f84-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="c6f84-149">MFCMAPI では、この関数では、 **IMAPIViewContext::ActivateNext**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="c6f84-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6f84-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="c6f84-150">See also</span></span>

- [<span data-ttu-id="c6f84-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="c6f84-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="c6f84-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6f84-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- <span data-ttu-id="c6f84-153">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c6f84-153">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

