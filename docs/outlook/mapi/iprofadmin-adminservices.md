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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309598"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="2ea6e-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="2ea6e-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="2ea6e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ea6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ea6e-105">プロファイル内のメッセージサービスに変更を加えるためのメッセージサービス管理オブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="2ea6e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2ea6e-106">Parameters</span></span>

 <span data-ttu-id="2ea6e-107">_lpszprofilename_</span><span class="sxs-lookup"><span data-stu-id="2ea6e-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="2ea6e-108">順番変更するプロファイルの名前へのポインターを指定します。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="2ea6e-109">_lpszprofilename_パラメーターを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="2ea6e-110">_lpszpassword_</span><span class="sxs-lookup"><span data-stu-id="2ea6e-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="2ea6e-111">順番常に NULL。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="2ea6e-112">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="2ea6e-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="2ea6e-113">順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウのハンドル。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="2ea6e-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2ea6e-114">_ulFlags_</span></span>
  
> <span data-ttu-id="2ea6e-115">順番メッセージサービス管理オブジェクトの取得を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="2ea6e-116">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-116">The following flags can be set:</span></span>
    
<span data-ttu-id="2ea6e-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2ea6e-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="2ea6e-118">ユーザーインターフェイスの表示を有効にします。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="2ea6e-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2ea6e-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2ea6e-120">プロファイル名が Unicode 形式である。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="2ea6e-121">MAPI_UNICODE フラグが設定されていない場合、名前は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="2ea6e-122">_lppserviceadmin_</span><span class="sxs-lookup"><span data-stu-id="2ea6e-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="2ea6e-123">読み上げメッセージサービス管理オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2ea6e-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="2ea6e-124">Return value</span></span>

<span data-ttu-id="2ea6e-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ea6e-125">S_OK</span></span> 
  
> <span data-ttu-id="2ea6e-126">メッセージサービス管理オブジェクトが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="2ea6e-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="2ea6e-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="2ea6e-128">指定されたプロファイルが存在しないか、またはパスワードが正しくないため、ユーザーに正しいパスワードを要求するためにダイアログボックスを表示できませんでした。 MAPI_DIALOG が_ulflags_で設定されていませんでした。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="2ea6e-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="2ea6e-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="2ea6e-130">ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2ea6e-131">解説</span><span class="sxs-lookup"><span data-stu-id="2ea6e-131">Remarks</span></span>

<span data-ttu-id="2ea6e-132">**IProfAdmin:: adminservices**メソッドは、プロファイル内のメッセージサービスに対する構成変更を行うためのメッセージサービス管理オブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="2ea6e-133">_lpszpassword_パラメーターは、NULL または長さ0の文字列へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2ea6e-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2ea6e-134">Notes to callers</span></span>

<span data-ttu-id="2ea6e-135">[IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターは、このメソッドまたは[imapisession:: adminservices](imapisession-adminservices.md)のいずれかを呼び出すことによって取得できますが、厳密に構成クライアントがあり、メッセージング機能を提供していない場合は、 **IProfAdmin:: adminservices**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="2ea6e-136">**IProfAdmin:: adminservices**では、セッションオブジェクトは作成されず、サービスプロバイダーは読み込まれません。これにより、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="2ea6e-137">**IProfAdmin:: adminservices**を使用してプロファイルを作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="2ea6e-138">そのため、 _lpszprofilename_に既存の有効なプロファイルを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="2ea6e-139">指定したプロファイルが存在しない場合、 **IProfAdmin:: adminservices**は MAPI_E_LOGON_FAILED を返します。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="2ea6e-140">プロファイルの名前は最大64文字の長さにすることができ、次の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="2ea6e-141">アクセント記号とアンダースコア文字を含むすべての英数字。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="2ea6e-142">スペースは埋め込まれますが、先頭または末尾にスペースは含まれません。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="2ea6e-143">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="2ea6e-143">MFCMAPI reference</span></span>

<span data-ttu-id="2ea6e-144">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2ea6e-145">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="2ea6e-145">**File**</span></span>|<span data-ttu-id="2ea6e-146">**関数**</span><span class="sxs-lookup"><span data-stu-id="2ea6e-146">**Function**</span></span>|<span data-ttu-id="2ea6e-147">**コメント**</span><span class="sxs-lookup"><span data-stu-id="2ea6e-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2ea6e-148">MAPIProfileFunctions</span><span class="sxs-lookup"><span data-stu-id="2ea6e-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="2ea6e-149">hraddservicetoprofile</span><span class="sxs-lookup"><span data-stu-id="2ea6e-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="2ea6e-150">mfcmapi は、 **IProfAdmin:: adminservices**メソッドを使用して、選択されたプロファイルのメッセージサービス管理オブジェクトを開き、サービスを追加します。</span><span class="sxs-lookup"><span data-stu-id="2ea6e-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ea6e-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ea6e-151">See also</span></span>



[<span data-ttu-id="2ea6e-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="2ea6e-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="2ea6e-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ea6e-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


<span data-ttu-id="2ea6e-154">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2ea6e-154">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

