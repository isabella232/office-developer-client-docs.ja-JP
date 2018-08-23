---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c1da292943d6e4d9625c6ce37019c630471e200b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800534"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a><span data-ttu-id="c2793-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="c2793-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="c2793-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c2793-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2793-105">フォームのコンテナー内のフォームにメッセージ クラスのグループを解決し、それらのフォームのオブジェクトの情報、フォームの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="c2793-105">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="c2793-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c2793-106">Parameters</span></span>

 <span data-ttu-id="c2793-107">_pMsgClassArray_</span><span class="sxs-lookup"><span data-stu-id="c2793-107">_pMsgClassArray_</span></span>
  
> <span data-ttu-id="c2793-108">[in]解決するのにはメッセージ クラスの名前を格納している配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c2793-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span> <span data-ttu-id="c2793-109">メッセージ クラス名は、常に ANSI 文字列を Unicode ではないです。</span><span class="sxs-lookup"><span data-stu-id="c2793-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="c2793-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c2793-110">_ulFlags_</span></span>
  
> <span data-ttu-id="c2793-111">[in]メッセージ クラスを解決する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="c2793-111">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="c2793-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c2793-112">The following flag can be set:</span></span>
    
<span data-ttu-id="c2793-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="c2793-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="c2793-114">完全に一致するメッセージ クラス文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2793-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="c2793-115">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="c2793-115">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="c2793-116">[out]フォーム情報オブジェクトの配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c2793-116">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="c2793-117">場合は、クライアント アプリケーションは、 _pMsgClassArray_パラメーターに NULL を渡す、 _ppfrminfoarray_パラメーターには、フォームのコンテナー内のすべてのフォーム オブジェクト情報にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c2793-117">If a client application passes NULL in the  _pMsgClassArray_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c2793-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c2793-118">Return value</span></span>

<span data-ttu-id="c2793-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2793-119">S_OK</span></span> 
  
> <span data-ttu-id="c2793-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="c2793-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2793-121">����</span><span class="sxs-lookup"><span data-stu-id="c2793-121">Remarks</span></span>

<span data-ttu-id="c2793-122">クライアント アプリケーションは、フォームのコンテナー内のフォームにメッセージ クラスのグループを解決するのには**IMAPIFormContainer::ResolveMultipleMessageClasses**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c2793-122">Client applications call the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="c2793-123">フォーム、 _ppfrminfoarray_パラメーターで返されるオブジェクトの情報の配列の各フォームのプロパティへのアクセスをさらに提供します。</span><span class="sxs-lookup"><span data-stu-id="c2793-123">The array of form information objects returned in the  _ppfrminfoarray_ parameter provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c2793-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c2793-124">Notes to callers</span></span>

<span data-ttu-id="c2793-125">メッセージ クラスのグループを解決するにはフォームに、解決するのにはメッセージ クラス名の配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="c2793-125">To resolve a group of message classes to forms, pass in an array of message class names to be resolved.</span></span> <span data-ttu-id="c2793-126">正確な解像度を強制的に (つまり、メッセージ クラスの基本クラスへの解像度を防ぐために)、 _ulFlags_パラメーターでは、MAPIFORM_EXACTMATCH フラグを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="c2793-126">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="c2793-127">フォームにメッセージ クラスを解決できない場合は、フォーム情報の配列では、そのメッセージ クラスの NULL が返されます。</span><span class="sxs-lookup"><span data-stu-id="c2793-127">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="c2793-128">したがって、場合でも、このメソッドは S_OK を返しますと仮定しないですべてのメッセージ クラスが正常に解決されていること。</span><span class="sxs-lookup"><span data-stu-id="c2793-128">Therefore, even if the method returns S_OK, do not assume that all message classes have been successfully resolved.</span></span> <span data-ttu-id="c2793-129">代わりに、返される配列内の値をチェックします。</span><span class="sxs-lookup"><span data-stu-id="c2793-129">Instead, check the values in the returned array.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c2793-130">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="c2793-130">MFCMAPI reference</span></span>

<span data-ttu-id="c2793-131">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="c2793-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c2793-132">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="c2793-132">**File**</span></span>|<span data-ttu-id="c2793-133">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="c2793-133">**Function**</span></span>|<span data-ttu-id="c2793-134">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="c2793-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c2793-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c2793-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="c2793-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="c2793-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span></span>  <br/> |<span data-ttu-id="c2793-137">MFCMAPI では、 **IMAPIFormContainer::ResolveMultipleMessageClasses**メソッドを使用して、一連のメッセージ クラスに関連付けられているフォームを見つけます。</span><span class="sxs-lookup"><span data-stu-id="c2793-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c2793-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="c2793-138">See also</span></span>



[<span data-ttu-id="c2793-139">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="c2793-139">IMAPIFormContainer::ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md)
  
[<span data-ttu-id="c2793-140">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2793-140">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


<span data-ttu-id="c2793-141">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c2793-141">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

