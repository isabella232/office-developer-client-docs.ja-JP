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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c93e01b1e4621cddc4c98d528e5f5339cba21dae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800732"
---
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="89b23-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="89b23-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="89b23-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="89b23-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="89b23-105">オブジェクトの 1 つまたは複数のプロパティを別のオブジェクトを移動またはコピーします。</span><span class="sxs-lookup"><span data-stu-id="89b23-105">Copies or moves one or more properties of an object to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="89b23-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89b23-106">Parameters</span></span>

 <span data-ttu-id="89b23-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="89b23-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="89b23-108">[in]コピーまたは移動するプロパティを持つオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="89b23-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="89b23-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="89b23-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="89b23-110">[in]コピーまたは移動するにはプロパティを格納しているオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="89b23-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="89b23-111">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="89b23-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="89b23-112">[in]コピーまたは移動するにはプロパティを指定するプロパティ タグのカウント済み配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="89b23-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="89b23-113">_LpIncludeProps_パラメーターは、NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="89b23-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="89b23-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="89b23-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="89b23-115">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="89b23-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="89b23-116">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="89b23-116">_lpProgress_</span></span>
  
> <span data-ttu-id="89b23-117">[in]進行状況のインジケーターの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="89b23-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="89b23-118">_LpProgress_パラメーターに NULL が渡されると、MAPI 実装を使用して進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="89b23-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="89b23-119">_UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="89b23-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="89b23-120">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="89b23-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="89b23-121">[in]プロパティをコピーまたは移動を受信するオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="89b23-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="89b23-122">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="89b23-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="89b23-123">[in]コピーまたは移動先のプロパティを表示するオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="89b23-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="89b23-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="89b23-124">_ulFlags_</span></span>
  
> <span data-ttu-id="89b23-125">[in]コピーまたは移動操作の実行方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="89b23-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="89b23-126">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="89b23-126">The following flags can be set:</span></span>
    
<span data-ttu-id="89b23-127">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="89b23-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="89b23-128">進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="89b23-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="89b23-129">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="89b23-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="89b23-130">**DoCopyProps**は、コピー操作ではなく移動操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89b23-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="89b23-131">このフラグが設定されていない場合、 **DoCopyProps**は、コピー操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="89b23-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="89b23-132">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="89b23-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="89b23-133">コピー先オブジェクトの既存のプロパティを上書きしてはなりません。</span><span class="sxs-lookup"><span data-stu-id="89b23-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="89b23-134">このフラグが設定されていない場合、 **DoCopyProps**には、既存のプロパティが上書きされます。</span><span class="sxs-lookup"><span data-stu-id="89b23-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="89b23-135">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="89b23-135">_lppProblems_</span></span>
  
> <span data-ttu-id="89b23-136">[で [チェック アウト][SPropProblemArray](spropproblemarray.md)構造体へのポインターへのポインターの入力でそれ以外の場合、NULL、エラー情報の必要性を示すしません。</span><span class="sxs-lookup"><span data-stu-id="89b23-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="89b23-137">_LppProblems_が入力時に有効なポインターである場合は、 **DoCopyProps**は、1 つまたは複数のプロパティのコピーでエラーに関する詳細な情報を返します。</span><span class="sxs-lookup"><span data-stu-id="89b23-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="89b23-138">�߂�l</span><span class="sxs-lookup"><span data-stu-id="89b23-138">Return value</span></span>

<span data-ttu-id="89b23-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="89b23-139">S_OK</span></span> 
  
> <span data-ttu-id="89b23-140">プロパティは、コピーまたは移動されて正常にします。</span><span class="sxs-lookup"><span data-stu-id="89b23-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="89b23-141">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="89b23-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="89b23-142">先のオブジェクトのプロパティをコピーまたは移動を既にが存在して MAPI_NOREPLACE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="89b23-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="89b23-143">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="89b23-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="89b23-144">ソース オブジェクトには直接または間接的に目的のオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="89b23-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="89b23-145">重要な作業が実行された前に、この条件が検出された元とコピー先のオブジェクトを部分的に変更された可能性がありますので。</span><span class="sxs-lookup"><span data-stu-id="89b23-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="89b23-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="89b23-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="89b23-147">ソース オブジェクトでは、 _lpSrcInterface_パラメーターで指定されたインターフェイスはサポートされていないか、先のオブジェクトでは、 _lpDestInterface_パラメーターで指定されたインターフェイスはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="89b23-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="89b23-148">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="89b23-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="89b23-149">呼び出し元が十分なアクセス許可を持っているオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="89b23-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="89b23-150">目的のオブジェクトは、ソース オブジェクトと同じ場合、このエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="89b23-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="89b23-151">次の値が返される、 **SPropProblemArray**構造体には戻り値としてではなく**DoCopyProps**。</span><span class="sxs-lookup"><span data-stu-id="89b23-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="89b23-152">これらのエラーは、1 つのプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="89b23-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="89b23-153">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="89b23-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="89b23-154">か、MAPI_UNICODE フラグが設定された**DoCopyProps**は、Unicode をサポートしていませんまたは MAPI_UNICODE が設定されていないと**DoCopyProps**は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="89b23-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="89b23-155">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="89b23-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="89b23-156">コピー先オブジェクトの所有者によって計算される、読み取り専用プロパティであるために、呼び出し元がプロパティを変更できません。</span><span class="sxs-lookup"><span data-stu-id="89b23-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="89b23-157">このエラーは重大です。呼び出し元は、コピー操作を続行を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89b23-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="89b23-158">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="89b23-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="89b23-159">プロパティの型が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="89b23-159">The property type is invalid.</span></span>
    
<span data-ttu-id="89b23-160">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="89b23-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="89b23-161">プロパティの型は、呼び出し元が要求する型ではありません。</span><span class="sxs-lookup"><span data-stu-id="89b23-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89b23-162">注釈</span><span class="sxs-lookup"><span data-stu-id="89b23-162">Remarks</span></span>

<span data-ttu-id="89b23-163">メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::DoCopyProps**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="89b23-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="89b23-164">メッセージ ストア プロバイダーは、そのフォルダーとメッセージの[IMAPIProp::CopyProps](imapiprop-copyprops.md)メソッドを実装するために**DoCopyProps**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="89b23-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="89b23-165">**DoCopyProps**にコピーまたは移動のプロパティで_lpIncludeProps_で指定されたプロパティ タグ配列を識別し、 _lpSrcObj_が指すオブジェクトに存在します。</span><span class="sxs-lookup"><span data-stu-id="89b23-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="89b23-166">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="89b23-166">Notes to callers</span></span>

<span data-ttu-id="89b23-167">_LpSrcInterface_および_lpDestInterface_パラメーターが同じインターフェイス識別子、および、 _lpSrcObj_および_lpDestObj_パラメーターを含める必要があります、2 つのメッセージなど、同じ種類のオブジェクト間でプロパティをコピーすると、同じ種類のオブジェクトをポイントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="89b23-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="89b23-168">_LpDestInterface_は、NULL に設定されている場合、 **DoCopyProps**は MAPI_E_INVALID_PARAMETER を返します。</span><span class="sxs-lookup"><span data-stu-id="89b23-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="89b23-169">許容可能なインタ フェース識別子は無効なポインターをセット_lpDestObj_に_lpDestInterface_を設定した場合、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="89b23-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="89b23-170">ほとんどの場合、プロバイダーは失敗します。</span><span class="sxs-lookup"><span data-stu-id="89b23-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="89b23-171">上書き先のオブジェクトのプロパティのいずれかしない場合は、MAPI_NOREPLACE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="89b23-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="89b23-172">ソース オブジェクト内に存在し、上書きされないプロパティを目的のオブジェクトには、削除したり、変更するはありません。</span><span class="sxs-lookup"><span data-stu-id="89b23-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="89b23-173">メッセージの受信者のリストをコピーするのには、 _lpIncludeProps_パラメーターで指定されたプロパティ タグ配列の**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="89b23-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="89b23-174">メッセージの添付ファイルをコピーするには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="89b23-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="89b23-175">フォルダーまたはアドレス帳コンテナーの階層構造または内容のテーブルをコピーするには、プロパティ タグ配列の**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) を含めます。</span><span class="sxs-lookup"><span data-stu-id="89b23-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="89b23-176">フォルダーの内容を関連するテーブルを含めるには、 **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) のプロパティを配列に指定します。</span><span class="sxs-lookup"><span data-stu-id="89b23-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="89b23-177">サブフォルダーは、コピーまたは移動は場合、その内容がコピーまたは、 **SPropTagArray**構造体で示されているプロパティの使用に関係なく、完全に移動します。</span><span class="sxs-lookup"><span data-stu-id="89b23-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="89b23-178">**DoCopyProps**は、グローバル エラーの全体としての操作で発生して、プロパティのいずれかで発生する個々 のエラーを報告します。</span><span class="sxs-lookup"><span data-stu-id="89b23-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="89b23-179">これらの個々 のエラーは、 **SPropProblemArray**構造体に配置されます。</span><span class="sxs-lookup"><span data-stu-id="89b23-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="89b23-180">プロパティ問題配列構造体パラメーターに有効なポインターではなく NULL を渡すことにより、プロパティ レベルでレポートのエラーを抑制できます。</span><span class="sxs-lookup"><span data-stu-id="89b23-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="89b23-181">エラーに関する情報を受信する場合は、 _lppProblems_パラメーターに有効な**SPropProblemArray**構造体のポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="89b23-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="89b23-182">**DoCopyProps**に S_OK が返されるときは、構造内の個々 のプロパティを持つ可能性のあるエラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="89b23-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="89b23-183">**DoCopyProps**にエラーが返されるとき、 **SPropProblemArray**構造体の情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="89b23-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="89b23-184">代わりに、詳細なエラー情報を取得するために[IMAPISupport::GetLastError](imapisupport-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="89b23-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="89b23-185">**DoCopyProps**では、S_OK が返された場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数の呼び出しによって返された**SPropProblemArray**構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="89b23-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="89b23-186">関連項目</span><span class="sxs-lookup"><span data-stu-id="89b23-186">See also</span></span>



[<span data-ttu-id="89b23-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="89b23-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="89b23-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="89b23-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="89b23-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="89b23-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="89b23-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="89b23-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="89b23-191">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="89b23-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="89b23-192">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="89b23-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="89b23-193">PidTagFolderAssociatedContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="89b23-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="89b23-194">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="89b23-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="89b23-195">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="89b23-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="89b23-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="89b23-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="89b23-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="89b23-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="89b23-198">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="89b23-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

