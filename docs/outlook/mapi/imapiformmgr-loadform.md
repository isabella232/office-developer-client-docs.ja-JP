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
# <a name="imapiformmgrloadform"></a><span data-ttu-id="1c119-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="1c119-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="1c119-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c119-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c119-105">既存のメッセージを開くフォームを開始します。</span><span class="sxs-lookup"><span data-stu-id="1c119-105">Starts a form to open an existing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1c119-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1c119-106">Parameters</span></span>

 <span data-ttu-id="1c119-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1c119-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="1c119-108">[in]フォームを開いている間に表示される進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="1c119-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="1c119-109">_ulUIParam_ パラメーターは _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="1c119-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="1c119-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1c119-110">_ulFlags_</span></span>
  
> <span data-ttu-id="1c119-111">[in]フォームの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="1c119-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="1c119-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1c119-112">The following flags can be set:</span></span>
    
<span data-ttu-id="1c119-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1c119-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="1c119-114">ユーザー インターフェイスを表示して、状態を提供するか、ユーザーに詳細を求めるプロンプトを表示します。</span><span class="sxs-lookup"><span data-stu-id="1c119-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="1c119-115">このフラグが設定されていない場合、ユーザー インターフェイスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="1c119-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="1c119-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="1c119-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="1c119-117">完全に一致するメッセージ クラスの文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c119-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="1c119-118">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="1c119-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="1c119-119">[in]読み込むメッセージのメッセージ クラスを示す文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1c119-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="1c119-120">_lpszMessageClass_ パラメーターで NULL が渡された場合、メッセージ クラスは _pmsg_ パラメーターが指すメッセージから決定されます。</span><span class="sxs-lookup"><span data-stu-id="1c119-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="1c119-121">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="1c119-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="1c119-122">[in]メッセージの状態に関する情報を提供するメッセージの **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされたクライアント定義フラグまたはプロバイダー定義フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="1c119-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="1c119-123">_lpszMessageClass_ が NULL 以外の場合は _、ulMessageStatus_ パラメーターを設定する必要があります。それ以外の場合 _、ulMessageStatus は_ 無視されます。</span><span class="sxs-lookup"><span data-stu-id="1c119-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="1c119-124">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="1c119-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="1c119-125">[in]メッセージの現在の状態を示す **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1c119-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="1c119-126">_lpszMessageClass が_ NULL 以外の場合は _、ulMessageFlags_ パラメーターを設定する必要があります。それ以外の場合 _、ulMessageFlags は_ 無視されます。</span><span class="sxs-lookup"><span data-stu-id="1c119-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="1c119-127">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="1c119-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="1c119-128">[in]メッセージを直接含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1c119-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="1c119-129">_pFolderFocus_ パラメーターは、そのようなフォルダーが存在しない場合は NULL にできます (たとえば、メッセージが別のメッセージに埋め込まれている場合)。</span><span class="sxs-lookup"><span data-stu-id="1c119-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="1c119-130">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="1c119-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="1c119-131">[in]メッセージのメッセージ サイトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1c119-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="1c119-132">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="1c119-132">_pmsg_</span></span>
  
> <span data-ttu-id="1c119-133">[in]メッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1c119-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="1c119-134">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="1c119-134">_pViewContext_</span></span>
  
> <span data-ttu-id="1c119-135">[in]メッセージのビュー コンテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1c119-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="1c119-136">_pViewContext パラメーター_ には NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1c119-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="1c119-137">_riid_</span><span class="sxs-lookup"><span data-stu-id="1c119-137">_riid_</span></span>
  
> <span data-ttu-id="1c119-138">[in]返されるフォーム オブジェクトに使用するインターフェイスのインターフェイス識別子 (IID)。</span><span class="sxs-lookup"><span data-stu-id="1c119-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="1c119-139">_riid パラメーターは_ NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="1c119-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="1c119-140">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="1c119-140">_ppvObj_</span></span>
  
> <span data-ttu-id="1c119-141">[out]返されたインターフェイスへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="1c119-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1c119-142">戻り値</span><span class="sxs-lookup"><span data-stu-id="1c119-142">Return value</span></span>

<span data-ttu-id="1c119-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="1c119-143">S_OK</span></span> 
  
> <span data-ttu-id="1c119-144">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="1c119-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1c119-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="1c119-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="1c119-146">フォームは、要求されたインターフェイスをサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="1c119-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="1c119-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1c119-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1c119-148">_lpszMessageClass_ で渡されたメッセージ クラスは、フォーム ライブラリ内のフォームのメッセージ クラスと一致しません。</span><span class="sxs-lookup"><span data-stu-id="1c119-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1c119-149">注釈</span><span class="sxs-lookup"><span data-stu-id="1c119-149">Remarks</span></span>

<span data-ttu-id="1c119-150">フォーム ビューアーは **IMAPIFormMgr::LoadForm** メソッドを呼び出して、既存のメッセージのフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="1c119-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="1c119-151">**LoadForm** はフォーム オブジェクトを開き、メッセージをフォーム オブジェクトに読み込み、必要に応じて適切なビュー コンテキストを設定し、フォーム オブジェクトの要求されたインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="1c119-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="1c119-152">_pFolderFocus パラメーター_ は、メッセージを含むフォルダーをポイントします。</span><span class="sxs-lookup"><span data-stu-id="1c119-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="1c119-153">メッセージが別のメッセージに埋め込まれている場合  _、pFolderFocus は_ NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c119-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1c119-154">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="1c119-154">Notes to implementers</span></span>

<span data-ttu-id="1c119-155">_lpszMessageClass_ で NULL が渡された場合、実装はメッセージの PR_MESSAGE_CLASS [(PidTagMessageClass)、PR_MSG_STATUS](pidtagmessageclass-canonical-property.md)プロパティ、および PR_MESSAGE_FLAGS プロパティからメッセージのメッセージ クラス、状態、**フラグを取得** します。 </span><span class="sxs-lookup"><span data-stu-id="1c119-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="1c119-156">_lpszMessageClass_ にメッセージ クラス文字列が指定されている場合、実装では _ulMessageStatus_ および _ulMessageFlags の値を使用する必要があります_。</span><span class="sxs-lookup"><span data-stu-id="1c119-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1c119-157">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="1c119-157">MFCMAPI reference</span></span>

<span data-ttu-id="1c119-158">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c119-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1c119-159">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="1c119-159">**File**</span></span>|<span data-ttu-id="1c119-160">**関数**</span><span class="sxs-lookup"><span data-stu-id="1c119-160">**Function**</span></span>|<span data-ttu-id="1c119-161">**コメント**</span><span class="sxs-lookup"><span data-stu-id="1c119-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1c119-162">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1c119-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1c119-163">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="1c119-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="1c119-164">MFCMAPI では **、IMAPIFormMgr::LoadForm** メソッドを使用してフォームを読み込み、表示します。</span><span class="sxs-lookup"><span data-stu-id="1c119-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c119-165">関連項目</span><span class="sxs-lookup"><span data-stu-id="1c119-165">See also</span></span>



[<span data-ttu-id="1c119-166">PidTagMessageClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1c119-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="1c119-167">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1c119-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="1c119-168">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1c119-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="1c119-169">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1c119-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


<span data-ttu-id="1c119-170">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1c119-170">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

