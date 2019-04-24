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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317116"
---
# <a name="iprofadmincreateprofile"></a><span data-ttu-id="200c7-103">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="200c7-103">IProfAdmin::CreateProfile</span></span>

  
  
<span data-ttu-id="200c7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="200c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="200c7-105">新しいプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="200c7-105">Creates a new profile.</span></span>
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="200c7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="200c7-106">Parameters</span></span>

 <span data-ttu-id="200c7-107">_lpszprofilename_</span><span class="sxs-lookup"><span data-stu-id="200c7-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="200c7-108">順番新しいプロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="200c7-108">[in] A pointer to the name of the new profile.</span></span>
    
 <span data-ttu-id="200c7-109">_lpszpassword_</span><span class="sxs-lookup"><span data-stu-id="200c7-109">_lpszPassword_</span></span>
  
> <span data-ttu-id="200c7-110">順番新しいプロファイルのパスワードへのポインター。</span><span class="sxs-lookup"><span data-stu-id="200c7-110">[in] A pointer to the password of the new profile.</span></span> 
    
 <span data-ttu-id="200c7-111">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="200c7-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="200c7-112">順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="200c7-112">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="200c7-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="200c7-113">_ulFlags_</span></span>
  
> <span data-ttu-id="200c7-114">順番プロファイルの作成方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="200c7-114">[in] A bitmask of flags that controls how the profile is created.</span></span> <span data-ttu-id="200c7-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="200c7-115">The following flags can be set:</span></span>
    
<span data-ttu-id="200c7-116">MAPI_DEFAULT_SERVICES</span><span class="sxs-lookup"><span data-stu-id="200c7-116">MAPI_DEFAULT_SERVICES</span></span> 
  
> <span data-ttu-id="200c7-117">MAPI は、mapisvc.inf ファイルの [Default services] セクションに含まれているメッセージサービスで新しいプロファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="200c7-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span></span>
    
<span data-ttu-id="200c7-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="200c7-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="200c7-119">追加するメッセージサービスの各プロバイダーの構成プロパティシートを表示できます。</span><span class="sxs-lookup"><span data-stu-id="200c7-119">The configuration property sheets of each of the providers in the message services to be added can be displayed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="200c7-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="200c7-120">Return value</span></span>

<span data-ttu-id="200c7-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="200c7-121">S_OK</span></span> 
  
> <span data-ttu-id="200c7-122">新しいプロファイルが作成されました。</span><span class="sxs-lookup"><span data-stu-id="200c7-122">The new profile was created.</span></span>
    
<span data-ttu-id="200c7-123">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="200c7-123">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="200c7-124">指定した新しいプロファイルが既に存在します。</span><span class="sxs-lookup"><span data-stu-id="200c7-124">The specified new profile already exists.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="200c7-125">解説</span><span class="sxs-lookup"><span data-stu-id="200c7-125">Remarks</span></span>

<span data-ttu-id="200c7-126">**IProfAdmin:: createprofile**メソッドは、新しいプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="200c7-126">The **IProfAdmin::CreateProfile** method creates a new profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="200c7-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="200c7-127">Notes to callers</span></span>

<span data-ttu-id="200c7-128">**createprofile**は、アプリケーションのインストール時またはセッション中にいつでも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="200c7-128">You can call **CreateProfile** at application installation time or at any time during a session.</span></span> <span data-ttu-id="200c7-129">このメソッドがインストール時に呼び出された場合、構成設定の多くは mapisvc.inf 構成ファイルから取得されます。</span><span class="sxs-lookup"><span data-stu-id="200c7-129">When this method is called at installation time, many of the configuration settings come from the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="200c7-130">アクティブなセッション中にこのメソッドが呼び出された場合、設定は一連のプロパティシートを使用してメッセージを表示するユーザーから取得されます。</span><span class="sxs-lookup"><span data-stu-id="200c7-130">When this method is called during an active session, the settings come from the user who is prompted through a series of property sheets.</span></span> 
  
<span data-ttu-id="200c7-131">MAPI_DEFAULT_SERVICES フラグが_ulflags_パラメーターで設定されている場合、 **createprofile**は mapisvc.inf ファイルの [DEFAULT SERVICES] セクションにある各メッセージサービスに対してメッセージサービスエントリポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="200c7-131">If the MAPI_DEFAULT_SERVICES flag is set in the  _ulFlags_ parameter, **CreateProfile** calls the message service entry point function for each message service in the [Default Services] section in the Mapisvc.inf file.</span></span> <span data-ttu-id="200c7-132">各メッセージサービスエントリポイント関数は、 _ulcontext_パラメーターを MSG_SERVICE_CREATE に設定して呼び出します。</span><span class="sxs-lookup"><span data-stu-id="200c7-132">Each message service entry point function is called with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
  
<span data-ttu-id="200c7-133">MAPI_DIALOG と MAPI_DEFAULT_SERVICES の両方のフラグが設定されている場合、 _uluiparam_パラメーターと_ulflags_パラメーターの値もメッセージサービスエントリポイント関数に渡されます。</span><span class="sxs-lookup"><span data-stu-id="200c7-133">If both the MAPI_DIALOG and MAPI_DEFAULT_SERVICES flags are set, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the message service entry point function.</span></span> <span data-ttu-id="200c7-134">メッセージサービスのエントリポイント関数は、mapisvc.inf ファイルのすべての利用可能な情報がプロファイルに追加された後にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="200c7-134">The message service entry point functions are called only after all available information from the Mapisvc.inf file has been added to the profile.</span></span> 
  
<span data-ttu-id="200c7-135">新しいプロファイルの名前とパスワードは、最大64文字の長さにすることができ、次の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="200c7-135">The name of the new profile and its password can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="200c7-136">アクセント記号とアンダースコア文字を含むすべての英数字。</span><span class="sxs-lookup"><span data-stu-id="200c7-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="200c7-137">スペースは埋め込まれますが、先頭または末尾にスペースは含まれません。</span><span class="sxs-lookup"><span data-stu-id="200c7-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="200c7-138">_lpszpassword_パラメーターは、NULL または長さ0の文字列へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="200c7-138">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="200c7-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="200c7-139">See also</span></span>



[<span data-ttu-id="200c7-140">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="200c7-140">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="200c7-141">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="200c7-141">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="200c7-142">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="200c7-142">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="200c7-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="200c7-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

