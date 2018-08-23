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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ad2014d1d003a4d80646ed1b679f0d3827341c1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800558"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="e3037-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e3037-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="e3037-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e3037-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e3037-105">フォームのコンテナー内でユーザーがフォームにメッセージ クラスのグループを解決し、それらのフォームのオブジェクトの情報、フォームの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="e3037-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="e3037-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e3037-106">Parameters</span></span>

 <span data-ttu-id="e3037-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="e3037-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="e3037-108">[in]解決するのにはメッセージ クラスの名前を格納している配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e3037-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="e3037-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e3037-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e3037-110">[in]メッセージ クラスを解決する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="e3037-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="e3037-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e3037-111">The following flag can be set:</span></span>
    
<span data-ttu-id="e3037-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="e3037-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="e3037-113">完全に一致するメッセージ クラス文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3037-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="e3037-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="e3037-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="e3037-115">キャッシュされたフォームは含まれません。</span><span class="sxs-lookup"><span data-stu-id="e3037-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="e3037-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="e3037-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="e3037-117">[in]メッセージ クラスを解決するフォームを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e3037-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="e3037-118">_PFolderFocus_パラメーターは NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="e3037-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="e3037-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="e3037-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="e3037-120">[out]フォーム情報オブジェクトの配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e3037-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="e3037-121">フォーム ビューアーでは、 _pMsgClasses_パラメーターに NULL が成功した場合、 _ppfrminfoarray_パラメーターには、フォームのコンテナー内のすべてのフォーム オブジェクト情報にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e3037-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e3037-122">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e3037-122">Return value</span></span>

<span data-ttu-id="e3037-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3037-123">S_OK</span></span> 
  
> <span data-ttu-id="e3037-124">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e3037-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3037-125">����</span><span class="sxs-lookup"><span data-stu-id="e3037-125">Remarks</span></span>

<span data-ttu-id="e3037-126">フォームの閲覧者は、フォームのコンテナー内のフォームにメッセージ クラスのグループを解決するのには**IMAPIFormMgr::ResolveMultipleMessageClasses**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e3037-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="e3037-127">フォーム_ppfrminfoarray_で返されるオブジェクトの情報の配列の各フォームのプロパティへのアクセスをさらに提供します。</span><span class="sxs-lookup"><span data-stu-id="e3037-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e3037-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e3037-128">Notes to callers</span></span>

<span data-ttu-id="e3037-129">メッセージ クラスのグループを解決するには、フォームに、フォーム ビューアーを解決するメッセージ クラス名の配列で渡します。</span><span class="sxs-lookup"><span data-stu-id="e3037-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="e3037-130">正確な解像度を強制する (つまりと正確に一致する、フォーム、のメッセージ クラスの基本クラスの解像度を防止するためにサーバーは使用できません)、 _ulFlags_パラメーターでは、MAPIFORM_EXACTMATCH フラグを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="e3037-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="e3037-131">メッセージ クラス名は、常に ANSI 文字列を Unicode ではないです。</span><span class="sxs-lookup"><span data-stu-id="e3037-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="e3037-132">フォームにメッセージ クラスを解決できない場合は、フォーム情報の配列では、そのメッセージ クラスの NULL が返されます。</span><span class="sxs-lookup"><span data-stu-id="e3037-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="e3037-133">したがって、場合でも、このメソッドは S_OK を返します、フォームの閲覧者必要があります動作しないすべてのメッセージ クラスが正常に解決されたことを前提としています。</span><span class="sxs-lookup"><span data-stu-id="e3037-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="e3037-134">代わりに、フォームのビューアーは、返される配列内の値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3037-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e3037-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3037-135">See also</span></span>



[<span data-ttu-id="e3037-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="e3037-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="e3037-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3037-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

