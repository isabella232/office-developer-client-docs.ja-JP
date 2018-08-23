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
ms.openlocfilehash: 4453465c04d7a5a3de79f2ae34d13095863487cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569506"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="7e30a-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="7e30a-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="7e30a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e30a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e30a-105">プロファイルに新しい名前が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="7e30a-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7e30a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7e30a-106">Parameters</span></span>

 <span data-ttu-id="7e30a-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="7e30a-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="7e30a-108">[in]名前を変更するプロファイルの現在の名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7e30a-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="7e30a-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="7e30a-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="7e30a-110">[in]常に NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="7e30a-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="7e30a-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="7e30a-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="7e30a-112">[in]名前を変更するプロファイルの新しい名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7e30a-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="7e30a-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7e30a-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="7e30a-114">[in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="7e30a-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="7e30a-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7e30a-115">_ulFlags_</span></span>
  
> <span data-ttu-id="7e30a-116">[in]常に NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="7e30a-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7e30a-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="7e30a-117">Return value</span></span>

<span data-ttu-id="7e30a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e30a-118">S_OK</span></span> 
  
> <span data-ttu-id="7e30a-119">プロファイルが変更されました。</span><span class="sxs-lookup"><span data-stu-id="7e30a-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="7e30a-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="7e30a-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="7e30a-121">プロファイルのパスワードが正しくないです。</span><span class="sxs-lookup"><span data-stu-id="7e30a-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="7e30a-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="7e30a-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="7e30a-123">ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="7e30a-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7e30a-124">注釈</span><span class="sxs-lookup"><span data-stu-id="7e30a-124">Remarks</span></span>

<span data-ttu-id="7e30a-125">**IProfAdmin::RenameProfile**メソッドは、1 つがある場合、プロファイルに新しい名前を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7e30a-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="7e30a-126">名前を変更するプロファイルがクライアントによる使用の場合、 **RenameProfile**が呼び出されたときに、 **RenameProfile**は、プロファイルをマークし、プロファイルを使用している間は、名前の変更操作を試みたのではなく、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="7e30a-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="7e30a-127">プロファイルが使用されていないと、 **RenameProfile**によって新しい名前が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="7e30a-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="7e30a-128">古いものと新しいプロファイルの名前は 64 文字以内であることができ、次の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7e30a-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="7e30a-129">すべての英数字文字、アクセント記号付き文字およびアンダー スコア文字を含みます。</span><span class="sxs-lookup"><span data-stu-id="7e30a-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="7e30a-130">埋め込みスペースがいない先頭または末尾のスペース。</span><span class="sxs-lookup"><span data-stu-id="7e30a-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="7e30a-131">_LpszPassword_は NULL または長さ 0 の文字列へのポインターに常にあります。</span><span class="sxs-lookup"><span data-stu-id="7e30a-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7e30a-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="7e30a-132">See also</span></span>



[<span data-ttu-id="7e30a-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e30a-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

