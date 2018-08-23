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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 694f7ec5715a7348c9bd90c28d14f30d43d19974
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581784"
---
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="f73b8-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="f73b8-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="f73b8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f73b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f73b8-105">新しいサブフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f73b8-105">Creates a new subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="f73b8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f73b8-106">Parameters</span></span>

 <span data-ttu-id="f73b8-107">_ulFolderType_</span><span class="sxs-lookup"><span data-stu-id="f73b8-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="f73b8-108">[in]作成するフォルダーの種類。</span><span class="sxs-lookup"><span data-stu-id="f73b8-108">[in] The type of folder to create.</span></span> <span data-ttu-id="f73b8-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f73b8-109">The following flags can be set:</span></span>
    
<span data-ttu-id="f73b8-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="f73b8-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="f73b8-111">汎用フォルダーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f73b8-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="f73b8-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="f73b8-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="f73b8-113">検索結果のフォルダーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f73b8-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="f73b8-114">_lpszFolderName_</span><span class="sxs-lookup"><span data-stu-id="f73b8-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="f73b8-115">[in]新しいフォルダーの名前を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f73b8-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="f73b8-116">この名前は、新しいフォルダーの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティの基本です。</span><span class="sxs-lookup"><span data-stu-id="f73b8-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="f73b8-117">_lpszFolderComment_</span><span class="sxs-lookup"><span data-stu-id="f73b8-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="f73b8-118">[in]新しいフォルダーに関連付けられているコメントを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f73b8-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="f73b8-119">この文字列では、新しいフォルダーの**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) のプロパティの値になります。</span><span class="sxs-lookup"><span data-stu-id="f73b8-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="f73b8-120">NULL を渡した場合、フォルダーの初期のコメントはありません。</span><span class="sxs-lookup"><span data-stu-id="f73b8-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="f73b8-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f73b8-121">_lpInterface_</span></span>
  
> <span data-ttu-id="f73b8-122">[in]新しいフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f73b8-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="f73b8-123">メッセージ ストア プロバイダーは、フォルダーの標準的なインタ フェースを取得すると、NULL を渡す[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="f73b8-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="f73b8-124">クライアントでは、NULL を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f73b8-124">Clients must pass NULL.</span></span> <span data-ttu-id="f73b8-125">他の呼び出し元に対する、IID_IMAPIProp、IID_IMAPIContainer、または IID_IMAPIFolder、 _lpInterface_パラメーターを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f73b8-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="f73b8-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f73b8-126">_ulFlags_</span></span>
  
> <span data-ttu-id="f73b8-127">[in]フォルダーを作成する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="f73b8-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="f73b8-128">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f73b8-128">The following flags can be set:</span></span>
    
<span data-ttu-id="f73b8-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="f73b8-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="f73b8-130">**CreateFolder**を正常に戻す、可能性のある新しいフォルダーは、呼び出し側のクライアントに完全に利用できる前にするにを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f73b8-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="f73b8-131">新しいフォルダーが使用できない場合は、それ以降の呼び出しを行うとエラーが発生することができます。</span><span class="sxs-lookup"><span data-stu-id="f73b8-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="f73b8-132">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f73b8-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f73b8-133">フォルダーの名前は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="f73b8-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="f73b8-134">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のフォルダー名です。</span><span class="sxs-lookup"><span data-stu-id="f73b8-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="f73b8-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="f73b8-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="f73b8-136">により、その名前を持つ既存のフォルダーを開いて、既に_lpszFolderName_パラメーターで指定されたフォルダーが存在する場合でも成功します。</span><span class="sxs-lookup"><span data-stu-id="f73b8-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="f73b8-137">メッセージ ストア プロバイダーの兄弟に同じ名前のフォルダーを開けない可能性があります既存のフォルダーは、指定された名前の 1 つ以上存在する場合に注意してください。</span><span class="sxs-lookup"><span data-stu-id="f73b8-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="f73b8-138">_lppFolder_</span><span class="sxs-lookup"><span data-stu-id="f73b8-138">_lppFolder_</span></span>
  
> <span data-ttu-id="f73b8-139">[out]新しく作成したフォルダーへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f73b8-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f73b8-140">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f73b8-140">Return value</span></span>

<span data-ttu-id="f73b8-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="f73b8-141">S_OK</span></span> 
  
> <span data-ttu-id="f73b8-142">新しいフォルダーが正常に作成または開くと、OPEN_IF_EXISTS フラグが設定されている場合。</span><span class="sxs-lookup"><span data-stu-id="f73b8-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="f73b8-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f73b8-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f73b8-144">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f73b8-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="f73b8-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="f73b8-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="f73b8-146">既に、 _lpszFolderName_パラメーターで指定された名前を持つフォルダーが存在します。</span><span class="sxs-lookup"><span data-stu-id="f73b8-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="f73b8-147">フォルダー名は一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f73b8-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f73b8-148">注釈</span><span class="sxs-lookup"><span data-stu-id="f73b8-148">Remarks</span></span>

<span data-ttu-id="f73b8-149">**IMAPIFolder::CreateFolder**メソッドは現在のフォルダーにサブフォルダーを作成し、新しいフォルダーのエントリ id を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f73b8-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f73b8-150">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f73b8-150">Notes to callers</span></span>

<span data-ttu-id="f73b8-151">**CreateFolder**が返される場合、その新しいフォルダーのエントリ id が使用できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f73b8-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="f73b8-152">メッセージ ストアのプロバイダーによっては行わないでくださいエントリ id まで使用可能な恒久的に保存するための新しいフォルダーの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出した後。</span><span class="sxs-lookup"><span data-stu-id="f73b8-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="f73b8-153">これは、MAPI_DEFERRED_ERRORS フラグを設定している場合に特に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="f73b8-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="f73b8-154">メッセージ ストアのプロバイダーによっては、フォルダーの標準的なインタ フェースに、 _lpInterface_パラメーターに渡す値に関係なく、 _lppFolder_パラメーターを常にポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="f73b8-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="f73b8-155">返されるインターフェイス ポインターは、必要な種類のできない場合があります、ためには、 **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) のプロパティを取得するために新しいフォルダーの[IMAPIProp::GetProps](imapiprop-getprops.md)のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f73b8-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="f73b8-156">必要に応じて、他の呼び出しを行う前より適切な型へのポインターをキャストします。</span><span class="sxs-lookup"><span data-stu-id="f73b8-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="f73b8-157">通常メッセージ ストア プロバイダーでは、その兄弟フォルダー名に対して一意にする新しいフォルダーの名前が必要です。</span><span class="sxs-lookup"><span data-stu-id="f73b8-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="f73b8-158">この規則に従わない場合に、MAPI_E_COLLISION エラー値を処理できるようにするには。</span><span class="sxs-lookup"><span data-stu-id="f73b8-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="f73b8-159">新しく作成したフォルダーのエントリ id を確認するのに、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティを取得するために、新しいフォルダーの**IMAPIProp::GetProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f73b8-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f73b8-160">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="f73b8-160">MFCMAPI reference</span></span>

<span data-ttu-id="f73b8-161">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="f73b8-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f73b8-162">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="f73b8-162">**File**</span></span>|<span data-ttu-id="f73b8-163">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="f73b8-163">**Function**</span></span>|<span data-ttu-id="f73b8-164">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="f73b8-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f73b8-165">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f73b8-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="f73b8-166">CMsgStoreDlg::OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="f73b8-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="f73b8-167">MFCMAPI では、 **CMsgStoreDlg::OnCreateSubFolder**メソッドを使用して、MFCMAPI で新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f73b8-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f73b8-168">関連項目</span><span class="sxs-lookup"><span data-stu-id="f73b8-168">See also</span></span>



[<span data-ttu-id="f73b8-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="f73b8-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="f73b8-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f73b8-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="f73b8-171">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="f73b8-171">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

