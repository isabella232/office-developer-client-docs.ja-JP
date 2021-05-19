---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c25f352e7fa607a46741164574a4ba91d4026edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423581"
---
# <a name="imapiformmgrselectform"></a><span data-ttu-id="9fc5e-103">IMAPIFormMgr::SelectForm</span><span class="sxs-lookup"><span data-stu-id="9fc5e-103">IMAPIFormMgr::SelectForm</span></span>

  
  
<span data-ttu-id="9fc5e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fc5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fc5e-105">ユーザーがフォームを選択できるダイアログ ボックスを表示し、そのフォームを説明するフォーム情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-105">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a><span data-ttu-id="9fc5e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9fc5e-106">Parameters</span></span>

 <span data-ttu-id="9fc5e-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9fc5e-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="9fc5e-108">[in]表示されるダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="9fc5e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9fc5e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9fc5e-110">[in]渡された文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="9fc5e-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="9fc5e-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9fc5e-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9fc5e-113">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="9fc5e-114">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9fc5e-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="9fc5e-115">_pszTitle_</span></span>
  
> <span data-ttu-id="9fc5e-116">[in]ダイアログ ボックスのキャプションを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="9fc5e-117">_pszTitle パラメーターが_ NULL の場合、フォーム ライブラリ プロバイダーは既定のキャプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-117">If the  _pszTitle_ parameter is NULL, the form library provider supplies a default caption.</span></span> 
    
 <span data-ttu-id="9fc5e-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="9fc5e-118">_pfld_</span></span>
  
> <span data-ttu-id="9fc5e-119">[in]フォームを選択するフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-119">[in] A pointer to the folder from which to select the form.</span></span> <span data-ttu-id="9fc5e-120">_pfld パラメーターが_ NULL の場合、フォームはローカル、個人用、または組織のフォーム コンテナーから選択できます。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-120">If the  _pfld_ parameter is NULL, the form can be selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="9fc5e-121">_ppfrminfoReturned_</span><span class="sxs-lookup"><span data-stu-id="9fc5e-121">_ppfrminfoReturned_</span></span>
  
> <span data-ttu-id="9fc5e-122">[out]返されるフォーム情報オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-122">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9fc5e-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="9fc5e-123">Return value</span></span>

<span data-ttu-id="9fc5e-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="9fc5e-124">S_OK</span></span> 
  
> <span data-ttu-id="9fc5e-125">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="9fc5e-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9fc5e-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9fc5e-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9fc5e-127">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="9fc5e-128">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="9fc5e-128">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="9fc5e-129">通常、ユーザーはダイアログ ボックスの [キャンセル]ボタンをクリックして操作をキャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-129">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9fc5e-130">注釈</span><span class="sxs-lookup"><span data-stu-id="9fc5e-130">Remarks</span></span>

<span data-ttu-id="9fc5e-131">フォーム ビューアーは **IMAPIFormMgr::SelectForm** メソッドを呼び出して、ユーザーがフォームを選択できるダイアログ ボックスを表示し、次に選択したフォームを記述するフォーム情報オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-131">Form viewers call the **IMAPIFormMgr::SelectForm** method to first present a dialog box that enables the user to select a form and then to retrieve a form information object that describes the selected form.</span></span> <span data-ttu-id="9fc5e-132">ダイアログ ボックスでは、ユーザーが 1 つのフォームを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-132">The dialog box constrains the user to select a single form.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9fc5e-133">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="9fc5e-133">Notes to callers</span></span>

<span data-ttu-id="9fc5e-134">**[SelectForm]** ダイアログ ボックスには、非表示ではないフォーム (つまり、非表示のプロパティがクリアされているフォーム) だけが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-134">The **SelectForm** dialog box displays only forms that are not hidden (that is, forms that have their hidden properties clear).</span></span> <span data-ttu-id="9fc5e-135">フォーム ビューアーが  _ulFlags_ パラメーター MAPI_UNICODEフラグを渡す場合、すべての文字列は Unicode です。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-135">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="9fc5e-136">Unicode 文字列をサポートしないフォーム ライブラリ プロバイダーは、渡された場合MAPI_E_BAD_CHARWIDTHをMAPI_UNICODEする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-136">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9fc5e-137">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="9fc5e-137">MFCMAPI reference</span></span>

<span data-ttu-id="9fc5e-138">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9fc5e-139">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="9fc5e-139">**File**</span></span>|<span data-ttu-id="9fc5e-140">**関数**</span><span class="sxs-lookup"><span data-stu-id="9fc5e-140">**Function**</span></span>|<span data-ttu-id="9fc5e-141">**コメント**</span><span class="sxs-lookup"><span data-stu-id="9fc5e-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9fc5e-142">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9fc5e-142">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="9fc5e-143">CFolderDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="9fc5e-143">CFolderDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="9fc5e-144">MFCMAPI は **IMAPIFormMgr::SelectForm** メソッドを使用してフォームを選択し、フォームに関する情報を 1 つ以上のログに送信します。</span><span class="sxs-lookup"><span data-stu-id="9fc5e-144">MFCMAPI uses the **IMAPIFormMgr::SelectForm** method to select a form and send information about the form to one or more logs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fc5e-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="9fc5e-145">See also</span></span>



[<span data-ttu-id="9fc5e-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9fc5e-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


<span data-ttu-id="9fc5e-147">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="9fc5e-147">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

