---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c6e18ee9f8ea1d7dc6592d576c5a1163db526639
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321666"
---
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="eb13a-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="eb13a-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="eb13a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb13a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb13a-105">フォームのメッセージクラスに基づいて新しいメッセージを作成するためのフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="eb13a-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="eb13a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="eb13a-106">Parameters</span></span>

 <span data-ttu-id="eb13a-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="eb13a-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="eb13a-108">順番フォームが開かれている間に表示される進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="eb13a-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="eb13a-109">_uluiparam_パラメーターは、 _ulflags_パラメーターで MAPI_DIALOG フラグが設定されていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="eb13a-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="eb13a-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eb13a-110">_ulFlags_</span></span>
  
> <span data-ttu-id="eb13a-111">順番フォームを開く方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="eb13a-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="eb13a-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="eb13a-112">The following flag can be set:</span></span>
    
<span data-ttu-id="eb13a-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="eb13a-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="eb13a-114">状態を提供するユーザーインターフェイスを表示します。詳細については、ユーザーに確認します。</span><span class="sxs-lookup"><span data-stu-id="eb13a-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="eb13a-115">このフラグが設定されていない場合、ユーザーインターフェイスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="eb13a-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="eb13a-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="eb13a-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="eb13a-117">順番フォームを開くために使用されるフォーム情報オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="eb13a-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="eb13a-118">_refiidtoask_</span><span class="sxs-lookup"><span data-stu-id="eb13a-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="eb13a-119">順番作成された form オブジェクトに対して返されるインターフェイスのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="eb13a-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="eb13a-120">_refiidtoask_パラメーターを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="eb13a-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="eb13a-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="eb13a-121">_ppvObj_</span></span>
  
> <span data-ttu-id="eb13a-122">読み上げ返されるインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="eb13a-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eb13a-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="eb13a-123">Return value</span></span>

<span data-ttu-id="eb13a-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb13a-124">S_OK</span></span> 
  
> <span data-ttu-id="eb13a-125">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="eb13a-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="eb13a-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="eb13a-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="eb13a-127">要求されたインターフェイスは、form オブジェクトでサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="eb13a-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb13a-128">解説</span><span class="sxs-lookup"><span data-stu-id="eb13a-128">Remarks</span></span>

<span data-ttu-id="eb13a-129">フォーム閲覧者は、 **imapiformmgr:: CreateForm**メソッドを呼び出して、フォームのメッセージクラスに基づいて新しいメッセージを作成するためのフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="eb13a-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="eb13a-130">指定したフォーム情報オブジェクトで説明されているフォームのフォームサーバーのインスタンスを作成することによって、 **CreateForm**によってフォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="eb13a-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="eb13a-131">必要に応じて、 **CreateForm**は[imapiformmgr::P repareform](imapiformmgr-prepareform.md)メソッドを呼び出して、フォームサーバーコードをユーザーのディスクにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="eb13a-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="eb13a-132">_pfrminfoToActivate_パラメーターは、正しく解決されたフォーム情報オブジェクトを指している必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb13a-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="eb13a-133">フォームを開いた後、呼び出し元フォームビューアーでは、 [IPersistMessage](ipersistmessageiunknown.md)インターフェイスを使用してメッセージを設定し、必要に応じてフォームのビューコンテキストを設定できます。</span><span class="sxs-lookup"><span data-stu-id="eb13a-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="eb13a-134">詳細については、「[フォームサーバーの起動](launching-a-form-server.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb13a-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="eb13a-135">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="eb13a-135">MFCMAPI reference</span></span>

<span data-ttu-id="eb13a-136">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb13a-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="eb13a-137">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="eb13a-137">**File**</span></span>|<span data-ttu-id="eb13a-138">**関数**</span><span class="sxs-lookup"><span data-stu-id="eb13a-138">**Function**</span></span>|<span data-ttu-id="eb13a-139">**コメント**</span><span class="sxs-lookup"><span data-stu-id="eb13a-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eb13a-140">MAPIFormFunctions</span><span class="sxs-lookup"><span data-stu-id="eb13a-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="eb13a-141">createanddisplaynewmailinfolder</span><span class="sxs-lookup"><span data-stu-id="eb13a-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="eb13a-142">mfcmapi は、 **imapiformmgr:: CreateForm**メソッドを使用して、表示する前にフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="eb13a-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb13a-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb13a-143">See also</span></span>



[<span data-ttu-id="eb13a-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="eb13a-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="eb13a-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb13a-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="eb13a-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb13a-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


<span data-ttu-id="eb13a-147">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="eb13a-147">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="eb13a-148">フォームサーバーの起動</span><span class="sxs-lookup"><span data-stu-id="eb13a-148">Launching a Form Server</span></span>](launching-a-form-server.md)

