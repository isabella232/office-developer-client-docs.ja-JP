---
title: imapisessionlogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338109"
---
# <a name="imapisessionlogoff"></a><span data-ttu-id="dc5f4-103">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="dc5f4-103">IMAPISession::Logoff</span></span>

  
  
<span data-ttu-id="dc5f4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc5f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc5f4-105">MAPI セッションを終了します。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-105">Ends a MAPI session.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a><span data-ttu-id="dc5f4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dc5f4-106">Parameters</span></span>

 <span data-ttu-id="dc5f4-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="dc5f4-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="dc5f4-108">順番表示されるダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-108">[in] A handle to the parent window of any dialog boxes or windows to be displayed.</span></span> <span data-ttu-id="dc5f4-109">MAPI_LOGOFF_UI フラグが設定されていない場合、このパラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-109">This parameter is ignored if the MAPI_LOGOFF_UI flag is not set.</span></span>
    
 <span data-ttu-id="dc5f4-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dc5f4-110">_ulFlags_</span></span>
  
> <span data-ttu-id="dc5f4-111">順番ログオフ操作を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-111">[in] A bitmask of flags that control the logoff operation.</span></span> <span data-ttu-id="dc5f4-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-112">The following flags can be set:</span></span>
    
<span data-ttu-id="dc5f4-113">MAPI_LOGOFF_SHARED</span><span class="sxs-lookup"><span data-stu-id="dc5f4-113">MAPI_LOGOFF_SHARED</span></span> 
  
> <span data-ttu-id="dc5f4-114">このセッションが共有されている場合、共有セッションを使用してログオンしたすべてのクライアントに、進行中のログオフが通知されます。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-114">If this session is shared, all clients that logged on by using the shared session should be notified of the logoff in progress.</span></span> <span data-ttu-id="dc5f4-115">クライアントはログオフする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-115">The clients should log off.</span></span> <span data-ttu-id="dc5f4-116">共有セッションを使用しているクライアントは、このフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-116">Any client that is using the shared session can set this flag.</span></span> <span data-ttu-id="dc5f4-117">現在のセッションが共有されていない場合、MAPI_LOGOFF_SHARED は無視されます。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-117">MAPI_LOGOFF_SHARED is ignored if the current session is not shared.</span></span>
    
<span data-ttu-id="dc5f4-118">MAPI_LOGOFF_UI</span><span class="sxs-lookup"><span data-stu-id="dc5f4-118">MAPI_LOGOFF_UI</span></span> 
  
> <span data-ttu-id="dc5f4-119">**ログオフ**操作中にダイアログボックスを表示することができます。ユーザーに確認を求めるメッセージが表示される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-119">**Logoff** can display a dialog box during the operation, possibly prompting the user for confirmation.</span></span> 
    
 <span data-ttu-id="dc5f4-120">_ulreserved_</span><span class="sxs-lookup"><span data-stu-id="dc5f4-120">_ulReserved_</span></span>
  
> <span data-ttu-id="dc5f4-121">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="dc5f4-121">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dc5f4-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="dc5f4-122">Return value</span></span>

<span data-ttu-id="dc5f4-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc5f4-123">S_OK</span></span> 
  
> <span data-ttu-id="dc5f4-124">ログオフ操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-124">The logoff operation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc5f4-125">解説</span><span class="sxs-lookup"><span data-stu-id="dc5f4-125">Remarks</span></span>

<span data-ttu-id="dc5f4-126">**imapisession:: Logoff**メソッドは MAPI セッションを終了します。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-126">The **IMAPISession::Logoff** method ends a MAPI session.</span></span> <span data-ttu-id="dc5f4-127">**Logoff**が戻ると、 [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)を除くすべてのメソッドを呼び出すことができなくなります。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-127">When **Logoff** returns, none of the methods except for [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) can be called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dc5f4-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="dc5f4-128">Notes to callers</span></span>

<span data-ttu-id="dc5f4-129">**ログオフ**時に、 **IUnknown:: release**メソッドを呼び出して session オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-129">When **Logoff** returns, release the session object by calling its **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="dc5f4-130">セッションを終了する方法の詳細については、「 [MAPI セッションを終了する](ending-a-mapi-session.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-130">For more information about ending a session, see [Ending a MAPI Session](ending-a-mapi-session.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dc5f4-131">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="dc5f4-131">MFCMAPI reference</span></span>

<span data-ttu-id="dc5f4-132">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dc5f4-133">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="dc5f4-133">**File**</span></span>|<span data-ttu-id="dc5f4-134">**関数**</span><span class="sxs-lookup"><span data-stu-id="dc5f4-134">**Function**</span></span>|<span data-ttu-id="dc5f4-135">**コメント**</span><span class="sxs-lookup"><span data-stu-id="dc5f4-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc5f4-136">MAPIObjects</span><span class="sxs-lookup"><span data-stu-id="dc5f4-136">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="dc5f4-137">cmapiobjects:: Logoff</span><span class="sxs-lookup"><span data-stu-id="dc5f4-137">CMapiObjects::Logoff</span></span>  <br/> |<span data-ttu-id="dc5f4-138">mfcmapi は、 **imapisession:: Logoff**メソッドを使用してセッションからログオフしてから、セッションを解放します。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-138">MFCMAPI uses the **IMAPISession::Logoff** method to log off from the session before releasing it.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="dc5f4-139">microsoft Office Outlook 2007 Service Pack 2、microsoft outlook 2010、および microsoft outlook 2013 で導入された高速シャットダウンの動作により、クライアントは**MAPI_LOGOFF_SHARED**パラメーターを[imapisession:: LOGOFF](imapisession-logoff.md)に渡すことはできません。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-139">Due to the fast shutdown behavior introduced in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010, and Microsoft Outlook 2013, clients should never pass the **MAPI_LOGOFF_SHARED** parameter to [IMAPISession::Logoff](imapisession-logoff.md).</span></span> <span data-ttu-id="dc5f4-140">**MAPI_LOGOFF_SHARED**を渡すと、すべての MAPI クライアントがシャットダウンを開始し、予期しない動作が発生します。</span><span class="sxs-lookup"><span data-stu-id="dc5f4-140">Passing **MAPI_LOGOFF_SHARED** will cause all MAPI clients to begin shutdown and unexpected behavior will occur.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dc5f4-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc5f4-141">See also</span></span>



[<span data-ttu-id="dc5f4-142">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dc5f4-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="dc5f4-143">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="dc5f4-143">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="dc5f4-144">MAPI セッションの終了</span><span class="sxs-lookup"><span data-stu-id="dc5f4-144">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)

