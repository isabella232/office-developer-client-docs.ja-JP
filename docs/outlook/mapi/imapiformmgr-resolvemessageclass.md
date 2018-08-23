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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a84698ccc132c750cbd071c05160117c40e352a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800587"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="ca249-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="ca249-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="ca249-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca249-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca249-105">フォームのコンテナー内のフォームにメッセージ クラスを解決し、そのフォームのフォームについてはオブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="ca249-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="ca249-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ca249-106">Parameters</span></span>

 <span data-ttu-id="ca249-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="ca249-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="ca249-108">[in]解決するメッセージ クラスの名前を示す文字列です。</span><span class="sxs-lookup"><span data-stu-id="ca249-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="ca249-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ca249-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ca249-110">[in]メッセージ クラスが解決される方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ca249-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="ca249-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ca249-111">The following flag can be set:</span></span>
    
<span data-ttu-id="ca249-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="ca249-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="ca249-113">完全に一致するメッセージ クラス文字列のみを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca249-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="ca249-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="ca249-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="ca249-115">[in]解決されているメッセージを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ca249-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="ca249-116">_PFolderFocus_パラメーターは NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="ca249-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="ca249-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="ca249-117">_ppResult_</span></span>
  
> <span data-ttu-id="ca249-118">[out]返されたフォームの情報オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ca249-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca249-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ca249-119">Return value</span></span>

<span data-ttu-id="ca249-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca249-120">S_OK</span></span> 
  
> <span data-ttu-id="ca249-121">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="ca249-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ca249-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ca249-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ca249-123">_SzMsgClass_パラメーターで渡されたメッセージ クラスでは、フォーム ライブラリ内の任意のフォームのメッセージ クラスが一致しません。</span><span class="sxs-lookup"><span data-stu-id="ca249-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ca249-124">注釈</span><span class="sxs-lookup"><span data-stu-id="ca249-124">Remarks</span></span>

<span data-ttu-id="ca249-125">フォームの閲覧者は、フォームのコンテナー内のフォームにメッセージ クラスを解決するのには**IMAPIFormMgr::ResolveMessageClass**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ca249-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="ca249-126">_PpResult_パラメーターに返されるフォームの情報オブジェクトを特定のメッセージ クラスを含むフォームのプロパティへのアクセスをさらに提供します。</span><span class="sxs-lookup"><span data-stu-id="ca249-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ca249-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ca249-127">Notes to callers</span></span>

<span data-ttu-id="ca249-128">フォームにメッセージ クラスを解決する、フォーム ビューアーを渡すように、解決するメッセージ クラスの名前" `IPM.HelpDesk.Software`"です。</span><span class="sxs-lookup"><span data-stu-id="ca249-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="ca249-129">正確な解像度を強制する (つまりと正確に一致する、フォーム、のメッセージ クラスの基本クラスの解像度を防止するためにサーバーは使用できません)、 _ulFlags_パラメーターでは、MAPIFORM_EXACTMATCH フラグを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="ca249-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="ca249-130">_PFolderFocus_パラメーターが NULL の場合は、メッセージのクラスの解決プロセスは、フォルダー コンテナーを検索しません。</span><span class="sxs-lookup"><span data-stu-id="ca249-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="ca249-131">検索コンテナーの順序は、フォーム ライブラリのプロバイダーの実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="ca249-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="ca249-132">既定のフォーム ライブラリのプロバイダーは、ローカルのコンテナーでは、[フォルダーのコンテナー、渡されたフォルダー、個人用フォームのコンテナーと、最後に、[組織] コンテナーを最初に検索します。</span><span class="sxs-lookup"><span data-stu-id="ca249-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="ca249-133">メッセージ クラス名は、常に ANSI 文字列を Unicode ではないです。</span><span class="sxs-lookup"><span data-stu-id="ca249-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="ca249-134">フォームの情報オブジェクトの一部として解決済みのメッセージ クラスのクラス識別子が返されます。</span><span class="sxs-lookup"><span data-stu-id="ca249-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="ca249-135">フォーム ビューアー フォーム ビューアーは、 [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)メソッドまたは[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)メソッドが呼び出されるとするまで、OLE ライブラリのクラス識別子が存在することを前提として動作していません。</span><span class="sxs-lookup"><span data-stu-id="ca249-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca249-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="ca249-136">See also</span></span>



[<span data-ttu-id="ca249-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ca249-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="ca249-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="ca249-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="ca249-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="ca249-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="ca249-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca249-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

