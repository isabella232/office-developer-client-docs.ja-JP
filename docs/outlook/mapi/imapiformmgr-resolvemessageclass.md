---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426395"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="c5578-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="c5578-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="c5578-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5578-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5578-105">メッセージ クラスをフォーム コンテナー内のフォームに解決し、そのフォームのフォーム情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="c5578-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="c5578-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c5578-106">Parameters</span></span>

 <span data-ttu-id="c5578-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="c5578-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="c5578-108">[in]解決されるメッセージ クラスの名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="c5578-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="c5578-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c5578-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c5578-110">[in]メッセージ クラスの解決方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="c5578-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="c5578-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c5578-111">The following flag can be set:</span></span>
    
<span data-ttu-id="c5578-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="c5578-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="c5578-113">完全に一致するメッセージ クラスの文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5578-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="c5578-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="c5578-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="c5578-115">[in]解決するメッセージを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c5578-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="c5578-116">_pFolderFocus パラメーター_ には NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c5578-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="c5578-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="c5578-117">_ppResult_</span></span>
  
> <span data-ttu-id="c5578-118">[out]返されるフォーム情報オブジェクトへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="c5578-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c5578-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="c5578-119">Return value</span></span>

<span data-ttu-id="c5578-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="c5578-120">S_OK</span></span> 
  
> <span data-ttu-id="c5578-121">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="c5578-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c5578-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c5578-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c5578-123">_szMsgClass_ パラメーターで渡されたメッセージ クラスは、フォーム ライブラリ内のフォームのメッセージ クラスと一致しません。</span><span class="sxs-lookup"><span data-stu-id="c5578-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c5578-124">注釈</span><span class="sxs-lookup"><span data-stu-id="c5578-124">Remarks</span></span>

<span data-ttu-id="c5578-125">フォーム ビューアーは **IMAPIFormMgr::ResolveMessageClass** メソッドを呼び出して、フォーム コンテナー内のフォームにメッセージ クラスを解決します。</span><span class="sxs-lookup"><span data-stu-id="c5578-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="c5578-126">_ppResult_ パラメーターで返されるフォーム情報オブジェクトは、指定されたメッセージ クラスを持つフォームのプロパティにさらにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c5578-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c5578-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c5578-127">Notes to callers</span></span>

<span data-ttu-id="c5578-128">メッセージ クラスをフォームに解決するために、フォーム ビューアーは解決するメッセージ クラスの名前 ("" など) を渡 `IPM.HelpDesk.Software` します。</span><span class="sxs-lookup"><span data-stu-id="c5578-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="c5578-129">解決を厳密に (つまり、完全に一致するフォーム サーバーが使用できない場合にメッセージ クラスの基本クラスの解決を防ぐため) には  _、ulFlags_ パラメーターに MAPIFORM_EXACTMATCH フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="c5578-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="c5578-130">_pFolderFocus パラメーター_ が NULL の場合、メッセージ クラス解決プロセスではフォルダー コンテナーは検索されません。</span><span class="sxs-lookup"><span data-stu-id="c5578-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="c5578-131">検索されるコンテナーの順序は、フォーム ライブラリ プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="c5578-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="c5578-132">既定のフォーム ライブラリ プロバイダーは、最初にローカル コンテナーを検索し、次にフォルダー コンテナーで、渡されたフォルダー、個人用フォーム コンテナー、最後に組織コンテナーを検索します。</span><span class="sxs-lookup"><span data-stu-id="c5578-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="c5578-133">メッセージ クラス名は常に ANSI 文字列で、Unicode は使用しません。</span><span class="sxs-lookup"><span data-stu-id="c5578-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="c5578-134">解決されたメッセージ クラスのクラス識別子は、フォーム情報オブジェクトの一部として返されます。</span><span class="sxs-lookup"><span data-stu-id="c5578-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="c5578-135">フォーム ビューアーは、フォーム ビューアーが [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) メソッドまたは [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) メソッドのいずれかを呼び出すまで、OLE ライブラリにクラス識別子が存在することを前提として機能しません。</span><span class="sxs-lookup"><span data-stu-id="c5578-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c5578-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="c5578-136">See also</span></span>



[<span data-ttu-id="c5578-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c5578-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="c5578-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="c5578-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="c5578-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="c5578-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="c5578-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c5578-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

