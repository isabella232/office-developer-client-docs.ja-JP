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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: db4b8d99c960deb3de3d228b2bf9549738501bcc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576282"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="37bcd-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="37bcd-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="37bcd-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37bcd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37bcd-105">フォームのコンテナー内のフォームにメッセージ クラスを解決し、そのフォームのフォームについてはオブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="37bcd-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="37bcd-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37bcd-106">Parameters</span></span>

 <span data-ttu-id="37bcd-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="37bcd-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="37bcd-108">[in]解決するメッセージ クラスの名前を示す文字列です。</span><span class="sxs-lookup"><span data-stu-id="37bcd-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="37bcd-109">メッセージ クラス名は、常に ANSI 文字列を Unicode ではないです。</span><span class="sxs-lookup"><span data-stu-id="37bcd-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="37bcd-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="37bcd-110">_ulFlags_</span></span>
  
> <span data-ttu-id="37bcd-111">[in]メッセージ クラスが解決される方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="37bcd-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="37bcd-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="37bcd-112">The following flag can be set:</span></span>
    
<span data-ttu-id="37bcd-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="37bcd-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="37bcd-114">完全に一致するメッセージ クラス文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37bcd-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="37bcd-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="37bcd-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="37bcd-116">[out]返されたフォームの情報オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="37bcd-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37bcd-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="37bcd-117">Return value</span></span>

<span data-ttu-id="37bcd-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="37bcd-118">S_OK</span></span> 
  
> <span data-ttu-id="37bcd-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="37bcd-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="37bcd-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="37bcd-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="37bcd-121">_SzMessageClass_パラメーターで渡されたメッセージ クラスでは、フォームのコンテナー内の任意のフォームのメッセージ クラスが一致しません。</span><span class="sxs-lookup"><span data-stu-id="37bcd-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="37bcd-122">注釈</span><span class="sxs-lookup"><span data-stu-id="37bcd-122">Remarks</span></span>

<span data-ttu-id="37bcd-123">クライアント アプリケーションは、フォームのコンテナー内のフォームにメッセージ クラスを解決するのには**IMAPIFormContainer::ResolveMessageClass**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="37bcd-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="37bcd-124">_Ppforminfo_パラメーターに返されるフォームの情報オブジェクトを特定のメッセージ クラスのフォームのプロパティへのアクセスをさらに提供します。</span><span class="sxs-lookup"><span data-stu-id="37bcd-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="37bcd-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="37bcd-125">Notes to callers</span></span>

<span data-ttu-id="37bcd-126">解決するメッセージ クラスの名前を渡すフォームにメッセージ クラスを解決するのには (たとえば、 `IPM.HelpDesk.Software`)。</span><span class="sxs-lookup"><span data-stu-id="37bcd-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="37bcd-127">正確な解像度を強制的に (つまり、メッセージ クラスの基本クラスへの解像度を防ぐために)、 _ulFlags_パラメーターでは、MAPIFORM_EXACTMATCH フラグを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="37bcd-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="37bcd-128">フォームの情報オブジェクトの一部として解決済みのメッセージ クラスのクラス識別子が返されます。</span><span class="sxs-lookup"><span data-stu-id="37bcd-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="37bcd-129">[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)または[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)のいずれかのメソッドを呼び出すまで、OLE ライブラリのクラス識別子が存在するとは限りません。</span><span class="sxs-lookup"><span data-stu-id="37bcd-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="37bcd-130">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="37bcd-130">MFCMAPI reference</span></span>

<span data-ttu-id="37bcd-131">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="37bcd-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="37bcd-132">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="37bcd-132">**File**</span></span>|<span data-ttu-id="37bcd-133">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="37bcd-133">**Function**</span></span>|<span data-ttu-id="37bcd-134">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="37bcd-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="37bcd-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="37bcd-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="37bcd-136">CFormContainerDlg::OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="37bcd-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="37bcd-137">MFCMAPI では、 **IMAPIFormContainer::ResolveMessageClass**メソッドを使用して、メッセージ クラスに関連付けられているフォームを見つけます。</span><span class="sxs-lookup"><span data-stu-id="37bcd-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37bcd-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="37bcd-138">See also</span></span>



[<span data-ttu-id="37bcd-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="37bcd-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="37bcd-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="37bcd-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="37bcd-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="37bcd-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="37bcd-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="37bcd-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

