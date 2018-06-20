---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: dcde242f5f2e956d1926d6914431008383f5aa55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800686"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="6c8e4-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="6c8e4-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="6c8e4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6c8e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6c8e4-105">さらにアクセスするための[IAddrBook](iaddrbookimapiprop.md)ポインターを返す MAPI 統合アドレス帳を開きます。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="6c8e4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6c8e4-106">Parameters</span></span>

 <span data-ttu-id="6c8e4-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6c8e4-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="6c8e4-108">[in]表示に関連して、共通のアドレス] ダイアログ ボックスおよびその他の親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="6c8e4-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6c8e4-109">_lpInterface_</span></span>
  
> <span data-ttu-id="6c8e4-110">[in]アドレス帳にアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="6c8e4-111">アドレス帳の標準的なインターフェイスへのポインターを返します**null**を渡す[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="6c8e4-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c8e4-112">_ulFlags_</span></span>
  
> <span data-ttu-id="6c8e4-113">[in]アドレス帳の開始を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="6c8e4-114">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-114">The following flag can be set:</span></span>
    
<span data-ttu-id="6c8e4-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6c8e4-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="6c8e4-116">ダイアログ ボックスの表示を抑制します。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="6c8e4-117">AB_NO_DIALOG フラグが設定されていない場合内蔵のアドレス帳に寄与するアドレス帳プロバイダーで必要な情報がないユーザーに確認することができます。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="6c8e4-118">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="6c8e4-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="6c8e4-119">[out]アドレス帳へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c8e4-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6c8e4-120">Return value</span></span>

<span data-ttu-id="6c8e4-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c8e4-121">S_OK</span></span> 
  
> <span data-ttu-id="6c8e4-122">アドレス帳が正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="6c8e4-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="6c8e4-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="6c8e4-124">呼び出しが成功したが、1 つまたは複数のアドレス帳プロバイダーのコンテナーを開くことができませんでした。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="6c8e4-125">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="6c8e4-126">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="6c8e4-127">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c8e4-128">備考</span><span class="sxs-lookup"><span data-stu-id="6c8e4-128">Remarks</span></span>

<span data-ttu-id="6c8e4-129">**IMAPISession::OpenAddressBook**メソッドでは、MAPI の統合のアドレス帳をプロファイル内のアドレス帳プロバイダーのすべての最上位のコンテナーのコレクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="6c8e4-130">_LppAdrBook_パラメーターで返されるポインターをアドレス帳の内容へのアクセスをさらに提供します。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="6c8e4-131">これにより、個々 のコンテナーを開き、メッセージング ユーザーの検索、および共通のアドレス] ダイアログ ボックスを表示するなどのタスクを実行する呼び出し元です。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6c8e4-132">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="6c8e4-132">Notes to callers</span></span>

 <span data-ttu-id="6c8e4-133">**OpenAddressBook**は、1 つまたは複数のプロファイルで、アドレス帳プロバイダーをロードすることがある場合に MAPI_W_ERRORS_RETURNED を返します。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="6c8e4-134">この値は、警告が表示されないエラーの値です。S_OK の場合と同様に処理します。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="6c8e4-135">**OpenAddressBook**は、常に読み込みに失敗をアドレス帳プロバイダーの数に関係なく、 _lppAdrBook_パラメーターに有効なポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="6c8e4-136">そのため、常にメソッドを呼び出してください、アドレス帳[が](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)ある時点でログオフする前にします。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-136">Therefore, you must always call the address book's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="6c8e4-137">**OpenAddressBook**に MAPI_W_ERRORS_RETURNED が返されるときは、障害のあるプロバイダーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を取得するのには[IMAPISession::GetLastError](imapisession-getlasterror.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="6c8e4-138">すべてのプロバイダーから提供された情報が含まれる 1 つの**MAPIERROR**構造体が返されます。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6c8e4-139">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="6c8e4-139">MFCMAPI reference</span></span>

<span data-ttu-id="6c8e4-140">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="6c8e4-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6c8e4-141">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="6c8e4-141">**File**</span></span>|<span data-ttu-id="6c8e4-142">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="6c8e4-142">**Function**</span></span>|<span data-ttu-id="6c8e4-143">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="6c8e4-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6c8e4-144">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="6c8e4-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="6c8e4-145">CMapiObjects::GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="6c8e4-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="6c8e4-146">MFCMAPI では、 **IMAPISession::OpenAddressBook**メソッドを使用して、内蔵のアドレス帳を取得します。</span><span class="sxs-lookup"><span data-stu-id="6c8e4-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c8e4-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c8e4-147">See also</span></span>



[<span data-ttu-id="6c8e4-148">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6c8e4-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="6c8e4-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6c8e4-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="6c8e4-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="6c8e4-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="6c8e4-151">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c8e4-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="6c8e4-152">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="6c8e4-152">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

