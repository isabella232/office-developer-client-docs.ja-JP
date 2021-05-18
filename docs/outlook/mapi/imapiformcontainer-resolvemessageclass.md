---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408552"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="a89c8-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="a89c8-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="a89c8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a89c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a89c8-105">メッセージ クラスをフォーム コンテナー内のフォームに解決し、そのフォームのフォーム情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="a89c8-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="a89c8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a89c8-106">Parameters</span></span>

 <span data-ttu-id="a89c8-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="a89c8-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="a89c8-108">[in]解決されるメッセージ クラスの名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="a89c8-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="a89c8-109">メッセージ クラス名は常に ANSI 文字列で、Unicode は使用しません。</span><span class="sxs-lookup"><span data-stu-id="a89c8-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="a89c8-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a89c8-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a89c8-111">[in]メッセージ クラスの解決方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a89c8-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="a89c8-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a89c8-112">The following flag can be set:</span></span>
    
<span data-ttu-id="a89c8-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="a89c8-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="a89c8-114">完全に一致するメッセージ クラスの文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a89c8-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="a89c8-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="a89c8-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="a89c8-116">[out]返されるフォーム情報オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a89c8-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a89c8-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="a89c8-117">Return value</span></span>

<span data-ttu-id="a89c8-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a89c8-118">S_OK</span></span> 
  
> <span data-ttu-id="a89c8-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a89c8-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a89c8-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a89c8-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a89c8-121">_szMessageClass_ パラメーターで渡されたメッセージ クラスは、フォーム コンテナー内のフォームのメッセージ クラスと一致しません。</span><span class="sxs-lookup"><span data-stu-id="a89c8-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a89c8-122">注釈</span><span class="sxs-lookup"><span data-stu-id="a89c8-122">Remarks</span></span>

<span data-ttu-id="a89c8-123">クライアント アプリケーションは **IMAPIFormContainer::ResolveMessageClass** メソッドを呼び出して、フォーム コンテナー内のフォームにメッセージ クラスを解決します。</span><span class="sxs-lookup"><span data-stu-id="a89c8-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="a89c8-124">_ppforminfo_ パラメーターで返されるフォーム情報オブジェクトは、指定されたメッセージ クラスを使用してフォームのプロパティにさらにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a89c8-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a89c8-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a89c8-125">Notes to callers</span></span>

<span data-ttu-id="a89c8-126">メッセージ クラスをフォームに解決するには、解決するメッセージ クラスの名前を渡します (たとえば  `IPM.HelpDesk.Software` )。</span><span class="sxs-lookup"><span data-stu-id="a89c8-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="a89c8-127">解決を厳密に (つまり、メッセージ クラスの基本クラスへの解決を防ぐため) には  _、ulFlags_ パラメーターに MAPIFORM_EXACTMATCH フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="a89c8-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="a89c8-128">解決されたメッセージ クラスのクラス識別子は、フォーム情報オブジェクトの一部として返されます。</span><span class="sxs-lookup"><span data-stu-id="a89c8-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="a89c8-129">[IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md)メソッドまたは[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)メソッドのいずれかを呼び出すまで、OLE ライブラリにクラス識別子が存在することを想定しません。</span><span class="sxs-lookup"><span data-stu-id="a89c8-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a89c8-130">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="a89c8-130">MFCMAPI reference</span></span>

<span data-ttu-id="a89c8-131">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a89c8-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a89c8-132">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="a89c8-132">**File**</span></span>|<span data-ttu-id="a89c8-133">**関数**</span><span class="sxs-lookup"><span data-stu-id="a89c8-133">**Function**</span></span>|<span data-ttu-id="a89c8-134">**コメント**</span><span class="sxs-lookup"><span data-stu-id="a89c8-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a89c8-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a89c8-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="a89c8-136">CFormContainerDlg::OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="a89c8-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="a89c8-137">MFCMAPI は **IMAPIFormContainer::ResolveMessageClass** メソッドを使用して、メッセージ クラスに関連付けられているフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="a89c8-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a89c8-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="a89c8-138">See also</span></span>



[<span data-ttu-id="a89c8-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a89c8-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="a89c8-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="a89c8-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="a89c8-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="a89c8-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="a89c8-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a89c8-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

