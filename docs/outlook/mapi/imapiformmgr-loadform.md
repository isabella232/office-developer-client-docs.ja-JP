---
title: IMAPIFormMgrLoadForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418786"
---
# <a name="imapiformmgrloadform"></a><span data-ttu-id="e6816-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="e6816-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="e6816-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6816-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6816-105">既存のメッセージを開くフォームを開始します。</span><span class="sxs-lookup"><span data-stu-id="e6816-105">Starts a form to open an existing message.</span></span>
  
```cpp
HRESULT LoadForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pmsg,
  LPMAPIVIEWCONTEXT pViewContext,
  REFIID riid,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="e6816-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e6816-106">Parameters</span></span>

 <span data-ttu-id="e6816-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="e6816-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="e6816-108">順番フォームが開かれている間に表示される進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="e6816-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="e6816-109">_uluiparam_パラメーターは、 _ulflags_パラメーターで MAPI_DIALOG フラグが設定されていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="e6816-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="e6816-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e6816-110">_ulFlags_</span></span>
  
> <span data-ttu-id="e6816-111">順番フォームを開く方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e6816-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="e6816-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e6816-112">The following flags can be set:</span></span>
    
<span data-ttu-id="e6816-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e6816-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="e6816-114">状態を提供するユーザーインターフェイスを表示します。詳細については、ユーザーに確認します。</span><span class="sxs-lookup"><span data-stu-id="e6816-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="e6816-115">このフラグが設定されていない場合、ユーザーインターフェイスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="e6816-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="e6816-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="e6816-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="e6816-117">完全一致のメッセージクラス文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6816-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="e6816-118">_lpszmessageclass_</span><span class="sxs-lookup"><span data-stu-id="e6816-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="e6816-119">順番読み込むメッセージのメッセージクラスの名前を示す文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6816-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="e6816-120">NULL が_lpszmessageclass_パラメーターで渡された場合、メッセージクラスは_pmsg_パラメーターによって示されるメッセージから判断されます。</span><span class="sxs-lookup"><span data-stu-id="e6816-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="e6816-121">_ulmessagestatus_</span><span class="sxs-lookup"><span data-stu-id="e6816-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="e6816-122">順番メッセージの状態に関する情報を提供する、メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされた、クライアント定義またはプロバイダー定義のフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e6816-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="e6816-123">_lpszmessageclass_が NULL 以外の場合は_ulmessagestatus_パラメーターを設定する必要があります。それ以外の場合、 _ulmessagestatus_は無視されます。</span><span class="sxs-lookup"><span data-stu-id="e6816-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="e6816-124">_ulmessageflags_</span><span class="sxs-lookup"><span data-stu-id="e6816-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="e6816-125">順番メッセージの現在の状態を示す、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6816-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="e6816-126">_lpszmessageclass_が NULL 以外の場合は、 _ulmessageflags_パラメーターを設定する必要があります。それ以外の場合、 _ulmessageflags_は無視されます。</span><span class="sxs-lookup"><span data-stu-id="e6816-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="e6816-127">_pfolderfocus_</span><span class="sxs-lookup"><span data-stu-id="e6816-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="e6816-128">順番直接メッセージを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6816-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="e6816-129">このようなフォルダーが存在しない場合 (たとえば、メッセージが別のメッセージに埋め込まれている場合) は、 _pfolderfocus_パラメーターを NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="e6816-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="e6816-130">_pメッセージ ite_</span><span class="sxs-lookup"><span data-stu-id="e6816-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="e6816-131">順番メッセージのメッセージサイトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6816-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="e6816-132">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="e6816-132">_pmsg_</span></span>
  
> <span data-ttu-id="e6816-133">順番メッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6816-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="e6816-134">_pviewcontext_</span><span class="sxs-lookup"><span data-stu-id="e6816-134">_pViewContext_</span></span>
  
> <span data-ttu-id="e6816-135">順番メッセージのビューコンテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6816-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="e6816-136">_pviewcontext_パラメーターは NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="e6816-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="e6816-137">_riid_</span><span class="sxs-lookup"><span data-stu-id="e6816-137">_riid_</span></span>
  
> <span data-ttu-id="e6816-138">順番返される form オブジェクトに対して使用されるインターフェイスのインターフェイス識別子 (IID)。</span><span class="sxs-lookup"><span data-stu-id="e6816-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="e6816-139">_riid_パラメーターを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e6816-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="e6816-140">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="e6816-140">_ppvObj_</span></span>
  
> <span data-ttu-id="e6816-141">読み上げ返されるインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6816-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6816-142">戻り値</span><span class="sxs-lookup"><span data-stu-id="e6816-142">Return value</span></span>

<span data-ttu-id="e6816-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6816-143">S_OK</span></span> 
  
> <span data-ttu-id="e6816-144">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e6816-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="e6816-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="e6816-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="e6816-146">フォームでは、要求されたインターフェイスがサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e6816-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="e6816-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e6816-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="e6816-148">_lpszmessageclass_で渡されるメッセージクラスが、フォームライブラリ内のフォームのメッセージクラスと一致しません。</span><span class="sxs-lookup"><span data-stu-id="e6816-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e6816-149">注釈</span><span class="sxs-lookup"><span data-stu-id="e6816-149">Remarks</span></span>

<span data-ttu-id="e6816-150">フォーム閲覧者は、 **imapiformmgr:: loadform**メソッドを呼び出して、既存のメッセージのフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="e6816-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="e6816-151">**loadform**は form オブジェクトを開き、form オブジェクトにメッセージを読み込み、必要に応じて適切なビューコンテキストを設定し、form オブジェクトの要求されたインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="e6816-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="e6816-152">_pfolderfocus_パラメーターは、メッセージを含むフォルダーを指します。</span><span class="sxs-lookup"><span data-stu-id="e6816-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="e6816-153">メッセージが別のメッセージに埋め込まれている場合、 _pfolderfocus_は NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6816-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e6816-154">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="e6816-154">Notes to implementers</span></span>

<span data-ttu-id="e6816-155">_lpszmessageclass_で NULL が渡されると、メッセージのメッセージクラス、状態、およびフラグがメッセージの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))、 **PR_MSG_STATUS** 、および PR_MESSAGE_FLAGS から取得されます。 \*\*\*\* プロパティ。</span><span class="sxs-lookup"><span data-stu-id="e6816-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="e6816-156">メッセージクラスの文字列が_lpszmessageclass_で提供されている場合、この実装では_ulmessagestatus_および_ulmessagestatus_の値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6816-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e6816-157">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="e6816-157">MFCMAPI reference</span></span>

<span data-ttu-id="e6816-158">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e6816-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e6816-159">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="e6816-159">**File**</span></span>|<span data-ttu-id="e6816-160">**関数**</span><span class="sxs-lookup"><span data-stu-id="e6816-160">**Function**</span></span>|<span data-ttu-id="e6816-161">**コメント**</span><span class="sxs-lookup"><span data-stu-id="e6816-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e6816-162">MAPIFormFunctions</span><span class="sxs-lookup"><span data-stu-id="e6816-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="e6816-163">openmessagenonmodal</span><span class="sxs-lookup"><span data-stu-id="e6816-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="e6816-164">mfcmapi は、 **imapiformmgr:: loadform**メソッドを使用して、表示する前にフォームを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="e6816-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6816-165">関連項目</span><span class="sxs-lookup"><span data-stu-id="e6816-165">See also</span></span>



[<span data-ttu-id="e6816-166">PidTagMessageClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e6816-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="e6816-167">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e6816-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="e6816-168">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e6816-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="e6816-169">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6816-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


<span data-ttu-id="e6816-170">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="e6816-170">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

