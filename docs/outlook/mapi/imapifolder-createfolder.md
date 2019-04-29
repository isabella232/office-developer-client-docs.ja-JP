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
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="2678a-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="2678a-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="2678a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2678a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2678a-105">新しいサブフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2678a-105">Creates a new subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="2678a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2678a-106">Parameters</span></span>

 <span data-ttu-id="2678a-107">_ulfoldertype_</span><span class="sxs-lookup"><span data-stu-id="2678a-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="2678a-108">順番作成するフォルダーの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="2678a-108">[in] The type of folder to create.</span></span> <span data-ttu-id="2678a-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2678a-109">The following flags can be set:</span></span>
    
<span data-ttu-id="2678a-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="2678a-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="2678a-111">汎用フォルダーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2678a-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="2678a-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="2678a-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="2678a-113">検索結果フォルダーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2678a-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="2678a-114">_lpszfoldername_</span><span class="sxs-lookup"><span data-stu-id="2678a-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="2678a-115">順番新しいフォルダーの名前を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2678a-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="2678a-116">この名前は、新しいフォルダーの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの基礎となります。</span><span class="sxs-lookup"><span data-stu-id="2678a-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="2678a-117">_lpszfoldercomment_</span><span class="sxs-lookup"><span data-stu-id="2678a-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="2678a-118">順番新しいフォルダーに関連付けられているコメントを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2678a-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="2678a-119">この文字列は、新しいフォルダーの**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) プロパティの値になります。</span><span class="sxs-lookup"><span data-stu-id="2678a-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="2678a-120">NULL が渡された場合、フォルダーには最初のコメントがありません。</span><span class="sxs-lookup"><span data-stu-id="2678a-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="2678a-121">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="2678a-121">_lpInterface_</span></span>
  
> <span data-ttu-id="2678a-122">順番新しいフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2678a-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="2678a-123">NULL を渡すと、メッセージストアプロバイダーは標準のフォルダーインターフェイス、 [imapifolder: IMAPIContainer](imapifolderimapicontainer.md)を返します。</span><span class="sxs-lookup"><span data-stu-id="2678a-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="2678a-124">クライアントは、NULL を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2678a-124">Clients must pass NULL.</span></span> <span data-ttu-id="2678a-125">他の呼び出し元が_lpinterface_パラメーターを IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、または IID_IMAPIFolder に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2678a-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="2678a-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2678a-126">_ulFlags_</span></span>
  
> <span data-ttu-id="2678a-127">順番フォルダーの作成方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="2678a-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="2678a-128">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2678a-128">The following flags can be set:</span></span>
    
<span data-ttu-id="2678a-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="2678a-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="2678a-130">呼び出し元クライアントが新しいフォルダーを完全に使用できるようになるまで、 **CreateFolder**が正常に戻ることができるようにします。</span><span class="sxs-lookup"><span data-stu-id="2678a-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="2678a-131">新しいフォルダーを使用できない場合は、それ以降の呼び出しを行うとエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2678a-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="2678a-132">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2678a-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2678a-133">フォルダーの名前は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="2678a-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="2678a-134">MAPI_UNICODE フラグが設定されていない場合、フォルダー名は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="2678a-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="2678a-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="2678a-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="2678a-136">指定した名前の既存のフォルダーを開いて、 _lpszfoldername_パラメーターで指定されたフォルダーが既に存在する場合でも、メソッドを正常に実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2678a-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="2678a-137">兄弟フォルダーに同じ名前を付けることができるメッセージストアプロバイダーは、指定された名前で複数のフォルダーが存在する場合は、既存のフォルダーを開かないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2678a-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="2678a-138">_lppfolder_</span><span class="sxs-lookup"><span data-stu-id="2678a-138">_lppFolder_</span></span>
  
> <span data-ttu-id="2678a-139">読み上げ新しく作成されたフォルダーへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2678a-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2678a-140">戻り値</span><span class="sxs-lookup"><span data-stu-id="2678a-140">Return value</span></span>

<span data-ttu-id="2678a-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="2678a-141">S_OK</span></span> 
  
> <span data-ttu-id="2678a-142">OPEN_IF_EXISTS フラグが設定されている場合、新しいフォルダーが正常に作成または開きます。</span><span class="sxs-lookup"><span data-stu-id="2678a-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="2678a-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2678a-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2678a-144">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="2678a-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="2678a-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="2678a-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="2678a-146">_lpszfoldername_パラメーターに指定した名前のフォルダーが既に存在します。</span><span class="sxs-lookup"><span data-stu-id="2678a-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="2678a-147">フォルダー名は一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2678a-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2678a-148">注釈</span><span class="sxs-lookup"><span data-stu-id="2678a-148">Remarks</span></span>

<span data-ttu-id="2678a-149">**imapifolder:: CreateFolder**メソッドを実行すると、現在のフォルダーにサブフォルダーが作成され、新しいフォルダーにエントリ識別子が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2678a-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2678a-150">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2678a-150">Notes to callers</span></span>

<span data-ttu-id="2678a-151">**CreateFolder**が返された場合は、新しいフォルダーのエントリ識別子が使用できない可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2678a-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="2678a-152">メッセージストアプロバイダーによっては、完全に保存するために、新しいフォルダーの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出した後に、エントリ識別子を使用できないことがあります。</span><span class="sxs-lookup"><span data-stu-id="2678a-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="2678a-153">これは、MAPI_DEFERRED_ERRORS フラグが設定されている場合に特に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="2678a-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="2678a-154">一部のメッセージストアプロバイダーは、 _lpinterface_パラメーターに渡す値に関係なく、常に_lppfolder_パラメーターをフォルダーの標準インターフェイスにポイントすることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2678a-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="2678a-155">返されるインターフェイスポインターが予期した型ではない場合があるため、新しいフォルダーの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="2678a-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="2678a-156">必要に応じて、他の呼び出しを行う前に、適切な型にポインターをキャストしてください。</span><span class="sxs-lookup"><span data-stu-id="2678a-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="2678a-157">ほとんどのメッセージストアプロバイダーでは、兄弟フォルダーの名前に対して一意の新しいフォルダー名が必要です。</span><span class="sxs-lookup"><span data-stu-id="2678a-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="2678a-158">このルールに従っていない場合に返される MAPI_E_COLLISION エラー値を処理できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2678a-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="2678a-159">新しく作成されたフォルダーのエントリ識別子を特定するには、新しいフォルダーの**imapiprop:: GetProps**メソッドを呼び出して、そのフォルダーの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="2678a-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2678a-160">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="2678a-160">MFCMAPI reference</span></span>

<span data-ttu-id="2678a-161">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2678a-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2678a-162">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="2678a-162">**File**</span></span>|<span data-ttu-id="2678a-163">**関数**</span><span class="sxs-lookup"><span data-stu-id="2678a-163">**Function**</span></span>|<span data-ttu-id="2678a-164">**コメント**</span><span class="sxs-lookup"><span data-stu-id="2678a-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2678a-165">MsgStoreDlg</span><span class="sxs-lookup"><span data-stu-id="2678a-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="2678a-166">CMsgStoreDlg:: OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="2678a-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="2678a-167">mfcmapi は、 **CMsgStoreDlg:: OnCreateSubFolder**メソッドを使用して、mfcmapi に新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2678a-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2678a-168">関連項目</span><span class="sxs-lookup"><span data-stu-id="2678a-168">See also</span></span>



[<span data-ttu-id="2678a-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="2678a-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="2678a-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="2678a-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="2678a-171">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2678a-171">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

