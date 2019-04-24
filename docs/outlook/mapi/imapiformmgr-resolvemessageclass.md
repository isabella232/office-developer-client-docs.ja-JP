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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321610"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="d9668-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="d9668-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="d9668-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9668-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9668-105">form コンテナー内のフォームに対してメッセージクラスを解決し、そのフォームのフォーム情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="d9668-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="d9668-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9668-106">Parameters</span></span>

 <span data-ttu-id="d9668-107">_szmsgclass_</span><span class="sxs-lookup"><span data-stu-id="d9668-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="d9668-108">順番解決されるメッセージクラスの名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="d9668-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="d9668-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d9668-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d9668-110">順番メッセージクラスの解決方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="d9668-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="d9668-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d9668-111">The following flag can be set:</span></span>
    
<span data-ttu-id="d9668-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="d9668-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="d9668-113">完全一致のメッセージクラス文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9668-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="d9668-114">_pfolderfocus_</span><span class="sxs-lookup"><span data-stu-id="d9668-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="d9668-115">順番解決されるメッセージを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9668-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="d9668-116">_pfolderfocus_パラメーターは NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="d9668-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d9668-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="d9668-117">_ppResult_</span></span>
  
> <span data-ttu-id="d9668-118">読み上げ返されるフォーム情報オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9668-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9668-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9668-119">Return value</span></span>

<span data-ttu-id="d9668-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9668-120">S_OK</span></span> 
  
> <span data-ttu-id="d9668-121">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="d9668-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d9668-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d9668-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d9668-123">_szmsgclass_パラメーターで渡されたメッセージクラスが、フォームライブラリ内のフォームのメッセージクラスと一致しません。</span><span class="sxs-lookup"><span data-stu-id="d9668-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d9668-124">解説</span><span class="sxs-lookup"><span data-stu-id="d9668-124">Remarks</span></span>

<span data-ttu-id="d9668-125">フォームビューアーは、 **imapiformmgr:: ResolveMessageClass**メソッドを呼び出して、form コンテナー内のフォームにメッセージクラスを解決します。</span><span class="sxs-lookup"><span data-stu-id="d9668-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="d9668-126">_ppResult_パラメーターで返されるフォーム情報オブジェクトは、指定されたメッセージクラスを持つフォームのプロパティへのアクセスをさらに提供します。</span><span class="sxs-lookup"><span data-stu-id="d9668-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d9668-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d9668-127">Notes to callers</span></span>

<span data-ttu-id="d9668-128">メッセージクラスをフォームに解決するために、フォームビューアーは解決するメッセージクラスの名前 (" `IPM.HelpDesk.Software`" など) を渡します。</span><span class="sxs-lookup"><span data-stu-id="d9668-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="d9668-129">解像度を正確にする (つまり、正確に一致するフォームサーバーが使用できない場合にメッセージクラスの基本クラスに解決されないようにする) には、 _ulflags_パラメーターに MAPIFORM_EXACTMATCH フラグを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="d9668-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="d9668-130">_pfolderfocus_パラメーターが NULL の場合、メッセージクラスの解決処理ではフォルダーコンテナーは検索されません。</span><span class="sxs-lookup"><span data-stu-id="d9668-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="d9668-131">検索されるコンテナーの順序は、フォームライブラリプロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="d9668-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="d9668-132">既定のフォームライブラリプロバイダーは、最初にローカルコンテナーを検索し、次に、渡されたフォルダーのフォルダーコンテナー、個人用フォームコンテナー、そして組織コンテナーを検索します。</span><span class="sxs-lookup"><span data-stu-id="d9668-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="d9668-133">メッセージクラス名は常に ANSI 文字列で、Unicode はありません。</span><span class="sxs-lookup"><span data-stu-id="d9668-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="d9668-134">解決されたメッセージクラスのクラス識別子は、フォーム情報オブジェクトの一部として返されます。</span><span class="sxs-lookup"><span data-stu-id="d9668-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="d9668-135">フォームビューアーが OLE ライブラリ内に存在することを前提としているのは、フォームビューアーが[imapiformmgr::P repareform](imapiformmgr-prepareform.md)メソッドまたは[imapiformmgr:: CreateForm](imapiformmgr-createform.md)メソッドを呼び出したときまでです。</span><span class="sxs-lookup"><span data-stu-id="d9668-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d9668-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9668-136">See also</span></span>



[<span data-ttu-id="d9668-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d9668-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="d9668-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="d9668-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="d9668-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="d9668-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="d9668-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9668-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

