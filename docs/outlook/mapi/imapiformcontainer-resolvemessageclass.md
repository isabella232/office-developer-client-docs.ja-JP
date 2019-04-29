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
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="b7374-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="b7374-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="b7374-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7374-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7374-105">メッセージクラスをフォームコンテナー内のフォームに解決し、そのフォームのフォーム情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="b7374-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="b7374-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b7374-106">Parameters</span></span>

 <span data-ttu-id="b7374-107">_szmessageclass_</span><span class="sxs-lookup"><span data-stu-id="b7374-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="b7374-108">順番解決されるメッセージクラスの名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="b7374-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="b7374-109">メッセージクラス名は常に ANSI 文字列で、Unicode はありません。</span><span class="sxs-lookup"><span data-stu-id="b7374-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="b7374-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b7374-110">_ulFlags_</span></span>
  
> <span data-ttu-id="b7374-111">順番メッセージクラスの解決方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="b7374-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="b7374-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b7374-112">The following flag can be set:</span></span>
    
<span data-ttu-id="b7374-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="b7374-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="b7374-114">完全一致のメッセージクラス文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7374-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="b7374-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="b7374-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="b7374-116">読み上げ返されるフォーム情報オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b7374-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b7374-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="b7374-117">Return value</span></span>

<span data-ttu-id="b7374-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7374-118">S_OK</span></span> 
  
> <span data-ttu-id="b7374-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b7374-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b7374-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b7374-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b7374-121">_szmessageclass_パラメーターで渡されたメッセージクラスが、フォームコンテナー内のフォームのメッセージクラスと一致しません。</span><span class="sxs-lookup"><span data-stu-id="b7374-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b7374-122">注釈</span><span class="sxs-lookup"><span data-stu-id="b7374-122">Remarks</span></span>

<span data-ttu-id="b7374-123">クライアントアプリケーションは、 **imapiformcontainer:: ResolveMessageClass**メソッドを呼び出して、form コンテナー内のフォームにメッセージクラスを解決します。</span><span class="sxs-lookup"><span data-stu-id="b7374-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="b7374-124">_ppforminfo_パラメーターで返されたフォーム情報オブジェクトは、指定されたメッセージクラスを使用して、フォームのプロパティにさらにアクセスできるようにします。</span><span class="sxs-lookup"><span data-stu-id="b7374-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b7374-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b7374-125">Notes to callers</span></span>

<span data-ttu-id="b7374-126">メッセージクラスをフォームに解決するには、解決するメッセージクラスの名前を渡します (例: `IPM.HelpDesk.Software`)。</span><span class="sxs-lookup"><span data-stu-id="b7374-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="b7374-127">解決策を正確にする (つまり、メッセージクラスの基本クラスに解決されないようにする) には、 _ulflags_パラメーターに MAPIFORM_EXACTMATCH フラグを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="b7374-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="b7374-128">解決されたメッセージクラスのクラス識別子は、フォーム情報オブジェクトの一部として返されます。</span><span class="sxs-lookup"><span data-stu-id="b7374-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="b7374-129">[imapiformmgr::P repareform](imapiformmgr-prepareform.md)または[imapiformmgr:: CreateForm](imapiformmgr-createform.md)メソッドのいずれかを呼び出すまで、クラス識別子が OLE ライブラリに存在することを前提としていません。</span><span class="sxs-lookup"><span data-stu-id="b7374-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b7374-130">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="b7374-130">MFCMAPI reference</span></span>

<span data-ttu-id="b7374-131">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7374-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b7374-132">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="b7374-132">**File**</span></span>|<span data-ttu-id="b7374-133">**関数**</span><span class="sxs-lookup"><span data-stu-id="b7374-133">**Function**</span></span>|<span data-ttu-id="b7374-134">**コメント**</span><span class="sxs-lookup"><span data-stu-id="b7374-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b7374-135">FormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="b7374-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="b7374-136">CFormContainerDlg:: OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="b7374-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="b7374-137">mfcmapi は、 **imapiformcontainer:: ResolveMessageClass**メソッドを使用して、メッセージクラスに関連付けられているフォームを特定します。</span><span class="sxs-lookup"><span data-stu-id="b7374-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7374-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7374-138">See also</span></span>



[<span data-ttu-id="b7374-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b7374-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="b7374-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="b7374-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="b7374-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="b7374-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="b7374-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7374-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

