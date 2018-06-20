---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cd70f5ee7b58bdf0b1fd61b1056bfc77e3e35992
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801122"
---
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="a5450-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="a5450-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="a5450-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a5450-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a5450-105">プロファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="a5450-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a5450-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a5450-106">Parameters</span></span>

 <span data-ttu-id="a5450-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="a5450-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="a5450-108">[in]コピーするプロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a5450-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="a5450-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="a5450-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="a5450-110">[in]コピーするプロファイルのパスワードへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a5450-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="a5450-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="a5450-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="a5450-112">[in]コピー先のプロファイルの新しい名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a5450-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="a5450-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a5450-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="a5450-114">[in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="a5450-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="a5450-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a5450-115">_ulFlags_</span></span>
  
> <span data-ttu-id="a5450-116">[in]プロファイルをコピーする方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="a5450-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="a5450-117">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a5450-117">The following flags can be set:</span></span>
    
<span data-ttu-id="a5450-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a5450-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="a5450-119">プロファイルの正しいパスワードをコピーするのにはユーザーの入力を求めるダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5450-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="a5450-120">このフラグが設定されていない場合、ダイアログ ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="a5450-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5450-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a5450-121">Return value</span></span>

<span data-ttu-id="a5450-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5450-122">S_OK</span></span> 
  
> <span data-ttu-id="a5450-123">プロファイルは正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="a5450-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="a5450-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="a5450-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="a5450-125">新しいプロファイル名は、既存のプロファイルと同じです。</span><span class="sxs-lookup"><span data-stu-id="a5450-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="a5450-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="a5450-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="a5450-127">コピーするプロファイルのパスワードが正しくないと、MAPI_DIALOG が_ulFlags_パラメーターで設定されていませんでしたので、正しいパスワードを要求するユーザーに、ダイアログ ボックスを表示できませんでした。</span><span class="sxs-lookup"><span data-stu-id="a5450-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="a5450-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a5450-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a5450-129">指定されたプロファイルが存在しません。</span><span class="sxs-lookup"><span data-stu-id="a5450-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="a5450-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a5450-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a5450-131">ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="a5450-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a5450-132">備考</span><span class="sxs-lookup"><span data-stu-id="a5450-132">Remarks</span></span>

<span data-ttu-id="a5450-133">**IProfAdmin::CopyProfile**メソッドは、 _lpszNewProfileName_で指定された名前を付けることが_lpszOldProfileName_を指すプロファイルのコピーを使用します。</span><span class="sxs-lookup"><span data-stu-id="a5450-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="a5450-134">プロファイルのコピー元と同じパスワードを使用してコピーを残します。</span><span class="sxs-lookup"><span data-stu-id="a5450-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="a5450-135">元のプロファイル、そのパスワード、およびコピーの名前は 64 文字までの長さにすることができ、次の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a5450-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="a5450-136">すべての英数字文字、アクセント記号付き文字およびアンダー スコア文字を含みます。</span><span class="sxs-lookup"><span data-stu-id="a5450-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="a5450-137">埋め込みスペースがいない先頭または末尾のスペース。</span><span class="sxs-lookup"><span data-stu-id="a5450-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="a5450-138">プロファイルのパスワードは、すべてのオペレーティング システムではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a5450-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="a5450-139">プロファイルのパスワードをサポートしていないオペレーティング システムで_lpszOldPassword_できます NULL または長さ 0 の文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a5450-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="a5450-140">コピーするプロファイルがパスワードを必要とし、MAPI_DIALOG フラグが設定されている_lpszOldPassword_は、NULL に設定されている場合ユーザーにパスワードの入力を求めるダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5450-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="a5450-141">パスワードが必要ですが、 _lpszOldPassword_は NULL に設定されて、MAPI_DIALOG フラグが設定されていない場合、 **CopyProfile**は MAPI_E_LOGON_FAILED を返します。</span><span class="sxs-lookup"><span data-stu-id="a5450-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a5450-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="a5450-142">See also</span></span>



[<span data-ttu-id="a5450-143">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5450-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

