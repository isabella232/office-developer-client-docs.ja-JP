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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329422"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="a06d0-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="a06d0-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="a06d0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a06d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a06d0-105">MAPI 統合アドレス帳を開き、さらにアクセスするために[IAddrBook](iaddrbookimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="a06d0-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="a06d0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a06d0-106">Parameters</span></span>

 <span data-ttu-id="a06d0-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="a06d0-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a06d0-108">順番[共通アドレス] ダイアログボックスとその他の関連する表示の親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="a06d0-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="a06d0-109">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="a06d0-109">_lpInterface_</span></span>
  
> <span data-ttu-id="a06d0-110">順番アドレス帳へのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a06d0-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="a06d0-111">**null**を渡すと、アドレス帳の標準インターフェイス[IAddrBook: imapiprop](iaddrbookimapiprop.md)へのポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="a06d0-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="a06d0-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a06d0-112">_ulFlags_</span></span>
  
> <span data-ttu-id="a06d0-113">順番アドレス帳を開くかどうかを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a06d0-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="a06d0-114">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a06d0-114">The following flag can be set:</span></span>
    
<span data-ttu-id="a06d0-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a06d0-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="a06d0-116">ダイアログボックスの表示を抑制します。</span><span class="sxs-lookup"><span data-stu-id="a06d0-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="a06d0-117">AB_NO_DIALOG フラグが設定されていない場合、統合アドレス帳に投稿されるアドレス帳プロバイダーは、必要な情報の入力をユーザーに求めることができます。</span><span class="sxs-lookup"><span data-stu-id="a06d0-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="a06d0-118">_lppadrbook_</span><span class="sxs-lookup"><span data-stu-id="a06d0-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="a06d0-119">読み上げアドレス帳へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a06d0-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a06d0-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="a06d0-120">Return value</span></span>

<span data-ttu-id="a06d0-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="a06d0-121">S_OK</span></span> 
  
> <span data-ttu-id="a06d0-122">アドレス帳が正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="a06d0-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="a06d0-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="a06d0-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="a06d0-124">呼び出しは成功しましたが、1つ以上のアドレス帳プロバイダーのコンテナーを開くことができませんでした。</span><span class="sxs-lookup"><span data-stu-id="a06d0-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="a06d0-125">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="a06d0-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a06d0-126">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="a06d0-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a06d0-127">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a06d0-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a06d0-128">解説</span><span class="sxs-lookup"><span data-stu-id="a06d0-128">Remarks</span></span>

<span data-ttu-id="a06d0-129">**imapisession:: OpenAddressBook**メソッドを実行すると、MAPI 統合アドレス帳 (プロファイル内のすべてのアドレス帳プロバイダーのトップレベルコンテナーのコレクション) が開きます。</span><span class="sxs-lookup"><span data-stu-id="a06d0-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="a06d0-130">_lppadrbook_パラメーターで返されるポインターは、アドレス帳の内容へのアクセスをさらに提供します。</span><span class="sxs-lookup"><span data-stu-id="a06d0-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="a06d0-131">これにより、発信者は、個々のコンテナーを開いたり、メッセージングユーザーを検索したり、共通のアドレスダイアログボックスを表示したりするなどのタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="a06d0-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a06d0-132">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a06d0-132">Notes to callers</span></span>

 <span data-ttu-id="a06d0-133">**OpenAddressBook**は、プロファイルにアドレス帳プロバイダーを1つ以上読み込むことができない場合、MAPI_W_ERRORS_RETURNED を返します。</span><span class="sxs-lookup"><span data-stu-id="a06d0-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="a06d0-134">この値は、エラー値ではなく警告です。これを S_OK として処理します。</span><span class="sxs-lookup"><span data-stu-id="a06d0-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="a06d0-135">**OpenAddressBook**は、いくつかのアドレス帳プロバイダーの読み込みに失敗したとしても、 _lppadrbook_パラメーターには常に有効なポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="a06d0-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="a06d0-136">そのため、ログオフする前に、いつでもアドレス帳の[IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a06d0-136">Therefore, you must always call the address book's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="a06d0-137">**OpenAddressBook**が MAPI_W_ERRORS_RETURNED を返す場合は、 [imapisession:: GetLastError](imapisession-getlasterror.md)を呼び出して、エラーが発生しているプロバイダーに関する情報を含む[MAPIERROR](mapierror.md)構造を取得します。</span><span class="sxs-lookup"><span data-stu-id="a06d0-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="a06d0-138">すべてのプロバイダーによって提供される情報を含む単一の**MAPIERROR**構造体が返されます。</span><span class="sxs-lookup"><span data-stu-id="a06d0-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a06d0-139">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="a06d0-139">MFCMAPI reference</span></span>

<span data-ttu-id="a06d0-140">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a06d0-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a06d0-141">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="a06d0-141">**File**</span></span>|<span data-ttu-id="a06d0-142">**関数**</span><span class="sxs-lookup"><span data-stu-id="a06d0-142">**Function**</span></span>|<span data-ttu-id="a06d0-143">**コメント**</span><span class="sxs-lookup"><span data-stu-id="a06d0-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a06d0-144">MAPIObjects</span><span class="sxs-lookup"><span data-stu-id="a06d0-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="a06d0-145">cmapiobjects:: GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="a06d0-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="a06d0-146">mfcmapi は、 **imapisession:: OpenAddressBook**メソッドを使用して、統合されたアドレス帳を取得します。</span><span class="sxs-lookup"><span data-stu-id="a06d0-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a06d0-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="a06d0-147">See also</span></span>



[<span data-ttu-id="a06d0-148">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a06d0-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="a06d0-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a06d0-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="a06d0-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="a06d0-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="a06d0-151">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a06d0-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="a06d0-152">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="a06d0-152">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

