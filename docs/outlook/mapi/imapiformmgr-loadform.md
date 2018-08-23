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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1f3a876269868c30df48e0a0b62036cfdc199955
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800549"
---
# <a name="imapiformmgrloadform"></a><span data-ttu-id="aa170-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="aa170-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="aa170-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa170-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa170-105">フォームを開くには既存のメッセージを開始します。</span><span class="sxs-lookup"><span data-stu-id="aa170-105">Starts a form to open an existing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="aa170-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="aa170-106">Parameters</span></span>

 <span data-ttu-id="aa170-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="aa170-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="aa170-108">[in]フォームを開いたときに表示される進行状況のインジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="aa170-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="aa170-109">_UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _ulUIParam_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="aa170-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="aa170-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aa170-110">_ulFlags_</span></span>
  
> <span data-ttu-id="aa170-111">[in]フォームを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="aa170-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="aa170-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="aa170-112">The following flags can be set:</span></span>
    
<span data-ttu-id="aa170-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="aa170-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="aa170-114">ステータスを指定するか、詳細についてはユーザーの入力を求めるのためのユーザー インターフェイスを表示します。</span><span class="sxs-lookup"><span data-stu-id="aa170-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="aa170-115">このフラグが設定されていない場合、ユーザー インターフェイスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="aa170-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="aa170-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="aa170-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="aa170-117">完全に一致するメッセージ クラス文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa170-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="aa170-118">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="aa170-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="aa170-119">[in]読み込まれるメッセージのメッセージ クラスの名前を示す文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="aa170-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="aa170-120">_LpszMessageClass_パラメーターに NULL を渡した場合、メッセージ クラスは、 _pmsg_パラメーターで指定されたメッセージから判断されます。</span><span class="sxs-lookup"><span data-stu-id="aa170-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="aa170-121">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="aa170-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="aa170-122">[in]メッセージの状態に関する情報を提供するメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティからコピーしたクライアント定義またはプロバイダー定義のフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="aa170-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="aa170-123">_LpszMessageClass_は、NULL 以外の場合、 _ulMessageStatus_パラメーターを設定する必要があります。それ以外の場合、 _ulMessageStatus_は無視されます。</span><span class="sxs-lookup"><span data-stu-id="aa170-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="aa170-124">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="aa170-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="aa170-125">[in]フラグは、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティ、メッセージの現在の状態を示すメッセージのコピーのビットマップへのポインター。</span><span class="sxs-lookup"><span data-stu-id="aa170-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="aa170-126">_LpszMessageClass_は、NULL 以外の場合、 _ulMessageFlags_パラメーターを設定する必要があります。それ以外の場合、 _ulMessageFlags_は無視されます。</span><span class="sxs-lookup"><span data-stu-id="aa170-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="aa170-127">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="aa170-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="aa170-128">[in]直接メッセージを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="aa170-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="aa170-129">_PFolderFocus_パラメーターは、(たとえば、メッセージは、別のメッセージに埋め込まれている) 場合、このようなフォルダーが存在しない場合、NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="aa170-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="aa170-130">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="aa170-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="aa170-131">[in]メッセージのメッセージのサイトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="aa170-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="aa170-132">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="aa170-132">_pmsg_</span></span>
  
> <span data-ttu-id="aa170-133">[in]メッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="aa170-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="aa170-134">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="aa170-134">_pViewContext_</span></span>
  
> <span data-ttu-id="aa170-135">[in]メッセージのビュー コンテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="aa170-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="aa170-136">_PViewContext_パラメーターは NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="aa170-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="aa170-137">_riid_</span><span class="sxs-lookup"><span data-stu-id="aa170-137">_riid_</span></span>
  
> <span data-ttu-id="aa170-138">[in]返信されたフォーム オブジェクトに使用するインターフェイスのインターフェイス id (IID)。</span><span class="sxs-lookup"><span data-stu-id="aa170-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="aa170-139">_Riid_パラメーターを NULL にする必要がありますはできません。</span><span class="sxs-lookup"><span data-stu-id="aa170-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="aa170-140">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="aa170-140">_ppvObj_</span></span>
  
> <span data-ttu-id="aa170-141">[out]返されたインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="aa170-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa170-142">�߂�l</span><span class="sxs-lookup"><span data-stu-id="aa170-142">Return value</span></span>

<span data-ttu-id="aa170-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa170-143">S_OK</span></span> 
  
> <span data-ttu-id="aa170-144">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="aa170-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="aa170-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="aa170-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="aa170-146">フォームは、要求されたインターフェイスをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="aa170-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="aa170-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="aa170-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="aa170-148">_LpszMessageClass_に渡されるメッセージ クラスでは、フォーム ライブラリ内の任意のフォームのメッセージ クラスが一致しません。</span><span class="sxs-lookup"><span data-stu-id="aa170-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="aa170-149">注釈</span><span class="sxs-lookup"><span data-stu-id="aa170-149">Remarks</span></span>

<span data-ttu-id="aa170-150">フォームの閲覧者は、既存のメッセージのフォームを開くに**IMAPIFormMgr::LoadForm**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aa170-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="aa170-151">**LoadForm**フォーム オブジェクトを開きます、フォーム オブジェクトにメッセージを読み込みます、必要に応じて、適切なビューのコンテキストを設定し、フォーム オブジェクトの要求されたインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="aa170-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="aa170-152">_PFolderFocus_パラメーターは、メッセージを含むフォルダーを指します。</span><span class="sxs-lookup"><span data-stu-id="aa170-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="aa170-153">メッセージは、別のメッセージに埋め込まれている場合_pFolderFocus_は NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa170-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="aa170-154">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="aa170-154">Notes to implementers</span></span>

<span data-ttu-id="aa170-155">実装がメッセージの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))、 **PR_MSG_STATUS** **PR_MESSAGE_FLAGS から、メッセージのメッセージ クラス、状態、およびフラグを取得する場合は_lpszMessageClass_に NULL が渡されると、** プロパティ。</span><span class="sxs-lookup"><span data-stu-id="aa170-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="aa170-156">_LpszMessageClass_のメッセージ クラスの文字列を指定すると、実装は_ulMessageStatus_と_ulMessageFlags_の値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa170-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="aa170-157">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="aa170-157">MFCMAPI reference</span></span>

<span data-ttu-id="aa170-158">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="aa170-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aa170-159">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="aa170-159">**File**</span></span>|<span data-ttu-id="aa170-160">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="aa170-160">**Function**</span></span>|<span data-ttu-id="aa170-161">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="aa170-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa170-162">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="aa170-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="aa170-163">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="aa170-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="aa170-164">MFCMAPI では、 **IMAPIFormMgr::LoadForm**メソッドを使用して、表示する前にフォームをロードします。</span><span class="sxs-lookup"><span data-stu-id="aa170-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa170-165">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa170-165">See also</span></span>



[<span data-ttu-id="aa170-166">PidTagMessageClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aa170-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="aa170-167">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aa170-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="aa170-168">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aa170-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="aa170-169">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa170-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


<span data-ttu-id="aa170-170">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="aa170-170">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

