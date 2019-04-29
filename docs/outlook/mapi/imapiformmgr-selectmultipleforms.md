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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c40d853c49645638c2ec4001d86e64a1b2d2e381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420312"
---
# <a name="imapiformmgrselectmultipleforms"></a><span data-ttu-id="33c5e-103">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="33c5e-103">IMAPIFormMgr::SelectMultipleForms</span></span>

  
  
<span data-ttu-id="33c5e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33c5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33c5e-105">ユーザーが複数のフォームを選択できるようにするダイアログボックスを表示し、それらのフォームを記述するフォーム情報オブジェクトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="33c5e-105">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="33c5e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="33c5e-106">Parameters</span></span>

 <span data-ttu-id="33c5e-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="33c5e-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="33c5e-108">順番表示されるダイアログボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="33c5e-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="33c5e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="33c5e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="33c5e-110">順番渡された文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="33c5e-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="33c5e-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="33c5e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="33c5e-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="33c5e-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="33c5e-113">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="33c5e-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="33c5e-114">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="33c5e-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="33c5e-115">_psztitle_</span><span class="sxs-lookup"><span data-stu-id="33c5e-115">_pszTitle_</span></span>
  
> <span data-ttu-id="33c5e-116">順番ダイアログボックスのキャプションを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="33c5e-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="33c5e-117">_psztitle_パラメーターが NULL の場合は、フォームを提供するフォームライブラリプロバイダーが既定のキャプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="33c5e-117">If the  _pszTitle_ parameter is NULL, the form library provider that provides the forms supplies a default caption.</span></span> 
    
 <span data-ttu-id="33c5e-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="33c5e-118">_pfld_</span></span>
  
> <span data-ttu-id="33c5e-119">順番フォームを選択するフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="33c5e-119">[in] A pointer to the folder from which to select the forms.</span></span> <span data-ttu-id="33c5e-120">_pfld_パラメーターが NULL の場合、フォームはローカル、個人用、または組織のフォームコンテナーから選択されます。</span><span class="sxs-lookup"><span data-stu-id="33c5e-120">If the  _pfld_ parameter is NULL, the forms are selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="33c5e-121">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="33c5e-121">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="33c5e-122">順番ユーザー用に事前に作成されたフォーム情報オブジェクトの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="33c5e-122">[in] A pointer to an array of form information objects that are preselected for the user.</span></span>
    
 <span data-ttu-id="33c5e-123">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="33c5e-123">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="33c5e-124">読み上げフォーム情報オブジェクトの返された配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="33c5e-124">[out] A pointer to a pointer to the returned array of form information objects.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="33c5e-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="33c5e-125">Return value</span></span>

<span data-ttu-id="33c5e-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="33c5e-126">S_OK</span></span> 
  
> <span data-ttu-id="33c5e-127">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="33c5e-127">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="33c5e-128">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="33c5e-128">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="33c5e-129">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="33c5e-129">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="33c5e-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="33c5e-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="33c5e-131">ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="33c5e-131">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="33c5e-132">注釈</span><span class="sxs-lookup"><span data-stu-id="33c5e-132">Remarks</span></span>

<span data-ttu-id="33c5e-133">フォーム閲覧者は、次のように、 **imapiformmgr:: selectmultipleforms**メソッドを呼び出して、ユーザーが複数のフォームを選択できるようにするダイアログボックスを最初に表示し、選択したフォームを記述するフォーム情報オブジェクトの配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="33c5e-133">Form viewers call the **IMAPIFormMgr::SelectMultipleForms** method to first present a dialog box that enables the user to select multiple forms and then to retrieve an array of form information objects that describe the selected forms.</span></span> <span data-ttu-id="33c5e-134">[ **select複数のフォーム**] ダイアログボックスには、非表示になっているかどうかにかかわらず、すべてのフォームが表示されます (非表示のプロパティがクリアされているかどうかは表示されません)。</span><span class="sxs-lookup"><span data-stu-id="33c5e-134">The **SelectMultipleForms** dialog box displays all forms, whether or not they are hidden (that is, whether or not their hidden properties are clear).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="33c5e-135">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="33c5e-135">Notes to implementers</span></span>

<span data-ttu-id="33c5e-136">フォームビューアーが_ulflags_パラメーターの MAPI_UNICODE フラグを渡すと、すべての文字列が UNICODE になります。</span><span class="sxs-lookup"><span data-stu-id="33c5e-136">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="33c5e-137">Unicode 文字列をサポートしていないフォームライブラリプロバイダーは、MAPI_UNICODE が渡された場合は MAPI_E_BAD_CHARWIDTH を返します。</span><span class="sxs-lookup"><span data-stu-id="33c5e-137">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="33c5e-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="33c5e-138">See also</span></span>



[<span data-ttu-id="33c5e-139">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33c5e-139">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

