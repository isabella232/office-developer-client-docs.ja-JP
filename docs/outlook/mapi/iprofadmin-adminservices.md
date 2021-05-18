---
title: IProfAdminAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422083"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="47ac9-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="47ac9-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="47ac9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47ac9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47ac9-105">プロファイル内のメッセージ サービスに変更を加えるメッセージ サービス管理オブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="47ac9-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="47ac9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="47ac9-106">Parameters</span></span>

 <span data-ttu-id="47ac9-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="47ac9-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="47ac9-108">[in]変更するプロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="47ac9-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="47ac9-109">_lpszProfileName パラメーター_ は NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="47ac9-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="47ac9-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="47ac9-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="47ac9-111">[in]常に NULL。</span><span class="sxs-lookup"><span data-stu-id="47ac9-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="47ac9-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="47ac9-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="47ac9-113">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウのハンドル。</span><span class="sxs-lookup"><span data-stu-id="47ac9-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="47ac9-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="47ac9-114">_ulFlags_</span></span>
  
> <span data-ttu-id="47ac9-115">[in]メッセージ サービス管理オブジェクトの取得を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="47ac9-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="47ac9-116">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="47ac9-116">The following flags can be set:</span></span>
    
<span data-ttu-id="47ac9-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="47ac9-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="47ac9-118">ユーザー インターフェイスの表示を有効にします。</span><span class="sxs-lookup"><span data-stu-id="47ac9-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="47ac9-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="47ac9-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="47ac9-120">プロファイル名は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="47ac9-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="47ac9-121">このフラグMAPI_UNICODE設定されていない場合、名前は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="47ac9-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="47ac9-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="47ac9-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="47ac9-123">[out]メッセージ サービス管理オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="47ac9-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47ac9-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="47ac9-124">Return value</span></span>

<span data-ttu-id="47ac9-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="47ac9-125">S_OK</span></span> 
  
> <span data-ttu-id="47ac9-126">メッセージ サービス管理オブジェクトが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="47ac9-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="47ac9-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="47ac9-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="47ac9-128">指定されたプロファイルが存在しないか、パスワードが間違っていたため、MAPI_DIALOG が  _ulFlags_ で設定されていないので、正しいパスワードを要求するダイアログ ボックスをユーザーに表示できません。</span><span class="sxs-lookup"><span data-stu-id="47ac9-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="47ac9-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="47ac9-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="47ac9-130">通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="47ac9-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="47ac9-131">注釈</span><span class="sxs-lookup"><span data-stu-id="47ac9-131">Remarks</span></span>

<span data-ttu-id="47ac9-132">**IProfAdmin::AdminServices** メソッドは、プロファイル内のメッセージ サービスに構成変更を加えるメッセージ サービス管理オブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="47ac9-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="47ac9-133">_lpszPassword パラメーター_ は NULL または長さ 0 の文字列へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="47ac9-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="47ac9-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="47ac9-134">Notes to callers</span></span>

<span data-ttu-id="47ac9-135">このメソッドまたは [IMAPISession::AdminServices](imapisession-adminservices.md)を呼び出すことによって [IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターを取得することができますが、厳密に構成クライアントを持ち、メッセージング機能を提供しない場合は **、IProfAdmin::AdminServices** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="47ac9-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="47ac9-136">**IProfAdmin::AdminServices** はセッション オブジェクトを作成し、サービス プロバイダーを読み込み、パフォーマンスを向上させます。</span><span class="sxs-lookup"><span data-stu-id="47ac9-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="47ac9-137">**IProfAdmin::AdminServices を使用してプロファイル** を作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="47ac9-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="47ac9-138">したがって、lpszProfileName で既存の有効な  _プロファイルを指定する必要があります_。</span><span class="sxs-lookup"><span data-stu-id="47ac9-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="47ac9-139">指定したプロファイルが存在しない場合 **、IProfAdmin::AdminServices** は、このMAPI_E_LOGON_FAILED。</span><span class="sxs-lookup"><span data-stu-id="47ac9-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="47ac9-140">プロファイルの名前の長さは最大 64 文字で、次の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="47ac9-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="47ac9-141">アクセント文字とアンダースコア文字を含むすべての英数字。</span><span class="sxs-lookup"><span data-stu-id="47ac9-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="47ac9-142">埋め込みスペースですが、先頭または末尾のスペースは使用できません。</span><span class="sxs-lookup"><span data-stu-id="47ac9-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="47ac9-143">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="47ac9-143">MFCMAPI reference</span></span>

<span data-ttu-id="47ac9-144">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47ac9-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="47ac9-145">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="47ac9-145">**File**</span></span>|<span data-ttu-id="47ac9-146">**関数**</span><span class="sxs-lookup"><span data-stu-id="47ac9-146">**Function**</span></span>|<span data-ttu-id="47ac9-147">**コメント**</span><span class="sxs-lookup"><span data-stu-id="47ac9-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="47ac9-148">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="47ac9-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="47ac9-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="47ac9-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="47ac9-150">MFCMAPI は **、IProfAdmin::AdminServices** メソッドを使用して、選択したプロファイルのメッセージ サービス管理オブジェクトを開き、サービスを追加します。</span><span class="sxs-lookup"><span data-stu-id="47ac9-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47ac9-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="47ac9-151">See also</span></span>



[<span data-ttu-id="47ac9-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="47ac9-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="47ac9-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47ac9-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


<span data-ttu-id="47ac9-154">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="47ac9-154">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

