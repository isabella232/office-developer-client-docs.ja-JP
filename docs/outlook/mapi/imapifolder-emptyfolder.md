---
title: imapifolderemptyfolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280107"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="14631-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="14631-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="14631-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14631-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14631-105">フォルダー自体を削除せずに、フォルダーからすべてのメッセージとサブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="14631-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="14631-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14631-106">Parameters</span></span>

 <span data-ttu-id="14631-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="14631-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="14631-108">順番進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="14631-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="14631-109">_uluiparam_パラメーターは、 _ulflags_パラメーターで FOLDER_DIALOG フラグが設定されていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="14631-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="14631-110">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="14631-110">_lpProgress_</span></span>
  
> <span data-ttu-id="14631-111">順番進行状況インジケーターを表示する progress オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="14631-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="14631-112">_lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="14631-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="14631-113">FOLDER_DIALOG フラグが_ulflags_パラメーターで設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="14631-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="14631-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="14631-114">_ulFlags_</span></span>
  
> <span data-ttu-id="14631-115">順番フォルダーを空にする方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="14631-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="14631-116">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="14631-116">The following flags can be set:</span></span>
    
<span data-ttu-id="14631-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="14631-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="14631-118">関連付けられたコンテンツを含むメッセージを含むサブフォルダーを含む、すべてのサブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="14631-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="14631-119">DEL_ASSOCIATED フラグは、呼び出しが作用する最上位のフォルダーに対してのみ意味があります。</span><span class="sxs-lookup"><span data-stu-id="14631-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="14631-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="14631-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="14631-121">削除されたものを含むすべてのメッセージを完全に削除します。</span><span class="sxs-lookup"><span data-stu-id="14631-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="14631-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="14631-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="14631-123">操作の進行中に進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="14631-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="14631-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="14631-124">Return value</span></span>

<span data-ttu-id="14631-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="14631-125">S_OK</span></span> 
  
> <span data-ttu-id="14631-126">フォルダーが正常に空にされました。</span><span class="sxs-lookup"><span data-stu-id="14631-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="14631-127">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="14631-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="14631-128">呼び出しは成功しましたが、フォルダーが完全に空になっていませんでした。</span><span class="sxs-lookup"><span data-stu-id="14631-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="14631-129">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="14631-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="14631-130">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="14631-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="14631-131">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="14631-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="14631-132">解説</span><span class="sxs-lookup"><span data-stu-id="14631-132">Remarks</span></span>

<span data-ttu-id="14631-133">**imapifolder:: emptyfolder**メソッドは、フォルダー自体を削除せずに、フォルダーの内容をすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="14631-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="14631-134">**emptyfolder**を呼び出している間、送信されたメッセージは削除されません。</span><span class="sxs-lookup"><span data-stu-id="14631-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="14631-135">フォルダーに関連付けられたコンテンツには、ビュー、ルール、カスタムフォーム、およびカスタムソリューションストレージを記述するために使用されるメッセージが含まれます。また、フォーム定義を含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="14631-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="14631-136">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="14631-136">Notes to implementers</span></span>

<span data-ttu-id="14631-137">送信されたフォルダー内のメッセージに対して[IMsgStore:: abortsubmit](imsgstore-abortsubmit.md)メソッドを呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="14631-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="14631-138">送信されたメッセージは削除されません。</span><span class="sxs-lookup"><span data-stu-id="14631-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="14631-139">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="14631-139">Notes to callers</span></span>

<span data-ttu-id="14631-140">これらの戻り値は、次の条件に当てはまることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="14631-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="14631-141">**Condition**</span><span class="sxs-lookup"><span data-stu-id="14631-141">**Condition**</span></span>|<span data-ttu-id="14631-142">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="14631-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="14631-143">**emptyfolder**は、フォルダーを正常に空にしました。</span><span class="sxs-lookup"><span data-stu-id="14631-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="14631-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="14631-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="14631-145">**emptyfolder**はフォルダーを完全に空にすることができませんでした。</span><span class="sxs-lookup"><span data-stu-id="14631-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="14631-146">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="14631-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="14631-147">**emptyfolder**を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="14631-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="14631-148">任意のエラー値</span><span class="sxs-lookup"><span data-stu-id="14631-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="14631-149">**emptyfolder**を完了できない場合は、作業が行われていないことを前提としていません。</span><span class="sxs-lookup"><span data-stu-id="14631-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="14631-150">**emptyfolder**は、エラーが発生する前にフォルダーの内容の一部を削除することができた可能性があります。</span><span class="sxs-lookup"><span data-stu-id="14631-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="14631-151">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="14631-151">MFCMAPI reference</span></span>

<span data-ttu-id="14631-152">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="14631-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="14631-153">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="14631-153">**File**</span></span>|<span data-ttu-id="14631-154">**関数**</span><span class="sxs-lookup"><span data-stu-id="14631-154">**Function**</span></span>|<span data-ttu-id="14631-155">**コメント**</span><span class="sxs-lookup"><span data-stu-id="14631-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="14631-156">MsgStoreDlg</span><span class="sxs-lookup"><span data-stu-id="14631-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="14631-157">CMsgStoreDlg:: onemptyfolder</span><span class="sxs-lookup"><span data-stu-id="14631-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="14631-158">mfcmapi は、 **imapifolder:: emptyfolder**メソッドを使用して、指定されたフォルダーの内容を削除します。</span><span class="sxs-lookup"><span data-stu-id="14631-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14631-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="14631-159">See also</span></span>



[<span data-ttu-id="14631-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="14631-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="14631-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="14631-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="14631-162">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="14631-162">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="14631-163">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="14631-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

