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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b481eaf00b7568da5f02ffa3301e8f2698a98e1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800567"
---
# <a name="imapiformmgrselectform"></a><span data-ttu-id="0bc60-103">IMAPIFormMgr::SelectForm</span><span class="sxs-lookup"><span data-stu-id="0bc60-103">IMAPIFormMgr::SelectForm</span></span>

  
  
<span data-ttu-id="0bc60-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0bc60-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0bc60-105">、フォームを選択するユーザーを有効にする] ダイアログ ボックスを表示し、そのフォームを記述するフォームの情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="0bc60-105">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a><span data-ttu-id="0bc60-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0bc60-106">Parameters</span></span>

 <span data-ttu-id="0bc60-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0bc60-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="0bc60-108">[in]表示されたダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="0bc60-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="0bc60-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0bc60-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0bc60-110">[in]渡された文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="0bc60-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="0bc60-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="0bc60-111">The following flag can be set:</span></span>
    
<span data-ttu-id="0bc60-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0bc60-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0bc60-113">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="0bc60-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="0bc60-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="0bc60-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="0bc60-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="0bc60-115">_pszTitle_</span></span>
  
> <span data-ttu-id="0bc60-116">[in]ダイアログ ボックスのキャプションを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0bc60-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="0bc60-117">_PszTitle_パラメーターが NULL の場合は、フォーム ライブラリのプロバイダーは、既定のキャプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="0bc60-117">If the  _pszTitle_ parameter is NULL, the form library provider supplies a default caption.</span></span> 
    
 <span data-ttu-id="0bc60-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="0bc60-118">_pfld_</span></span>
  
> <span data-ttu-id="0bc60-119">[in]フォームを選択するフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0bc60-119">[in] A pointer to the folder from which to select the form.</span></span> <span data-ttu-id="0bc60-120">_Pfld_パラメーターが NULL の場合は、ローカル、個人、または組織フォームのコンテナーから、フォームを選択できます。</span><span class="sxs-lookup"><span data-stu-id="0bc60-120">If the  _pfld_ parameter is NULL, the form can be selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="0bc60-121">_ppfrminfoReturned_</span><span class="sxs-lookup"><span data-stu-id="0bc60-121">_ppfrminfoReturned_</span></span>
  
> <span data-ttu-id="0bc60-122">[out]返されたフォームの情報オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0bc60-122">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0bc60-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0bc60-123">Return value</span></span>

<span data-ttu-id="0bc60-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="0bc60-124">S_OK</span></span> 
  
> <span data-ttu-id="0bc60-125">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="0bc60-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0bc60-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0bc60-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0bc60-127">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0bc60-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="0bc60-128">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="0bc60-128">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="0bc60-129">ユーザー操作がキャンセルされました、通常] ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="0bc60-129">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0bc60-130">備考</span><span class="sxs-lookup"><span data-stu-id="0bc60-130">Remarks</span></span>

<span data-ttu-id="0bc60-131">フォーム ビューアー メソッドを呼び出して、 **IMAPIFormMgr::SelectForm**最初の存在するフォームを選択するユーザーを有効にする] ダイアログ ボックスと、選択したフォームを説明する情報のフォーム オブジェクトを取得するために、します。</span><span class="sxs-lookup"><span data-stu-id="0bc60-131">Form viewers call the **IMAPIFormMgr::SelectForm** method to first present a dialog box that enables the user to select a form and then to retrieve a form information object that describes the selected form.</span></span> <span data-ttu-id="0bc60-132">ダイアログ ボックスには、1 つのフォームを選択するのにはユーザーが制限されます。</span><span class="sxs-lookup"><span data-stu-id="0bc60-132">The dialog box constrains the user to select a single form.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0bc60-133">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="0bc60-133">Notes to callers</span></span>

<span data-ttu-id="0bc60-134">**SelectForm** ] ダイアログ ボックスには、隠されていないフォームのみが表示されます (つまり、非表示のプロパティを持つフォームをオフに)。</span><span class="sxs-lookup"><span data-stu-id="0bc60-134">The **SelectForm** dialog box displays only forms that are not hidden (that is, forms that have their hidden properties clear).</span></span> <span data-ttu-id="0bc60-135">_UlFlags_パラメーターで、フォームのビューアーが MAPI_UNICODE フラグを渡すと、すべての文字列は Unicode です。</span><span class="sxs-lookup"><span data-stu-id="0bc60-135">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="0bc60-136">Unicode 文字列をサポートしていないフォーム ライブラリ プロバイダーは、MAPI_UNICODE が渡された場合、MAPI_E_BAD_CHARWIDTH を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0bc60-136">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0bc60-137">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="0bc60-137">MFCMAPI reference</span></span>

<span data-ttu-id="0bc60-138">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="0bc60-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0bc60-139">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="0bc60-139">**File**</span></span>|<span data-ttu-id="0bc60-140">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="0bc60-140">**Function**</span></span>|<span data-ttu-id="0bc60-141">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="0bc60-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0bc60-142">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0bc60-142">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="0bc60-143">CFolderDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="0bc60-143">CFolderDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="0bc60-144">MFCMAPI では、 **IMAPIFormMgr::SelectForm**メソッドを使用して、フォームを選択し、フォームに関する情報を 1 つまたは複数のログに送信します。</span><span class="sxs-lookup"><span data-stu-id="0bc60-144">MFCMAPI uses the **IMAPIFormMgr::SelectForm** method to select a form and send information about the form to one or more logs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0bc60-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="0bc60-145">See also</span></span>



[<span data-ttu-id="0bc60-146">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0bc60-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


<span data-ttu-id="0bc60-147">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="0bc60-147">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

