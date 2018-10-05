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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399649"
---
# <a name="imapisessionlogoff"></a><span data-ttu-id="72469-103">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="72469-103">IMAPISession::Logoff</span></span>

  
  
<span data-ttu-id="72469-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72469-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72469-105">MAPI セッションを終了します。</span><span class="sxs-lookup"><span data-stu-id="72469-105">Ends a MAPI session.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a><span data-ttu-id="72469-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="72469-106">Parameters</span></span>

 <span data-ttu-id="72469-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="72469-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="72469-108">[in]ハンドルのダイアログ ボックスの親ウィンドウまたはウィンドウを表示できます。</span><span class="sxs-lookup"><span data-stu-id="72469-108">[in] A handle to the parent window of any dialog boxes or windows to be displayed.</span></span> <span data-ttu-id="72469-109">MAPI_LOGOFF_UI フラグが設定されていない場合、このパラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="72469-109">This parameter is ignored if the MAPI_LOGOFF_UI flag is not set.</span></span>
    
 <span data-ttu-id="72469-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="72469-110">_ulFlags_</span></span>
  
> <span data-ttu-id="72469-111">[in]ログオフ操作を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="72469-111">[in] A bitmask of flags that control the logoff operation.</span></span> <span data-ttu-id="72469-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="72469-112">The following flags can be set:</span></span>
    
<span data-ttu-id="72469-113">MAPI_LOGOFF_SHARED</span><span class="sxs-lookup"><span data-stu-id="72469-113">MAPI_LOGOFF_SHARED</span></span> 
  
> <span data-ttu-id="72469-114">このセッションを共有すると、共有セッションを使用してログオンするすべてのクライアントが実行中のログオフ時の通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72469-114">If this session is shared, all clients that logged on by using the shared session should be notified of the logoff in progress.</span></span> <span data-ttu-id="72469-115">クライアントがログオフする必要があります。</span><span class="sxs-lookup"><span data-stu-id="72469-115">The clients should log off.</span></span> <span data-ttu-id="72469-116">共有セッションを使用している任意のクライアントは、このフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="72469-116">Any client that is using the shared session can set this flag.</span></span> <span data-ttu-id="72469-117">MAPI_LOGOFF_SHARED には、現在のセッションが共有されていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="72469-117">MAPI_LOGOFF_SHARED is ignored if the current session is not shared.</span></span>
    
<span data-ttu-id="72469-118">MAPI_LOGOFF_UI</span><span class="sxs-lookup"><span data-stu-id="72469-118">MAPI_LOGOFF_UI</span></span> 
  
> <span data-ttu-id="72469-119">**ログオフ**できますダイアログ ボックスを表示、操作中にユーザーに確認を要求する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="72469-119">**Logoff** can display a dialog box during the operation, possibly prompting the user for confirmation.</span></span> 
    
 <span data-ttu-id="72469-120">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="72469-120">_ulReserved_</span></span>
  
> <span data-ttu-id="72469-121">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="72469-121">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="72469-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="72469-122">Return value</span></span>

<span data-ttu-id="72469-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="72469-123">S_OK</span></span> 
  
> <span data-ttu-id="72469-124">ログオフ操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="72469-124">The logoff operation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72469-125">備考</span><span class="sxs-lookup"><span data-stu-id="72469-125">Remarks</span></span>

<span data-ttu-id="72469-126">**IMAPISession::Logoff**メソッドでは、MAPI セッションを終了します。</span><span class="sxs-lookup"><span data-stu-id="72469-126">The **IMAPISession::Logoff** method ends a MAPI session.</span></span> <span data-ttu-id="72469-127">**ログオフ**が返されるときは[リ ス](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)を除くメソッド呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="72469-127">When **Logoff** returns, none of the methods except for [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) can be called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="72469-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="72469-128">Notes to callers</span></span>

<span data-ttu-id="72469-129">**ログオフ**が返されるの\*\*\*\* メソッドを呼び出して、セッション オブジェクトを放します。</span><span class="sxs-lookup"><span data-stu-id="72469-129">When **Logoff** returns, release the session object by calling its **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="72469-130">セッションの終了についての詳細については、 [MAPI セッションを終了](ending-a-mapi-session.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72469-130">For more information about ending a session, see [Ending a MAPI Session](ending-a-mapi-session.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="72469-131">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="72469-131">MFCMAPI reference</span></span>

<span data-ttu-id="72469-132">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72469-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="72469-133">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="72469-133">**File**</span></span>|<span data-ttu-id="72469-134">**関数**</span><span class="sxs-lookup"><span data-stu-id="72469-134">**Function**</span></span>|<span data-ttu-id="72469-135">**コメント**</span><span class="sxs-lookup"><span data-stu-id="72469-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="72469-136">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="72469-136">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="72469-137">CMapiObjects::Logoff</span><span class="sxs-lookup"><span data-stu-id="72469-137">CMapiObjects::Logoff</span></span>  <br/> |<span data-ttu-id="72469-138">MFCMAPI では、 **IMAPISession::Logoff**メソッドを使用して、それを解放する前にセッションからログオフします。</span><span class="sxs-lookup"><span data-stu-id="72469-138">MFCMAPI uses the **IMAPISession::Logoff** method to log off from the session before releasing it.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="72469-139">、Microsoft Office Outlook 2007 Service Pack 2、Microsoft Outlook 2010 では、および Microsoft Outlook 2013 で導入された高速シャット ダウンの動作のためクライアントは**MAPI_LOGOFF_SHARED**パラメーターを[IMAPISession::Logoff](imapisession-logoff.md)にことはありません渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="72469-139">Due to the fast shutdown behavior introduced in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010, and Microsoft Outlook 2013, clients should never pass the **MAPI_LOGOFF_SHARED** parameter to [IMAPISession::Logoff](imapisession-logoff.md).</span></span> <span data-ttu-id="72469-140">**MAPI_LOGOFF_SHARED**を渡すと、すべての MAPI クライアントをシャット ダウンを開始して、予期しない動作が発生します。</span><span class="sxs-lookup"><span data-stu-id="72469-140">Passing **MAPI_LOGOFF_SHARED** will cause all MAPI clients to begin shutdown and unexpected behavior will occur.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="72469-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="72469-141">See also</span></span>



[<span data-ttu-id="72469-142">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="72469-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="72469-143">コード サンプルとしての MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="72469-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="72469-144">MAPI セッションの終了</span><span class="sxs-lookup"><span data-stu-id="72469-144">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)

