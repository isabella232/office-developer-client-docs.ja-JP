---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b974b733c24e61cb256ac0cf7b377d5630966fdf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579292"
---
# <a name="imapiformmgrselectmultipleforms"></a><span data-ttu-id="5e881-103">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="5e881-103">IMAPIFormMgr::SelectMultipleForms</span></span>

  
  
<span data-ttu-id="5e881-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e881-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e881-105">複数のフォームを選択するユーザーを有効にする] ダイアログ ボックスを表示し、それらのフォームを記述するオブジェクトの情報、フォームの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="5e881-105">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>
  
```cpp
HRESULT SelectMultipleForms(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFOARRAY pfrminfoarray,
  LPMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="5e881-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e881-106">Parameters</span></span>

 <span data-ttu-id="5e881-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5e881-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="5e881-108">[in]表示されたダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="5e881-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="5e881-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e881-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5e881-110">[in]渡された文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="5e881-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="5e881-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5e881-111">The following flag can be set:</span></span>
    
<span data-ttu-id="5e881-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5e881-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5e881-113">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="5e881-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="5e881-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="5e881-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="5e881-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="5e881-115">_pszTitle_</span></span>
  
> <span data-ttu-id="5e881-116">[in]ダイアログ ボックスのキャプションを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5e881-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="5e881-117">_PszTitle_パラメーターが NULL の場合は、フォームを提供するフォーム ライブラリ プロバイダーは、既定のキャプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="5e881-117">If the  _pszTitle_ parameter is NULL, the form library provider that provides the forms supplies a default caption.</span></span> 
    
 <span data-ttu-id="5e881-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="5e881-118">_pfld_</span></span>
  
> <span data-ttu-id="5e881-119">[in]フォームを選択するフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5e881-119">[in] A pointer to the folder from which to select the forms.</span></span> <span data-ttu-id="5e881-120">_Pfld_パラメーターが NULL の場合は、ローカル、個人、または組織フォームのコンテナーから、フォームが選択されます。</span><span class="sxs-lookup"><span data-stu-id="5e881-120">If the  _pfld_ parameter is NULL, the forms are selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="5e881-121">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="5e881-121">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="5e881-122">[in]ユーザーに事前に選択されているフォーム情報オブジェクトの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5e881-122">[in] A pointer to an array of form information objects that are preselected for the user.</span></span>
    
 <span data-ttu-id="5e881-123">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="5e881-123">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="5e881-124">[out]フォーム情報オブジェクトの返される配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5e881-124">[out] A pointer to a pointer to the returned array of form information objects.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e881-125">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5e881-125">Return value</span></span>

<span data-ttu-id="5e881-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e881-126">S_OK</span></span> 
  
> <span data-ttu-id="5e881-127">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="5e881-127">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="5e881-128">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5e881-128">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5e881-129">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5e881-129">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="5e881-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="5e881-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="5e881-131">ユーザー操作がキャンセルされました、通常] ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="5e881-131">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5e881-132">注釈</span><span class="sxs-lookup"><span data-stu-id="5e881-132">Remarks</span></span>

<span data-ttu-id="5e881-133">フォーム ビューアー メソッドを呼び出して、 **IMAPIFormMgr::SelectMultipleForms**を最初の存在により、ユーザーが複数のフォームを選択するダイアログ ボックスと、フォームの配列を取得するために情報オブジェクトを選択したフォームを記述します。</span><span class="sxs-lookup"><span data-stu-id="5e881-133">Form viewers call the **IMAPIFormMgr::SelectMultipleForms** method to first present a dialog box that enables the user to select multiple forms and then to retrieve an array of form information objects that describe the selected forms.</span></span> <span data-ttu-id="5e881-134">**SelectMultipleForms** ] ダイアログ ボックスでは、(つまり、かどうか、非表示のプロパティは、クリア) が非表示にするかどうか、すべてのフォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e881-134">The **SelectMultipleForms** dialog box displays all forms, whether or not they are hidden (that is, whether or not their hidden properties are clear).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5e881-135">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="5e881-135">Notes to implementers</span></span>

<span data-ttu-id="5e881-136">_UlFlags_パラメーターで、フォームのビューアーが MAPI_UNICODE フラグを渡すと、すべての文字列は Unicode です。</span><span class="sxs-lookup"><span data-stu-id="5e881-136">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="5e881-137">Unicode 文字列をサポートしていないフォーム ライブラリ プロバイダーは、MAPI_UNICODE が渡された場合、MAPI_E_BAD_CHARWIDTH を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e881-137">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5e881-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e881-138">See also</span></span>



[<span data-ttu-id="5e881-139">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e881-139">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

