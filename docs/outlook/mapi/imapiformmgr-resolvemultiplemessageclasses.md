---
title: IMAPIFormMgrResolveMultipleMessageClasses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 515061c6c208008c4752e5ff2f23933a4c259c00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428019"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="8e984-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="8e984-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="8e984-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e984-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e984-105">メッセージ クラスのグループをフォーム コンテナー内のフォームに解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="8e984-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="8e984-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8e984-106">Parameters</span></span>

 <span data-ttu-id="8e984-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="8e984-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="8e984-108">[in]解決するメッセージ クラスの名前を含む配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8e984-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="8e984-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e984-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8e984-110">[in]メッセージ クラスの解決方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8e984-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="8e984-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8e984-111">The following flag can be set:</span></span>
    
<span data-ttu-id="8e984-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="8e984-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="8e984-113">完全に一致するメッセージ クラスの文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e984-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="8e984-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="8e984-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="8e984-115">キャッシュされたフォームは含めない。</span><span class="sxs-lookup"><span data-stu-id="8e984-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="8e984-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="8e984-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="8e984-117">[in]メッセージ クラスが解決されるフォームを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8e984-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="8e984-118">_pFolderFocus パラメーター_ には NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="8e984-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="8e984-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="8e984-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="8e984-120">[out]フォーム情報オブジェクトの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8e984-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="8e984-121">_pMsgClasses_ パラメーターでフォーム ビューアーが NULL を渡す場合 _、ppfrminfoarray_ パラメーターには、コンテナー内のすべてのフォームのフォーム情報オブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8e984-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8e984-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="8e984-122">Return value</span></span>

<span data-ttu-id="8e984-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e984-123">S_OK</span></span> 
  
> <span data-ttu-id="8e984-124">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="8e984-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e984-125">注釈</span><span class="sxs-lookup"><span data-stu-id="8e984-125">Remarks</span></span>

<span data-ttu-id="8e984-126">フォーム ビューアーは **IMAPIFormMgr::ResolveMultipleMessageClasses** メソッドを呼び出して、メッセージ クラスのグループをフォーム コンテナー内のフォームに解決します。</span><span class="sxs-lookup"><span data-stu-id="8e984-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="8e984-127">_ppfrminfoarray_ で返されるフォーム情報オブジェクトの配列は、フォームの各プロパティにさらにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8e984-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8e984-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="8e984-128">Notes to callers</span></span>

<span data-ttu-id="8e984-129">メッセージ クラスのグループをフォームに解決するために、フォーム ビューアーは解決するメッセージ クラス名の配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="8e984-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="8e984-130">解決を厳密に強制するには (つまり、完全に一致するフォーム サーバーが使用できない場合にメッセージ クラスの基本クラスの解決を防ぐため)、MAPIFORM_EXACTMATCH フラグを  _ulFlags_ パラメーターに渡します。</span><span class="sxs-lookup"><span data-stu-id="8e984-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="8e984-131">メッセージ クラス名は常に ANSI 文字列で、Unicode は使用しません。</span><span class="sxs-lookup"><span data-stu-id="8e984-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="8e984-132">メッセージ クラスをフォームに解決できない場合、フォーム情報配列内のそのメッセージ クラスに対して NULL が返されます。</span><span class="sxs-lookup"><span data-stu-id="8e984-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="8e984-133">したがって、メソッドがメッセージ クラスを返S_OK、フォーム ビューアーは、すべてのメッセージ クラスが正常に解決されたという前提で動作しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e984-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="8e984-134">代わりに、フォームビューアーは返された配列の値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e984-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e984-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e984-135">See also</span></span>



[<span data-ttu-id="8e984-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="8e984-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="8e984-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e984-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

