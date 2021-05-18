---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b104c62eb617e6c68f85dea4ef6379c831733844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404401"
---
# <a name="iprofadmincreateprofile"></a><span data-ttu-id="0f5c3-103">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="0f5c3-103">IProfAdmin::CreateProfile</span></span>

  
  
<span data-ttu-id="0f5c3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f5c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f5c3-105">新しいプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-105">Creates a new profile.</span></span>
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0f5c3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f5c3-106">Parameters</span></span>

 <span data-ttu-id="0f5c3-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="0f5c3-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="0f5c3-108">[in]新しいプロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-108">[in] A pointer to the name of the new profile.</span></span>
    
 <span data-ttu-id="0f5c3-109">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="0f5c3-109">_lpszPassword_</span></span>
  
> <span data-ttu-id="0f5c3-110">[in]新しいプロファイルのパスワードへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-110">[in] A pointer to the password of the new profile.</span></span> 
    
 <span data-ttu-id="0f5c3-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0f5c3-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="0f5c3-112">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-112">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="0f5c3-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0f5c3-113">_ulFlags_</span></span>
  
> <span data-ttu-id="0f5c3-114">[in]プロファイルの作成方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-114">[in] A bitmask of flags that controls how the profile is created.</span></span> <span data-ttu-id="0f5c3-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-115">The following flags can be set:</span></span>
    
<span data-ttu-id="0f5c3-116">MAPI_DEFAULT_SERVICES</span><span class="sxs-lookup"><span data-stu-id="0f5c3-116">MAPI_DEFAULT_SERVICES</span></span> 
  
> <span data-ttu-id="0f5c3-117">MAPI は、Mapisvc.inf ファイルの [既定のサービス] セクションに含まれるメッセージ サービスを新しいプロファイルに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span></span>
    
<span data-ttu-id="0f5c3-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="0f5c3-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="0f5c3-119">追加するメッセージ サービス内の各プロバイダーの構成プロパティ シートを表示できます。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-119">The configuration property sheets of each of the providers in the message services to be added can be displayed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0f5c3-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="0f5c3-120">Return value</span></span>

<span data-ttu-id="0f5c3-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f5c3-121">S_OK</span></span> 
  
> <span data-ttu-id="0f5c3-122">新しいプロファイルが作成されました。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-122">The new profile was created.</span></span>
    
<span data-ttu-id="0f5c3-123">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0f5c3-123">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0f5c3-124">指定した新しいプロファイルが既に存在します。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-124">The specified new profile already exists.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f5c3-125">注釈</span><span class="sxs-lookup"><span data-stu-id="0f5c3-125">Remarks</span></span>

<span data-ttu-id="0f5c3-126">**IProfAdmin::CreateProfile** メソッドは、新しいプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-126">The **IProfAdmin::CreateProfile** method creates a new profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0f5c3-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="0f5c3-127">Notes to callers</span></span>

<span data-ttu-id="0f5c3-128">**CreateProfile は、アプリケーション** のインストール時またはセッション中にいつでも呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-128">You can call **CreateProfile** at application installation time or at any time during a session.</span></span> <span data-ttu-id="0f5c3-129">インストール時にこのメソッドが呼び出される場合、構成設定の多くは Mapisvc.inf 構成ファイルから取得されます。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-129">When this method is called at installation time, many of the configuration settings come from the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="0f5c3-130">アクティブ なセッション中にこのメソッドが呼び出された場合、設定は、一連のプロパティ シートを介してプロンプトが表示されるユーザーから行います。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-130">When this method is called during an active session, the settings come from the user who is prompted through a series of property sheets.</span></span> 
  
<span data-ttu-id="0f5c3-131">_ulFlags_ パラメーターで MAPI_DEFAULT_SERVICES フラグが設定されている場合 **、CreateProfile** は Mapisvc.inf ファイルの [既定のサービス] セクションの各メッセージ サービスのメッセージ サービス エントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-131">If the MAPI_DEFAULT_SERVICES flag is set in the  _ulFlags_ parameter, **CreateProfile** calls the message service entry point function for each message service in the [Default Services] section in the Mapisvc.inf file.</span></span> <span data-ttu-id="0f5c3-132">各メッセージ サービス エントリ ポイント関数は  _、ulContext_ パラメーターを指定して呼び出MSG_SERVICE_CREATE。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-132">Each message service entry point function is called with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
  
<span data-ttu-id="0f5c3-133">MAPI_DIALOG フラグと MAPI_DEFAULT_SERVICES フラグの両方が設定されている場合は  _、ulUIParam_ パラメーターと  _ulFlags_ パラメーターの値もメッセージ サービスエントリ ポイント関数に渡されます。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-133">If both the MAPI_DIALOG and MAPI_DEFAULT_SERVICES flags are set, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the message service entry point function.</span></span> <span data-ttu-id="0f5c3-134">メッセージ サービスエントリ ポイント関数は、Mapisvc.inf ファイルから利用可能なすべての情報がプロファイルに追加された後にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-134">The message service entry point functions are called only after all available information from the Mapisvc.inf file has been added to the profile.</span></span> 
  
<span data-ttu-id="0f5c3-135">新しいプロファイルの名前とそのパスワードの長さは最大 64 文字で、次の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-135">The name of the new profile and its password can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="0f5c3-136">アクセント文字とアンダースコア文字を含むすべての英数字。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="0f5c3-137">埋め込みスペースですが、先頭または末尾のスペースは使用できません。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="0f5c3-138">_lpszPassword パラメーター_ は NULL または長さ 0 の文字列へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f5c3-138">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f5c3-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f5c3-139">See also</span></span>



[<span data-ttu-id="0f5c3-140">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="0f5c3-140">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="0f5c3-141">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="0f5c3-141">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="0f5c3-142">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="0f5c3-142">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="0f5c3-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0f5c3-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

