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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c94c60cf9ff1adbe2b54bd85b228e21b4be0e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801133"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="093c4-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="093c4-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="093c4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="093c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="093c4-105">プロファイルに新しい名前が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="093c4-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="093c4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="093c4-106">Parameters</span></span>

 <span data-ttu-id="093c4-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="093c4-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="093c4-108">[in]名前を変更するプロファイルの現在の名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="093c4-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="093c4-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="093c4-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="093c4-110">[in]常に NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="093c4-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="093c4-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="093c4-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="093c4-112">[in]名前を変更するプロファイルの新しい名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="093c4-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="093c4-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="093c4-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="093c4-114">[in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="093c4-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="093c4-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="093c4-115">_ulFlags_</span></span>
  
> <span data-ttu-id="093c4-116">[in]常に NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="093c4-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="093c4-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="093c4-117">Return value</span></span>

<span data-ttu-id="093c4-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="093c4-118">S_OK</span></span> 
  
> <span data-ttu-id="093c4-119">プロファイルが変更されました。</span><span class="sxs-lookup"><span data-stu-id="093c4-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="093c4-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="093c4-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="093c4-121">プロファイルのパスワードが正しくないです。</span><span class="sxs-lookup"><span data-stu-id="093c4-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="093c4-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="093c4-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="093c4-123">ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="093c4-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="093c4-124">注釈</span><span class="sxs-lookup"><span data-stu-id="093c4-124">Remarks</span></span>

<span data-ttu-id="093c4-125">**IProfAdmin::RenameProfile**メソッドは、1 つがある場合、プロファイルに新しい名前を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="093c4-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="093c4-126">名前を変更するプロファイルがクライアントによる使用の場合、 **RenameProfile**が呼び出されたときに、 **RenameProfile**は、プロファイルをマークし、プロファイルを使用している間は、名前の変更操作を試みたのではなく、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="093c4-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="093c4-127">プロファイルが使用されていないと、 **RenameProfile**によって新しい名前が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="093c4-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="093c4-128">古いものと新しいプロファイルの名前は 64 文字以内であることができ、次の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="093c4-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="093c4-129">すべての英数字文字、アクセント記号付き文字およびアンダー スコア文字を含みます。</span><span class="sxs-lookup"><span data-stu-id="093c4-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="093c4-130">埋め込みスペースがいない先頭または末尾のスペース。</span><span class="sxs-lookup"><span data-stu-id="093c4-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="093c4-131">_LpszPassword_は NULL または長さ 0 の文字列へのポインターに常にあります。</span><span class="sxs-lookup"><span data-stu-id="093c4-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="093c4-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="093c4-132">See also</span></span>



[<span data-ttu-id="093c4-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="093c4-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

