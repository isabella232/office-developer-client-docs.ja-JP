---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 162f20485fc21cf8523b6d4a653e52c35f4b3d9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317081"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="dfdb3-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="dfdb3-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="dfdb3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfdb3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfdb3-105">プロファイルに新しい名前を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="dfdb3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dfdb3-106">Parameters</span></span>

 <span data-ttu-id="dfdb3-107">_lpszoldprofilename_</span><span class="sxs-lookup"><span data-stu-id="dfdb3-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="dfdb3-108">順番名前を変更するプロファイルの現在の名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="dfdb3-109">_lpszoldpassword_</span><span class="sxs-lookup"><span data-stu-id="dfdb3-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="dfdb3-110">順番常に NULL。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="dfdb3-111">_lpsznewprofilename_</span><span class="sxs-lookup"><span data-stu-id="dfdb3-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="dfdb3-112">順番名前を変更するプロファイルの新しい名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="dfdb3-113">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="dfdb3-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="dfdb3-114">順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="dfdb3-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dfdb3-115">_ulFlags_</span></span>
  
> <span data-ttu-id="dfdb3-116">順番常に NULL。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dfdb3-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="dfdb3-117">Return value</span></span>

<span data-ttu-id="dfdb3-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="dfdb3-118">S_OK</span></span> 
  
> <span data-ttu-id="dfdb3-119">プロファイルの名前が正常に変更されました。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="dfdb3-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="dfdb3-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="dfdb3-121">プロファイルのパスワードが正しくありません。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="dfdb3-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="dfdb3-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="dfdb3-123">ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dfdb3-124">解説</span><span class="sxs-lookup"><span data-stu-id="dfdb3-124">Remarks</span></span>

<span data-ttu-id="dfdb3-125">**IProfAdmin:: renameprofile**メソッドは、プロファイルに新しい名前を割り当てます (プロファイルがある場合)。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="dfdb3-126">**renameprofile**を呼び出したときに、名前を変更するプロファイルがクライアントによって使用されている場合、 **renameprofile**はプロファイルをマークし、S_OK を返します。プロファイルが使用されている間に名前を変更する操作を試行するのではなく、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="dfdb3-127">プロファイルが使用されなくなると、 **renameprofile**は新しい名前を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="dfdb3-128">プロファイルの新旧の名前は最大64文字の長さにすることができ、次の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="dfdb3-129">アクセント記号とアンダースコア文字を含むすべての英数字。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="dfdb3-130">スペースは埋め込まれますが、先頭または末尾にスペースは含まれません。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="dfdb3-131">_lpszpassword_は常に NULL にするか、長さ0の文字列へのポインターにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dfdb3-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dfdb3-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="dfdb3-132">See also</span></span>



[<span data-ttu-id="dfdb3-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dfdb3-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

