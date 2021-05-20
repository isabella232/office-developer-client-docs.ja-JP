---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 606d780aa59e363c30ddc7a5b562db64d845ccb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436763"
---
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="ce751-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ce751-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="ce751-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce751-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce751-105">新しいサブフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ce751-105">Creates a new subfolder.</span></span>
  
```cpp
HRESULT CreateFolder(
  ULONG ulFolderType,
  LPSTR lpszFolderName,
  LPSTR lpszFolderComment,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMAPIFOLDER FAR * lppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="ce751-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ce751-106">Parameters</span></span>

 <span data-ttu-id="ce751-107">_ulFolderType_</span><span class="sxs-lookup"><span data-stu-id="ce751-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="ce751-108">[in]作成するフォルダーの種類。</span><span class="sxs-lookup"><span data-stu-id="ce751-108">[in] The type of folder to create.</span></span> <span data-ttu-id="ce751-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ce751-109">The following flags can be set:</span></span>
    
<span data-ttu-id="ce751-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="ce751-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="ce751-111">汎用フォルダーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce751-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="ce751-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="ce751-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="ce751-113">検索結果フォルダーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce751-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="ce751-114">_lpszFolderName_</span><span class="sxs-lookup"><span data-stu-id="ce751-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="ce751-115">[in]新しいフォルダーの名前を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ce751-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="ce751-116">この名前は、新しいフォルダーのプロパティ [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)**プロパティPR_DISPLAY_NAME基** になります。</span><span class="sxs-lookup"><span data-stu-id="ce751-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="ce751-117">_lpszFolderComment_</span><span class="sxs-lookup"><span data-stu-id="ce751-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="ce751-118">[in]新しいフォルダーに関連付けられたコメントを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ce751-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="ce751-119">この文字列は、新しいフォルダーのプロパティ ([PidTagComment](pidtagcomment-canonical-property.md)) **PR_COMMENT** の値になります。</span><span class="sxs-lookup"><span data-stu-id="ce751-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="ce751-120">NULL が渡された場合、フォルダーには最初のコメントはありません。</span><span class="sxs-lookup"><span data-stu-id="ce751-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="ce751-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ce751-121">_lpInterface_</span></span>
  
> <span data-ttu-id="ce751-122">[in]新しいフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ce751-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="ce751-123">NULL を渡すと、メッセージ ストア プロバイダーは標準のフォルダー インターフェイス [IMAPIFolder : IMAPIContainer を返します](imapifolderimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="ce751-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="ce751-124">クライアントは NULL を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce751-124">Clients must pass NULL.</span></span> <span data-ttu-id="ce751-125">他の呼び出し元は  _、lpInterface_ パラメーターを、IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、またはIID_IMAPIFolder。</span><span class="sxs-lookup"><span data-stu-id="ce751-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="ce751-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ce751-126">_ulFlags_</span></span>
  
> <span data-ttu-id="ce751-127">[in]フォルダーの作成方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ce751-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="ce751-128">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ce751-128">The following flags can be set:</span></span>
    
<span data-ttu-id="ce751-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ce751-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ce751-130">新しいフォルダーが呼び出し元のクライアントで完全に使用できる前に **、CreateFolder** を正常に返します。</span><span class="sxs-lookup"><span data-stu-id="ce751-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="ce751-131">新しいフォルダーを使用できない場合は、そのフォルダーを後続の呼び出しで呼び出した場合、エラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ce751-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="ce751-132">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ce751-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ce751-133">フォルダーの名前は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="ce751-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="ce751-134">このフラグMAPI_UNICODE設定されていない場合、フォルダー名は ANSI 形式です。</span><span class="sxs-lookup"><span data-stu-id="ce751-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="ce751-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="ce751-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="ce751-136">_lpszFolderName_ パラメーターで指定されたフォルダーが既に存在する場合でも、その名前を持つ既存のフォルダーを開いて、メソッドを成功できます。</span><span class="sxs-lookup"><span data-stu-id="ce751-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="ce751-137">同じ名前の兄弟フォルダーを許可するメッセージ ストア プロバイダーは、指定された名前で複数のフォルダーが存在する場合、既存のフォルダーを開かない場合があります。</span><span class="sxs-lookup"><span data-stu-id="ce751-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="ce751-138">_lppFolder_</span><span class="sxs-lookup"><span data-stu-id="ce751-138">_lppFolder_</span></span>
  
> <span data-ttu-id="ce751-139">[out]新しく作成されたフォルダーへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="ce751-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ce751-140">戻り値</span><span class="sxs-lookup"><span data-stu-id="ce751-140">Return value</span></span>

<span data-ttu-id="ce751-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce751-141">S_OK</span></span> 
  
> <span data-ttu-id="ce751-142">新しいフォルダーが正常に作成または開かされました (OPEN_IF_EXISTSが設定されている場合)。</span><span class="sxs-lookup"><span data-stu-id="ce751-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="ce751-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ce751-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ce751-144">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ce751-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="ce751-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="ce751-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="ce751-146">_lpszFolderName_ パラメーターに指定された名前を持つフォルダーが既に存在します。</span><span class="sxs-lookup"><span data-stu-id="ce751-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="ce751-147">フォルダー名は一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce751-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ce751-148">注釈</span><span class="sxs-lookup"><span data-stu-id="ce751-148">Remarks</span></span>

<span data-ttu-id="ce751-149">**IMAPIFolder::CreateFolder** メソッドは、現在のフォルダーにサブフォルダーを作成し、新しいフォルダーにエントリ識別子を割り当てる。</span><span class="sxs-lookup"><span data-stu-id="ce751-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ce751-150">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ce751-150">Notes to callers</span></span>

<span data-ttu-id="ce751-151">**CreateFolder が返** される場合は、新しいフォルダーのエントリ識別子が使用できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ce751-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="ce751-152">一部のメッセージ ストア プロバイダーは、新しいフォルダーの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出して完全に保存するまで、エントリ識別子を使用できません。</span><span class="sxs-lookup"><span data-stu-id="ce751-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="ce751-153">これは、このフラグを設定している場合は特にMAPI_DEFERRED_ERRORSです。</span><span class="sxs-lookup"><span data-stu-id="ce751-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="ce751-154">一部のメッセージ ストア プロバイダーは _、lpInterface_ パラメーターに渡す値に関係なく、常に _lppFolder_ パラメーターをフォルダーの標準インターフェイスにポイントします。</span><span class="sxs-lookup"><span data-stu-id="ce751-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="ce751-155">返されるインターフェイス ポインターは、必要な種類ではない可能性があります。ため、新しいフォルダーの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して **、PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="ce751-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="ce751-156">必要に応じて、他の呼び出しを行う前に、ポインターをより適切な型にキャストします。</span><span class="sxs-lookup"><span data-stu-id="ce751-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="ce751-157">ほとんどのメッセージ ストア プロバイダーでは、新しいフォルダーの名前が兄弟フォルダーの名前に対して一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce751-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="ce751-158">このルールに従MAPI_E_COLLISION返されるエラー値を処理できます。</span><span class="sxs-lookup"><span data-stu-id="ce751-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="ce751-159">新しく作成したフォルダーのエントリ識別子を確認するには、新しいフォルダーの **IMAPIProp::GetProps** メソッドを呼び出して、PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="ce751-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ce751-160">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="ce751-160">MFCMAPI reference</span></span>

<span data-ttu-id="ce751-161">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce751-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ce751-162">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="ce751-162">**File**</span></span>|<span data-ttu-id="ce751-163">**関数**</span><span class="sxs-lookup"><span data-stu-id="ce751-163">**Function**</span></span>|<span data-ttu-id="ce751-164">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ce751-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce751-165">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ce751-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="ce751-166">CMsgStoreDlg::OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="ce751-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="ce751-167">MFCMAPI は **、CMsgStoreDlg::OnCreateSubFolder** メソッドを使用して、MFCMAPI で新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ce751-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce751-168">関連項目</span><span class="sxs-lookup"><span data-stu-id="ce751-168">See also</span></span>



[<span data-ttu-id="ce751-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="ce751-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="ce751-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ce751-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="ce751-171">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ce751-171">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

