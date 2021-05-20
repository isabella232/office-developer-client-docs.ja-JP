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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c3c4ac10003aad8949de94e0f144410af10078b1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437239"
---
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="4cda3-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="4cda3-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="4cda3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cda3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cda3-105">プロファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="4cda3-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4cda3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4cda3-106">Parameters</span></span>

 <span data-ttu-id="4cda3-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="4cda3-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="4cda3-108">[in]コピーするプロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4cda3-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="4cda3-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="4cda3-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="4cda3-110">[in]コピーするプロファイルのパスワードへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4cda3-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="4cda3-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="4cda3-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="4cda3-112">[in]コピーされたプロファイルの新しい名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4cda3-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="4cda3-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4cda3-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="4cda3-114">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="4cda3-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="4cda3-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4cda3-115">_ulFlags_</span></span>
  
> <span data-ttu-id="4cda3-116">[in]プロファイルのコピー方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="4cda3-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="4cda3-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4cda3-117">The following flags can be set:</span></span>
    
<span data-ttu-id="4cda3-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="4cda3-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="4cda3-119">コピーするプロファイルの正しいパスワードをユーザーに求めるダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="4cda3-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="4cda3-120">このフラグが設定されていない場合、ダイアログ ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="4cda3-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4cda3-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="4cda3-121">Return value</span></span>

<span data-ttu-id="4cda3-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="4cda3-122">S_OK</span></span> 
  
> <span data-ttu-id="4cda3-123">プロファイルが正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="4cda3-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="4cda3-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="4cda3-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="4cda3-125">新しいプロファイル名は、既存のプロファイルと同じです。</span><span class="sxs-lookup"><span data-stu-id="4cda3-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="4cda3-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="4cda3-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="4cda3-127">プロファイルをコピーするパスワードが正しくないので、MAPI_DIALOG が  _ulFlags_ パラメーターで設定されていないので、正しいパスワードを要求するダイアログ ボックスをユーザーに表示できません。</span><span class="sxs-lookup"><span data-stu-id="4cda3-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="4cda3-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4cda3-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="4cda3-129">指定したプロファイルが存在しません。</span><span class="sxs-lookup"><span data-stu-id="4cda3-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="4cda3-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="4cda3-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="4cda3-131">通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="4cda3-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4cda3-132">注釈</span><span class="sxs-lookup"><span data-stu-id="4cda3-132">Remarks</span></span>

<span data-ttu-id="4cda3-133">**IProfAdmin::CopyProfile** メソッドは _、lpszOldProfileName_ が指すプロファイルのコピーを作成し _、lpszNewProfileName_ によって指される名前を与える。</span><span class="sxs-lookup"><span data-stu-id="4cda3-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="4cda3-134">プロファイルをコピーすると、コピーには元のパスワードと同じパスワードが残ります。</span><span class="sxs-lookup"><span data-stu-id="4cda3-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="4cda3-135">元のプロファイルの名前、パスワード、およびコピーの長さは最大 64 文字で、次の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4cda3-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="4cda3-136">アクセント文字とアンダースコア文字を含むすべての英数字。</span><span class="sxs-lookup"><span data-stu-id="4cda3-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="4cda3-137">埋め込みスペースですが、先頭または末尾のスペースは使用できません。</span><span class="sxs-lookup"><span data-stu-id="4cda3-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="4cda3-138">プロファイル パスワードは、すべてのオペレーティング システムではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4cda3-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="4cda3-139">プロファイル パスワードをサポートしないオペレーティング システムでは  _、lpszOldPassword_ には NULL または長さ 0 の文字列へのポインターを指定できます。</span><span class="sxs-lookup"><span data-stu-id="4cda3-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="4cda3-140">_lpszOldPassword_ が NULL に設定されている場合、コピーするプロファイルにはパスワードが必要であり、MAPI_DIALOGフラグが設定されます。パスワードの入力を求めるダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4cda3-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="4cda3-141">パスワードが必要ですが  _、lpszOldPassword_ が NULL に設定され、MAPI_DIALOG フラグが設定されていない場合 **、CopyProfile** はパスワードをMAPI_E_LOGON_FAILED。</span><span class="sxs-lookup"><span data-stu-id="4cda3-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4cda3-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="4cda3-142">See also</span></span>



[<span data-ttu-id="4cda3-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4cda3-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

