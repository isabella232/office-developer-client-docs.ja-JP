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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412542"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a><span data-ttu-id="8ad0c-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="8ad0c-103">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="8ad0c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ad0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ad0c-105">メッセージ クラスのグループをフォーム コンテナー内のフォームに解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-105">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="8ad0c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8ad0c-106">Parameters</span></span>

 <span data-ttu-id="8ad0c-107">_pMsgClassArray_</span><span class="sxs-lookup"><span data-stu-id="8ad0c-107">_pMsgClassArray_</span></span>
  
> <span data-ttu-id="8ad0c-108">[in]解決するメッセージ クラスの名前を含む配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span> <span data-ttu-id="8ad0c-109">メッセージ クラス名は常に ANSI 文字列で、Unicode は使用しません。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="8ad0c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8ad0c-110">_ulFlags_</span></span>
  
> <span data-ttu-id="8ad0c-111">[in]メッセージ クラスの解決方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-111">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="8ad0c-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-112">The following flag can be set:</span></span>
    
<span data-ttu-id="8ad0c-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="8ad0c-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="8ad0c-114">完全に一致するメッセージ クラスの文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="8ad0c-115">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="8ad0c-115">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="8ad0c-116">[out]フォーム情報オブジェクトの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-116">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="8ad0c-117">クライアント アプリケーションが  _pMsgClassArray_ パラメーターで NULL を渡した場合  _、ppfrminfoarray_ パラメーターには、コンテナー内のすべてのフォームのフォーム情報オブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-117">If a client application passes NULL in the  _pMsgClassArray_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8ad0c-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="8ad0c-118">Return value</span></span>

<span data-ttu-id="8ad0c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8ad0c-119">S_OK</span></span> 
  
> <span data-ttu-id="8ad0c-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="8ad0c-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8ad0c-121">注釈</span><span class="sxs-lookup"><span data-stu-id="8ad0c-121">Remarks</span></span>

<span data-ttu-id="8ad0c-122">クライアント アプリケーションは **IMAPIFormContainer::ResolveMultipleMessageClasses** メソッドを呼び出して、メッセージ クラスのグループをフォーム コンテナー内のフォームに解決します。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-122">Client applications call the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="8ad0c-123">_ppfrminfoarray_ パラメーターで返されるフォーム情報オブジェクトの配列は、フォームの各プロパティにさらにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-123">The array of form information objects returned in the  _ppfrminfoarray_ parameter provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8ad0c-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="8ad0c-124">Notes to callers</span></span>

<span data-ttu-id="8ad0c-125">メッセージ クラスのグループをフォームに解決するには、解決するメッセージ クラス名の配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-125">To resolve a group of message classes to forms, pass in an array of message class names to be resolved.</span></span> <span data-ttu-id="8ad0c-126">解決を厳密に (つまり、メッセージ クラスの基本クラスへの解決を防ぐため) には  _、ulFlags_ パラメーターに MAPIFORM_EXACTMATCH フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-126">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="8ad0c-127">メッセージ クラスをフォームに解決できない場合、フォーム情報配列内のそのメッセージ クラスに対して NULL が返されます。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-127">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="8ad0c-128">したがって、メソッドがメッセージ クラスを返S_OK、すべてのメッセージ クラスが正常に解決されたと見なす必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-128">Therefore, even if the method returns S_OK, do not assume that all message classes have been successfully resolved.</span></span> <span data-ttu-id="8ad0c-129">代わりに、返される配列の値を確認します。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-129">Instead, check the values in the returned array.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8ad0c-130">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="8ad0c-130">MFCMAPI reference</span></span>

<span data-ttu-id="8ad0c-131">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8ad0c-132">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="8ad0c-132">**File**</span></span>|<span data-ttu-id="8ad0c-133">**関数**</span><span class="sxs-lookup"><span data-stu-id="8ad0c-133">**Function**</span></span>|<span data-ttu-id="8ad0c-134">**コメント**</span><span class="sxs-lookup"><span data-stu-id="8ad0c-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8ad0c-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="8ad0c-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="8ad0c-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="8ad0c-136">CFormContainerDlg::OnResolveMultipleMessageClasses</span></span>  <br/> |<span data-ttu-id="8ad0c-137">MFCMAPI は **IMAPIFormContainer::ResolveMultipleMessageClasses** メソッドを使用して、一連のメッセージ クラスに関連付けられているフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="8ad0c-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ad0c-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="8ad0c-138">See also</span></span>



[<span data-ttu-id="8ad0c-139">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="8ad0c-139">IMAPIFormContainer::ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md)
  
[<span data-ttu-id="8ad0c-140">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8ad0c-140">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


<span data-ttu-id="8ad0c-141">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="8ad0c-141">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

