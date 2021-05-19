---
title: IMAPISessionLogoff
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338109"
---
# <a name="imapisessionlogoff"></a><span data-ttu-id="00448-103">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="00448-103">IMAPISession::Logoff</span></span>

  
  
<span data-ttu-id="00448-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00448-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00448-105">MAPI セッションを終了します。</span><span class="sxs-lookup"><span data-stu-id="00448-105">Ends a MAPI session.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a><span data-ttu-id="00448-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="00448-106">Parameters</span></span>

 <span data-ttu-id="00448-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="00448-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="00448-108">[in]表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="00448-108">[in] A handle to the parent window of any dialog boxes or windows to be displayed.</span></span> <span data-ttu-id="00448-109">このパラメーターは、フラグが設定されていないMAPI_LOGOFF_UI無視されます。</span><span class="sxs-lookup"><span data-stu-id="00448-109">This parameter is ignored if the MAPI_LOGOFF_UI flag is not set.</span></span>
    
 <span data-ttu-id="00448-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="00448-110">_ulFlags_</span></span>
  
> <span data-ttu-id="00448-111">[in]ログオフ操作を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="00448-111">[in] A bitmask of flags that control the logoff operation.</span></span> <span data-ttu-id="00448-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="00448-112">The following flags can be set:</span></span>
    
<span data-ttu-id="00448-113">MAPI_LOGOFF_SHARED</span><span class="sxs-lookup"><span data-stu-id="00448-113">MAPI_LOGOFF_SHARED</span></span> 
  
> <span data-ttu-id="00448-114">このセッションが共有されている場合は、共有セッションを使用してログオンしたすべてのクライアントに、進行中のログオフが通知されます。</span><span class="sxs-lookup"><span data-stu-id="00448-114">If this session is shared, all clients that logged on by using the shared session should be notified of the logoff in progress.</span></span> <span data-ttu-id="00448-115">クライアントはログオフする必要があります。</span><span class="sxs-lookup"><span data-stu-id="00448-115">The clients should log off.</span></span> <span data-ttu-id="00448-116">共有セッションを使用しているクライアントは、このフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="00448-116">Any client that is using the shared session can set this flag.</span></span> <span data-ttu-id="00448-117">MAPI_LOGOFF_SHAREDセッションが共有されていない場合、この値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="00448-117">MAPI_LOGOFF_SHARED is ignored if the current session is not shared.</span></span>
    
<span data-ttu-id="00448-118">MAPI_LOGOFF_UI</span><span class="sxs-lookup"><span data-stu-id="00448-118">MAPI_LOGOFF_UI</span></span> 
  
> <span data-ttu-id="00448-119">**ログオフ** では、操作中にダイアログ ボックスを表示し、ユーザーに確認を求めるメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="00448-119">**Logoff** can display a dialog box during the operation, possibly prompting the user for confirmation.</span></span> 
    
 <span data-ttu-id="00448-120">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="00448-120">_ulReserved_</span></span>
  
> <span data-ttu-id="00448-121">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="00448-121">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="00448-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="00448-122">Return value</span></span>

<span data-ttu-id="00448-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="00448-123">S_OK</span></span> 
  
> <span data-ttu-id="00448-124">ログオフ操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="00448-124">The logoff operation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="00448-125">注釈</span><span class="sxs-lookup"><span data-stu-id="00448-125">Remarks</span></span>

<span data-ttu-id="00448-126">**IMAPISession::Logoff メソッドは** MAPI セッションを終了します。</span><span class="sxs-lookup"><span data-stu-id="00448-126">The **IMAPISession::Logoff** method ends a MAPI session.</span></span> <span data-ttu-id="00448-127">**Logoff が返** された場合 [、IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)以外のメソッドは呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="00448-127">When **Logoff** returns, none of the methods except for [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) can be called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="00448-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="00448-128">Notes to callers</span></span>

<span data-ttu-id="00448-129">**Logoff が返** された場合は、その **IUnknown::Release** メソッドを呼び出してセッション オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="00448-129">When **Logoff** returns, release the session object by calling its **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="00448-130">セッションの終了の詳細については、「MAPI セッションの [終了」を参照してください](ending-a-mapi-session.md)。</span><span class="sxs-lookup"><span data-stu-id="00448-130">For more information about ending a session, see [Ending a MAPI Session](ending-a-mapi-session.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="00448-131">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="00448-131">MFCMAPI reference</span></span>

<span data-ttu-id="00448-132">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00448-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="00448-133">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="00448-133">**File**</span></span>|<span data-ttu-id="00448-134">**関数**</span><span class="sxs-lookup"><span data-stu-id="00448-134">**Function**</span></span>|<span data-ttu-id="00448-135">**コメント**</span><span class="sxs-lookup"><span data-stu-id="00448-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="00448-136">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="00448-136">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="00448-137">CMapiObjects::Logoff</span><span class="sxs-lookup"><span data-stu-id="00448-137">CMapiObjects::Logoff</span></span>  <br/> |<span data-ttu-id="00448-138">MFCMAPI は **IMAPISession::Logoff** メソッドを使用して、セッションを解放する前にセッションからログオフします。</span><span class="sxs-lookup"><span data-stu-id="00448-138">MFCMAPI uses the **IMAPISession::Logoff** method to log off from the session before releasing it.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="00448-139">Microsoft Office Outlook 2007 Service Pack 2、Microsoft Outlook 2010、および Microsoft Outlook 2013 で導入された高速シャットダウン動作のため、クライアントは **MAPI_LOGOFF_SHARED** パラメーターを [IMAPISession::Logoff](imapisession-logoff.md)に渡す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="00448-139">Due to the fast shutdown behavior introduced in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010, and Microsoft Outlook 2013, clients should never pass the **MAPI_LOGOFF_SHARED** parameter to [IMAPISession::Logoff](imapisession-logoff.md).</span></span> <span data-ttu-id="00448-140">この **MAPI_LOGOFF_SHARED** すると、すべての MAPI クライアントがシャットダウンを開始し、予期しない動作が発生します。</span><span class="sxs-lookup"><span data-stu-id="00448-140">Passing **MAPI_LOGOFF_SHARED** will cause all MAPI clients to begin shutdown and unexpected behavior will occur.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00448-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="00448-141">See also</span></span>



[<span data-ttu-id="00448-142">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="00448-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="00448-143">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="00448-143">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="00448-144">MAPI セッションの終了</span><span class="sxs-lookup"><span data-stu-id="00448-144">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)

