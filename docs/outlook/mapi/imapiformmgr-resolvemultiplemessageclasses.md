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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321869"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="b9d5a-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="b9d5a-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="b9d5a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9d5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9d5a-105">フォームコンテナー内のフォームに対するメッセージクラスのグループを解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="b9d5a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b9d5a-106">Parameters</span></span>

 <span data-ttu-id="b9d5a-107">_pmsgclasses_</span><span class="sxs-lookup"><span data-stu-id="b9d5a-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="b9d5a-108">順番解決するメッセージクラスの名前を含む配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="b9d5a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b9d5a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b9d5a-110">順番メッセージクラスの解決方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="b9d5a-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-111">The following flag can be set:</span></span>
    
<span data-ttu-id="b9d5a-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="b9d5a-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="b9d5a-113">完全一致のメッセージクラス文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="b9d5a-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="b9d5a-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="b9d5a-115">キャッシュされたフォームを含めないでください。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="b9d5a-116">_pfolderfocus_</span><span class="sxs-lookup"><span data-stu-id="b9d5a-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="b9d5a-117">順番メッセージクラスが解決されるフォームを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="b9d5a-118">_pfolderfocus_パラメーターは NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="b9d5a-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="b9d5a-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="b9d5a-120">読み上げフォーム情報オブジェクトの配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="b9d5a-121">フォームビューアーが_pmsgclasses_パラメーターで NULL を渡す場合、 _ppfrminfoarray_パラメーターには、コンテナー内のすべてのフォームのフォーム情報オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b9d5a-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="b9d5a-122">Return value</span></span>

<span data-ttu-id="b9d5a-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9d5a-123">S_OK</span></span> 
  
> <span data-ttu-id="b9d5a-124">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b9d5a-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b9d5a-125">解説</span><span class="sxs-lookup"><span data-stu-id="b9d5a-125">Remarks</span></span>

<span data-ttu-id="b9d5a-126">フォームビューアーは、 **imapiformmgr:: ResolveMultipleMessageClasses**メソッドを呼び出して、フォームコンテナー内のフォームに対するメッセージクラスのグループを解決します。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="b9d5a-127">_ppfrminfoarray_で返されるフォーム情報オブジェクトの配列は、各フォームのプロパティへのアクセスをさらに提供します。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b9d5a-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b9d5a-128">Notes to callers</span></span>

<span data-ttu-id="b9d5a-129">メッセージクラスのグループをフォームに解決するために、フォームビューアーは解決されるメッセージクラス名の配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="b9d5a-130">解決策を強制的に正確なものにする (つまり、正確に一致するフォームサーバーが使用できない場合にメッセージクラスの基本クラスを解決できないようにする) には、MAPIFORM_EXACTMATCH フラグを_ulflags_パラメーターで渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="b9d5a-131">メッセージクラス名は常に ANSI 文字列で、Unicode はありません。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="b9d5a-132">メッセージクラスをフォームに解決できない場合は、フォーム情報配列でそのメッセージクラスに対して NULL が返されます。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="b9d5a-133">そのため、メソッドが S_OK を返す場合でも、フォームビューアーは、すべてのメッセージクラスが正常に解決されたという前提では機能しません。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="b9d5a-134">代わりに、フォームビューアーは、返される配列内の値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9d5a-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b9d5a-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9d5a-135">See also</span></span>



[<span data-ttu-id="b9d5a-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="b9d5a-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="b9d5a-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9d5a-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

