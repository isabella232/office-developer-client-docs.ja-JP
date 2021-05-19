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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419521"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="5b02c-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="5b02c-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="5b02c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b02c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b02c-105">プロファイルに新しい名前を割り当てる。</span><span class="sxs-lookup"><span data-stu-id="5b02c-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5b02c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5b02c-106">Parameters</span></span>

 <span data-ttu-id="5b02c-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="5b02c-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="5b02c-108">[in]名前を変更するプロファイルの現在の名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5b02c-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="5b02c-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="5b02c-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="5b02c-110">[in]常に NULL。</span><span class="sxs-lookup"><span data-stu-id="5b02c-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="5b02c-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="5b02c-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="5b02c-112">[in]名前を変更するプロファイルの新しい名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5b02c-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="5b02c-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5b02c-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="5b02c-114">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="5b02c-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="5b02c-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5b02c-115">_ulFlags_</span></span>
  
> <span data-ttu-id="5b02c-116">[in]常に NULL。</span><span class="sxs-lookup"><span data-stu-id="5b02c-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5b02c-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="5b02c-117">Return value</span></span>

<span data-ttu-id="5b02c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b02c-118">S_OK</span></span> 
  
> <span data-ttu-id="5b02c-119">プロファイルの名前が正常に変更されました。</span><span class="sxs-lookup"><span data-stu-id="5b02c-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="5b02c-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="5b02c-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="5b02c-121">プロファイル のパスワードが正しくありません。</span><span class="sxs-lookup"><span data-stu-id="5b02c-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="5b02c-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="5b02c-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="5b02c-123">通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="5b02c-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5b02c-124">注釈</span><span class="sxs-lookup"><span data-stu-id="5b02c-124">Remarks</span></span>

<span data-ttu-id="5b02c-125">**IProfAdmin::RenameProfile** メソッドは、プロファイルがある場合は、新しい名前をプロファイルに割り当てる。</span><span class="sxs-lookup"><span data-stu-id="5b02c-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="5b02c-126">**RenameProfile** が呼び出された場合に、名前を変更するプロファイルがクライアントによって使用されている場合 **、RenameProfile** はプロファイルにマークを付け、プロファイルの実行中に名前の変更操作を試みる代わりに S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="5b02c-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="5b02c-127">プロファイルが使用されなくなった場合 **、RenameProfile は** プロファイルに新しい名前を割り当てる。</span><span class="sxs-lookup"><span data-stu-id="5b02c-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="5b02c-128">プロファイルの古い名前と新しい名前の長さは最大 64 文字で、次の文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5b02c-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="5b02c-129">アクセント文字とアンダースコア文字を含むすべての英数字。</span><span class="sxs-lookup"><span data-stu-id="5b02c-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="5b02c-130">埋め込みスペースですが、先頭または末尾のスペースは使用できません。</span><span class="sxs-lookup"><span data-stu-id="5b02c-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="5b02c-131">_lpszPassword は常_ に NULL または長さ 0 の文字列へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b02c-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5b02c-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="5b02c-132">See also</span></span>



[<span data-ttu-id="5b02c-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b02c-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

