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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309570"
---
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="44c01-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="44c01-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="44c01-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44c01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44c01-105">プロファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="44c01-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="44c01-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="44c01-106">Parameters</span></span>

 <span data-ttu-id="44c01-107">_lpszoldprofilename_</span><span class="sxs-lookup"><span data-stu-id="44c01-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="44c01-108">順番コピーするプロファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="44c01-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="44c01-109">_lpszoldpassword_</span><span class="sxs-lookup"><span data-stu-id="44c01-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="44c01-110">順番コピーするプロファイルのパスワードへのポインター。</span><span class="sxs-lookup"><span data-stu-id="44c01-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="44c01-111">_lpsznewprofilename_</span><span class="sxs-lookup"><span data-stu-id="44c01-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="44c01-112">順番コピーされたプロファイルの新しい名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="44c01-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="44c01-113">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="44c01-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="44c01-114">順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="44c01-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="44c01-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="44c01-115">_ulFlags_</span></span>
  
> <span data-ttu-id="44c01-116">順番プロファイルのコピー方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="44c01-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="44c01-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="44c01-117">The following flags can be set:</span></span>
    
<span data-ttu-id="44c01-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="44c01-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="44c01-119">コピーするプロファイルの正しいパスワードをユーザーに確認するダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="44c01-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="44c01-120">このフラグが設定されていない場合は、ダイアログボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="44c01-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="44c01-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="44c01-121">Return value</span></span>

<span data-ttu-id="44c01-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="44c01-122">S_OK</span></span> 
  
> <span data-ttu-id="44c01-123">プロファイルが正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="44c01-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="44c01-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="44c01-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="44c01-125">新しいプロファイル名は、既存のプロファイルの名前と同じです。</span><span class="sxs-lookup"><span data-stu-id="44c01-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="44c01-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="44c01-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="44c01-127">コピーするプロファイルのパスワードが正しくありません。 MAPI_DIALOG が_ulflags_パラメーターで設定されていないため、ユーザーに正しいパスワードを要求するためのダイアログボックスを表示できませんでした。</span><span class="sxs-lookup"><span data-stu-id="44c01-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="44c01-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="44c01-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="44c01-129">指定されたプロファイルが存在しません。</span><span class="sxs-lookup"><span data-stu-id="44c01-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="44c01-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="44c01-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="44c01-131">ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="44c01-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="44c01-132">解説</span><span class="sxs-lookup"><span data-stu-id="44c01-132">Remarks</span></span>

<span data-ttu-id="44c01-133">**IProfAdmin:: copyprofile**メソッドは、 _lpszoldprofilename_によって参照されているプロファイルのコピーを作成し、 _lpszoldprofilename_で指定された名前を付与します。</span><span class="sxs-lookup"><span data-stu-id="44c01-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="44c01-134">プロファイルをコピーすると、元のパスワードと同じパスワードでコピーが残ります。</span><span class="sxs-lookup"><span data-stu-id="44c01-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="44c01-135">元のプロファイルの名前、パスワード、およびコピーの長さは最大64文字で、次の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="44c01-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="44c01-136">アクセント記号とアンダースコア文字を含むすべての英数字。</span><span class="sxs-lookup"><span data-stu-id="44c01-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="44c01-137">スペースは埋め込まれますが、先頭または末尾にスペースは含まれません。</span><span class="sxs-lookup"><span data-stu-id="44c01-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="44c01-138">プロファイルパスワードは、すべてのオペレーティングシステムでサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="44c01-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="44c01-139">プロファイルパスワードをサポートしていないオペレーティングシステムでは、 _lpszoldpassword_は NULL または長さ0の文字列へのポインターにすることができます。</span><span class="sxs-lookup"><span data-stu-id="44c01-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="44c01-140">_lpszoldpassword_が NULL に設定されている場合、コピーされるプロファイルにはパスワードが必要です。また、MAPI_DIALOG フラグが設定されています。ユーザーにパスワードの入力を求めるダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="44c01-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="44c01-141">パスワードが必要で、 _lpszoldpassword_が NULL に設定されていて、MAPI_DIALOG フラグが設定されていない場合、 **copyprofile**は MAPI_E_LOGON_FAILED を返します。</span><span class="sxs-lookup"><span data-stu-id="44c01-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44c01-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="44c01-142">See also</span></span>



[<span data-ttu-id="44c01-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="44c01-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

