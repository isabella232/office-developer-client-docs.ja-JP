---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405584"
---
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="40ffd-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="40ffd-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="40ffd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40ffd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40ffd-105">オブジェクトの 1 つ以上のプロパティを別のオブジェクトにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="40ffd-105">Copies or moves one or more properties of an object to another object.</span></span>
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="40ffd-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="40ffd-106">Parameters</span></span>

 <span data-ttu-id="40ffd-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="40ffd-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="40ffd-108">[in]コピーまたは移動するプロパティを持つオブジェクトにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="40ffd-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="40ffd-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="40ffd-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="40ffd-110">[in]コピーまたは移動するプロパティを含むオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="40ffd-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="40ffd-111">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="40ffd-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="40ffd-112">[in]コピーまたは移動するプロパティを示すプロパティ タグのカウントされた配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="40ffd-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="40ffd-113">_lpIncludeProps_ パラメーターを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="40ffd-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="40ffd-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="40ffd-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="40ffd-115">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="40ffd-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="40ffd-116">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="40ffd-116">_lpProgress_</span></span>
  
> <span data-ttu-id="40ffd-117">[in]進行状況インジケーターの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="40ffd-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="40ffd-118">_lpProgress_ パラメーターで NULL が渡された場合、MAPI 実装を使用して進行状況インジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="40ffd-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="40ffd-119">_lpProgress パラメーター_ は _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="40ffd-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="40ffd-120">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="40ffd-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="40ffd-121">[in]オブジェクトにアクセスして、コピーまたは移動されるプロパティを受け取るインターフェイスを表すインターフェイス識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="40ffd-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="40ffd-122">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="40ffd-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="40ffd-123">[in]コピーまたは移動されたプロパティを受け取るオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="40ffd-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="40ffd-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="40ffd-124">_ulFlags_</span></span>
  
> <span data-ttu-id="40ffd-125">[in]コピーまたは移動操作の実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="40ffd-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="40ffd-126">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="40ffd-126">The following flags can be set:</span></span>
    
<span data-ttu-id="40ffd-127">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="40ffd-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="40ffd-128">進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="40ffd-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="40ffd-129">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="40ffd-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="40ffd-130">**DoCopyProps は、** コピー操作の代わりに移動操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40ffd-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="40ffd-131">このフラグを設定しない場合 **、DoCopyProps は** コピー操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="40ffd-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="40ffd-132">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="40ffd-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="40ffd-133">移動先オブジェクト内の既存のプロパティは上書きしないでください。</span><span class="sxs-lookup"><span data-stu-id="40ffd-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="40ffd-134">このフラグを設定しない場合 **、DoCopyProps は既存** のプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="40ffd-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="40ffd-135">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="40ffd-135">_lppProblems_</span></span>
  
> <span data-ttu-id="40ffd-136">[in, out]入力時に [、SPropProblemArray](spropproblemarray.md) 構造体へのポインターを指すポインター。それ以外の場合は、エラー情報を必要としない NULL を指定します。</span><span class="sxs-lookup"><span data-stu-id="40ffd-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="40ffd-137">_lppProblems が_ 入力の有効なポインターである場合 **、DoCopyProps** は 1 つ以上のプロパティをコピーするエラーに関する詳細情報を返します。</span><span class="sxs-lookup"><span data-stu-id="40ffd-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="40ffd-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="40ffd-138">Return value</span></span>

<span data-ttu-id="40ffd-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="40ffd-139">S_OK</span></span> 
  
> <span data-ttu-id="40ffd-140">プロパティが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="40ffd-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="40ffd-141">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="40ffd-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="40ffd-142">コピーまたは移動するプロパティは、コピー先オブジェクトに既に存在し、MAPI_NOREPLACEフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="40ffd-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="40ffd-143">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="40ffd-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="40ffd-144">ソース オブジェクトには、直接または間接的に移動先オブジェクトが含まれる。</span><span class="sxs-lookup"><span data-stu-id="40ffd-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="40ffd-145">この条件が検出される前に重要な作業が実行された可能性があります。そのため、ソース オブジェクトと移動先オブジェクトが部分的に変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="40ffd-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="40ffd-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="40ffd-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="40ffd-147">_lpSrcInterface_ パラメーターで識別されるインターフェイスは、ソース オブジェクトでサポートされていないか _、lpDestInterface_ パラメーターで識別されるインターフェイスは、移動先オブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="40ffd-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="40ffd-148">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="40ffd-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="40ffd-149">呼び出し元のアクセス許可が不十分なオブジェクトにアクセスしようとした。</span><span class="sxs-lookup"><span data-stu-id="40ffd-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="40ffd-150">このエラーは、移動先オブジェクトがソース オブジェクトと同じ場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="40ffd-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="40ffd-151">次の値は **、SPropProblemArray** 構造体で返されますが **、DoCopyProps の戻り値として返す値として返す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="40ffd-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="40ffd-152">これらのエラーは、1 つのプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="40ffd-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="40ffd-153">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="40ffd-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="40ffd-154">このフラグMAPI_UNICODE設定され **、DoCopyProps** が Unicode をサポートしていないか、または MAPI_UNICODEが設定されていないと **DoCopyProps** は Unicode のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="40ffd-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="40ffd-155">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="40ffd-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="40ffd-156">プロパティは、読み取り専用プロパティなので、呼び出し元が変更することはできません。これは、移動先オブジェクトの所有者によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="40ffd-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="40ffd-157">このエラーは重大ではありません。呼び出し元は、コピー操作の続行を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40ffd-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="40ffd-158">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="40ffd-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="40ffd-159">プロパティの種類が無効です。</span><span class="sxs-lookup"><span data-stu-id="40ffd-159">The property type is invalid.</span></span>
    
<span data-ttu-id="40ffd-160">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="40ffd-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="40ffd-161">プロパティの種類は、呼び出し元が期待する型ではありません。</span><span class="sxs-lookup"><span data-stu-id="40ffd-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40ffd-162">注釈</span><span class="sxs-lookup"><span data-stu-id="40ffd-162">Remarks</span></span>

<span data-ttu-id="40ffd-163">**IMAPISupport::D oCopyProps** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="40ffd-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="40ffd-164">メッセージ ストア プロバイダーは **、DoCopyProps** を呼び出して、フォルダーとメッセージの [IMAPIProp::CopyProps](imapiprop-copyprops.md) メソッドを実装できます。</span><span class="sxs-lookup"><span data-stu-id="40ffd-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="40ffd-165">**DoCopyProps** は  _、lpIncludeProps_ が指すプロパティ タグ配列で識別され  _、lpSrcObj_ が指すオブジェクトに存在するプロパティをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="40ffd-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="40ffd-166">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="40ffd-166">Notes to callers</span></span>

<span data-ttu-id="40ffd-167">2 つのメッセージなど、同じ種類のオブジェクト間でプロパティをコピーする場合  _、lpSrcInterface_ パラメーターと  _lpDestInterface_ パラメーターには同じインターフェイス識別子が含まれている必要があります。  _また、lpSrcObj_ パラメーターと  _lpDestObj_ パラメーターは、同じ種類のオブジェクトを指している必要があります。</span><span class="sxs-lookup"><span data-stu-id="40ffd-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="40ffd-168">_lpDestInterface が_ NULL に設定されている場合 **、DoCopyProps は** 値をMAPI_E_INVALID_PARAMETER。</span><span class="sxs-lookup"><span data-stu-id="40ffd-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="40ffd-169">_lpDestInterface_ を許容可能なインターフェイス識別子に設定し _、lpDestObj_ を無効なポインターに設定すると、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="40ffd-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="40ffd-170">ほとんどの場合、プロバイダーは失敗します。</span><span class="sxs-lookup"><span data-stu-id="40ffd-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="40ffd-171">宛先オブジェクトMAPI_NOREPLACEプロパティを上書きしない場合は、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="40ffd-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="40ffd-172">ソース オブジェクトに存在し、上書きされないコピー先オブジェクトのプロパティは削除または変更されません。</span><span class="sxs-lookup"><span data-stu-id="40ffd-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="40ffd-173">メッセージの受信者リストをコピーするには _、lpIncludeProps_ パラメーターが指すプロパティ タグ配列に **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="40ffd-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="40ffd-174">メッセージの添付ファイルをコピーするには、PR_MESSAGE_ATTACHMENTS **(** [PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="40ffd-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="40ffd-175">フォルダーまたはアドレス帳コンテナーの階層またはコンテンツ テーブルをコピーするには、プロパティ タグ配列に **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="40ffd-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="40ffd-176">フォルダーに関連付けられているコンテンツ テーブルを含めるには、配列に PR_FOLDER_ASSOCIATED_CONTENTS **(** [PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) プロパティを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="40ffd-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="40ffd-177">サブフォルダーがコピーまたは移動された場合 **、SPropTagArray** 構造で示されるプロパティの使用に関係なく、その内容はコピーまたは移動されます。</span><span class="sxs-lookup"><span data-stu-id="40ffd-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="40ffd-178">**DoCopyProps は** 、操作全体で発生するグローバル エラーと、1 つ以上のプロパティで発生する個々のエラーを報告します。</span><span class="sxs-lookup"><span data-stu-id="40ffd-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="40ffd-179">これらの個々のエラーは **、SPropProblemArray 構造体に入** れ込まれています。</span><span class="sxs-lookup"><span data-stu-id="40ffd-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="40ffd-180">プロパティの問題配列構造パラメーターに対して、有効なポインターではなく NULL を渡して、プロパティ レベルでエラー報告を抑制できます。</span><span class="sxs-lookup"><span data-stu-id="40ffd-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="40ffd-181">エラーに関する情報を受け取る場合は _、lppProblems_ パラメーターに有効な **SPropProblemArray** 構造体ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="40ffd-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="40ffd-182">**DoCopyProps は**、S_OKを返す場合は、構造体内の個々のプロパティで発生する可能性のあるエラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="40ffd-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="40ffd-183">**DoCopyProps が** エラーを返す場合 **、SPropProblemArray** 構造体に情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="40ffd-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="40ffd-184">代わりに [、IMAPISupport::GetLastError](imapisupport-getlasterror.md) メソッドを呼び出して、詳細なエラー情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="40ffd-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="40ffd-185">**DoCopyProps が** 関数を返S_OK [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、返される **SPropProblemArray** 構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="40ffd-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40ffd-186">関連項目</span><span class="sxs-lookup"><span data-stu-id="40ffd-186">See also</span></span>



[<span data-ttu-id="40ffd-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="40ffd-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="40ffd-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="40ffd-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="40ffd-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="40ffd-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="40ffd-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="40ffd-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="40ffd-191">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="40ffd-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="40ffd-192">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="40ffd-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="40ffd-193">PidTagFolderAssociatedContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="40ffd-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="40ffd-194">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="40ffd-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="40ffd-195">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="40ffd-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="40ffd-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="40ffd-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="40ffd-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="40ffd-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="40ffd-198">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="40ffd-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

