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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7566bb075c2ef9903b5a376fd90f209c8683c31e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801134"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="f1dc1-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="f1dc1-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="f1dc1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f1dc1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f1dc1-105">プロファイル内のメッセージ サービスを変更する場合、メッセージ サービスの管理オブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="f1dc1-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f1dc1-106">Parameters</span></span>

 <span data-ttu-id="f1dc1-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="f1dc1-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="f1dc1-108">[in]変更するプロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="f1dc1-109">_LpszProfileName_パラメーターを NULL にする必要がありますはできません。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="f1dc1-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="f1dc1-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="f1dc1-111">[in]常に NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="f1dc1-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f1dc1-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="f1dc1-113">[in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="f1dc1-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f1dc1-114">_ulFlags_</span></span>
  
> <span data-ttu-id="f1dc1-115">[in]メッセージ サービスの管理オブジェクトの検索を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="f1dc1-116">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-116">The following flags can be set:</span></span>
    
<span data-ttu-id="f1dc1-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f1dc1-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="f1dc1-118">ユーザー インターフェイスの表示を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="f1dc1-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f1dc1-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f1dc1-120">プロファイル名は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="f1dc1-121">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の名前です。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="f1dc1-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="f1dc1-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="f1dc1-123">[out]メッセージ サービス管理オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f1dc1-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f1dc1-124">Return value</span></span>

<span data-ttu-id="f1dc1-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1dc1-125">S_OK</span></span> 
  
> <span data-ttu-id="f1dc1-126">メッセージ サービスの管理オブジェクトが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="f1dc1-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="f1dc1-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="f1dc1-128">指定されたプロファイルが存在しないまたはパスワードが間違っていたし、 _ulFlags_で MAPI_DIALOG が設定されていないために、正しいパスワードを要求するユーザーに、ダイアログ ボックスを表示できませんでした。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="f1dc1-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="f1dc1-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="f1dc1-130">ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f1dc1-131">備考</span><span class="sxs-lookup"><span data-stu-id="f1dc1-131">Remarks</span></span>

<span data-ttu-id="f1dc1-132">**IProfAdmin::AdminServices**メソッドは、プロファイル内のメッセージ サービスの構成を変更のメッセージ サービスの管理オブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="f1dc1-133">_LpszPassword_パラメーターは、NULL または長さ 0 の文字列へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f1dc1-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f1dc1-134">Notes to callers</span></span>

<span data-ttu-id="f1dc1-135">[IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターを取得するには、このメソッドまたは[IMAPISession::AdminServices](imapisession-adminservices.md)のいずれか、ですが、厳密に構成のクライアントがあり、メッセージング機能を提供していない場合**IProfAdmin::AdminServices**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="f1dc1-136">**IProfAdmin::AdminServices**では、セッション オブジェクトを作成できませんし、読み込まれないすべてのサービス プロバイダーでは、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="f1dc1-137">**IProfAdmin::AdminServices**を使用して、プロファイルを作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="f1dc1-138">したがって、 _lpszProfileName_では、既存の有効なプロファイルを指定してください。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="f1dc1-139">指定されたプロファイルが存在しない場合、 **IProfAdmin::AdminServices**は MAPI_E_LOGON_FAILED を返します。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="f1dc1-140">プロファイルの名前は 64 文字までの長さにすることができ、次の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="f1dc1-141">すべての英数字文字、アクセント記号付き文字およびアンダー スコア文字を含みます。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="f1dc1-142">埋め込みスペースがいない先頭または末尾のスペース。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="f1dc1-143">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="f1dc1-143">MFCMAPI reference</span></span>

<span data-ttu-id="f1dc1-144">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="f1dc1-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f1dc1-145">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="f1dc1-145">**File**</span></span>|<span data-ttu-id="f1dc1-146">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="f1dc1-146">**Function**</span></span>|<span data-ttu-id="f1dc1-147">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="f1dc1-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f1dc1-148">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="f1dc1-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="f1dc1-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="f1dc1-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="f1dc1-150">MFCMAPI では、 **IProfAdmin::AdminServices**メソッドを使用して、サービスを追加するのには選択したプロファイルのメッセージ サービスの管理オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="f1dc1-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1dc1-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1dc1-151">See also</span></span>



[<span data-ttu-id="f1dc1-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="f1dc1-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="f1dc1-153">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f1dc1-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


<span data-ttu-id="f1dc1-154">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="f1dc1-154">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

