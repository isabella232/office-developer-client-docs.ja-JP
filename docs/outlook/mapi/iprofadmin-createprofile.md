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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a15561a6f3af35c1c7c2285bb6252e6400e0e8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801128"
---
# <a name="iprofadmincreateprofile"></a><span data-ttu-id="5ce94-103">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="5ce94-103">IProfAdmin::CreateProfile</span></span>

  
  
<span data-ttu-id="5ce94-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5ce94-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5ce94-105">新しいプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5ce94-105">Creates a new profile.</span></span>
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5ce94-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5ce94-106">Parameters</span></span>

 <span data-ttu-id="5ce94-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="5ce94-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="5ce94-108">[in]新しいプロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5ce94-108">[in] A pointer to the name of the new profile.</span></span>
    
 <span data-ttu-id="5ce94-109">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="5ce94-109">_lpszPassword_</span></span>
  
> <span data-ttu-id="5ce94-110">[in]新しいプロファイルのパスワードへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5ce94-110">[in] A pointer to the password of the new profile.</span></span> 
    
 <span data-ttu-id="5ce94-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5ce94-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="5ce94-112">[in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="5ce94-112">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="5ce94-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5ce94-113">_ulFlags_</span></span>
  
> <span data-ttu-id="5ce94-114">[in]プロファイルを作成する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="5ce94-114">[in] A bitmask of flags that controls how the profile is created.</span></span> <span data-ttu-id="5ce94-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5ce94-115">The following flags can be set:</span></span>
    
<span data-ttu-id="5ce94-116">MAPI_DEFAULT_SERVICES</span><span class="sxs-lookup"><span data-stu-id="5ce94-116">MAPI_DEFAULT_SERVICES</span></span> 
  
> <span data-ttu-id="5ce94-117">MAPI には、Mapisvc.inf ファイルの [サービスの既定値] セクションに含まれるメッセージ サービスを使用して新しいプロファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ce94-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span></span>
    
<span data-ttu-id="5ce94-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="5ce94-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="5ce94-119">メッセージ サービスに追加するプロバイダーのそれぞれの構成のプロパティ シートを表示できます。</span><span class="sxs-lookup"><span data-stu-id="5ce94-119">The configuration property sheets of each of the providers in the message services to be added can be displayed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5ce94-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5ce94-120">Return value</span></span>

<span data-ttu-id="5ce94-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ce94-121">S_OK</span></span> 
  
> <span data-ttu-id="5ce94-122">新しいプロファイルが作成されました。</span><span class="sxs-lookup"><span data-stu-id="5ce94-122">The new profile was created.</span></span>
    
<span data-ttu-id="5ce94-123">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5ce94-123">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="5ce94-124">指定された新しいプロファイルが既に存在します。</span><span class="sxs-lookup"><span data-stu-id="5ce94-124">The specified new profile already exists.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ce94-125">注釈</span><span class="sxs-lookup"><span data-stu-id="5ce94-125">Remarks</span></span>

<span data-ttu-id="5ce94-126">**IProfAdmin::CreateProfile**メソッドは、新しいプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5ce94-126">The **IProfAdmin::CreateProfile** method creates a new profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5ce94-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5ce94-127">Notes to callers</span></span>

<span data-ttu-id="5ce94-128">**CreateProfile**は、インストール時にアプリケーションまたはセッション中にいつでも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="5ce94-128">You can call **CreateProfile** at application installation time or at any time during a session.</span></span> <span data-ttu-id="5ce94-129">インストール時にこのメソッドが呼び出されると、Mapisvc.inf の構成ファイルから構成設定の多くのもの。</span><span class="sxs-lookup"><span data-stu-id="5ce94-129">When this method is called at installation time, many of the configuration settings come from the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="5ce94-130">アクティブなセッション中にこのメソッドを呼び出すと、設定した一連のプロパティ シートが表示されますユーザーに起因します。</span><span class="sxs-lookup"><span data-stu-id="5ce94-130">When this method is called during an active session, the settings come from the user who is prompted through a series of property sheets.</span></span> 
  
<span data-ttu-id="5ce94-131">_UlFlags_パラメーターに MAPI_DEFAULT_SERVICES フラグを設定すると、 **CreateProfile**は、Mapisvc.inf ファイルの [サービスの既定値] セクションでは、各メッセージ サービスのメッセージ サービスのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5ce94-131">If the MAPI_DEFAULT_SERVICES flag is set in the  _ulFlags_ parameter, **CreateProfile** calls the message service entry point function for each message service in the [Default Services] section in the Mapisvc.inf file.</span></span> <span data-ttu-id="5ce94-132">メッセージの各サービスのエントリ ポイント関数は、MSG_SERVICE_CREATE に_ulContext_パラメーターを使用して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ce94-132">Each message service entry point function is called with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
  
<span data-ttu-id="5ce94-133">MAPI_DIALOG と MAPI_DEFAULT_SERVICES の両方のフラグが設定されている場合、 _ulUIParam_と_ulFlags_パラメーターの値もメッセージ サービスのエントリ ポイント関数に渡されます。</span><span class="sxs-lookup"><span data-stu-id="5ce94-133">If both the MAPI_DIALOG and MAPI_DEFAULT_SERVICES flags are set, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the message service entry point function.</span></span> <span data-ttu-id="5ce94-134">メッセージ サービスのエントリ ポイント関数は、Mapisvc.inf ファイルからのすべての利用可能な情報がプロファイルに追加された後にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ce94-134">The message service entry point functions are called only after all available information from the Mapisvc.inf file has been added to the profile.</span></span> 
  
<span data-ttu-id="5ce94-135">新しいプロファイルとパスワードの名前は 64 文字までの長さにすることができ、次の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5ce94-135">The name of the new profile and its password can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="5ce94-136">すべての英数字文字、アクセント記号付き文字およびアンダー スコア文字を含みます。</span><span class="sxs-lookup"><span data-stu-id="5ce94-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="5ce94-137">埋め込みスペースがいない先頭または末尾のスペース。</span><span class="sxs-lookup"><span data-stu-id="5ce94-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="5ce94-138">_LpszPassword_パラメーターは、NULL または長さ 0 の文字列へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ce94-138">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ce94-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ce94-139">See also</span></span>



[<span data-ttu-id="5ce94-140">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="5ce94-140">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="5ce94-141">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="5ce94-141">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="5ce94-142">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="5ce94-142">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="5ce94-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ce94-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

