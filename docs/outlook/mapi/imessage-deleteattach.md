---
title: IMessageDeleteAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c14ccac0addbc1288e3507cf549344f75e69cc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430708"
---
# <a name="imessagedeleteattach"></a><span data-ttu-id="431ad-103">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="431ad-103">IMessage::DeleteAttach</span></span>

  
  
<span data-ttu-id="431ad-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="431ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="431ad-105">添付ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="431ad-105">Deletes an attachment.</span></span>
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="431ad-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="431ad-106">Parameters</span></span>

 <span data-ttu-id="431ad-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="431ad-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="431ad-108">[in]削除する添付ファイルのインデックス番号。</span><span class="sxs-lookup"><span data-stu-id="431ad-108">[in] Index number of the attachment to delete.</span></span> <span data-ttu-id="431ad-109">これは、添付ファイルのプロパティ [(PidTagAttachNumber)](pidtagattachnumber-canonical-property.md)**プロパティPR_ATTACH_NUM** 値です。</span><span class="sxs-lookup"><span data-stu-id="431ad-109">This is the value for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="431ad-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="431ad-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="431ad-111">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウを処理します。</span><span class="sxs-lookup"><span data-stu-id="431ad-111">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="431ad-112">_ulUIParam_ パラメーターは _、ulFlags_ パラメーター ATTACH_DIALOGフラグが設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="431ad-112">The  _ulUIParam_ parameter is ignored unless the ATTACH_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="431ad-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="431ad-113">_lpProgress_</span></span>
  
> <span data-ttu-id="431ad-114">[in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="431ad-114">[in] Pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="431ad-115">_lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="431ad-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator using the MAPI progress object implementation.</span></span> <span data-ttu-id="431ad-116">_lpProgress パラメーター_ は _、ulFlags_ で ATTACH_DIALOGフラグが設定されていない限り無視されます。</span><span class="sxs-lookup"><span data-stu-id="431ad-116">The  _lpProgress_ parameter is ignored unless the ATTACH_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="431ad-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="431ad-117">_ulFlags_</span></span>
  
> <span data-ttu-id="431ad-118">[in]ユーザー インターフェイスの表示を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="431ad-118">[in] Bitmask of flags that controls the display of a user interface.</span></span> <span data-ttu-id="431ad-119">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="431ad-119">The following flag can be set:</span></span>
    
<span data-ttu-id="431ad-120">ATTACH_DIALOG</span><span class="sxs-lookup"><span data-stu-id="431ad-120">ATTACH_DIALOG</span></span> 
  
> <span data-ttu-id="431ad-121">操作が進むにつれて進行状況インジケーターの表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="431ad-121">Requests the display of a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="431ad-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="431ad-122">Return value</span></span>

<span data-ttu-id="431ad-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="431ad-123">S_OK</span></span> 
  
> <span data-ttu-id="431ad-124">添付ファイルが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="431ad-124">The attachment was successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="431ad-125">注釈</span><span class="sxs-lookup"><span data-stu-id="431ad-125">Remarks</span></span>

<span data-ttu-id="431ad-126">**IMessage::D eleteAttach** メソッドは、メッセージ内から添付ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="431ad-126">The **IMessage::DeleteAttach** method deletes an attachment from within a message.</span></span> 
  
<span data-ttu-id="431ad-127">メッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドが呼び出されるまで、削除された添付ファイルは完全に削除されません。</span><span class="sxs-lookup"><span data-stu-id="431ad-127">A deleted attachment is not permanently deleted until the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="431ad-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="431ad-128">Notes to callers</span></span>

<span data-ttu-id="431ad-129">**DeleteAttach を呼び出** す前に、添付ファイルとそのストリームの **IUnknown::Release** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="431ad-129">Before calling **DeleteAttach**, call the **IUnknown::Release** method for the attachment and each of its streams.</span></span> 
  
<span data-ttu-id="431ad-130">添付ファイルの削除は長いプロセスになる可能性があるから **、DeleteAttach は** 進行状況インジケーターを表示するメカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="431ad-130">Because deleting an attachment can be a lengthy process, **DeleteAttach** provides the mechanism that displays a progress indicator.</span></span> <span data-ttu-id="431ad-131">[IMAPIProgress : IUnknown](imapiprogressiunknown.md)実装または実装がない場合は NULL にポインターを渡して進行状況インジケーターの表示を要求できます。</span><span class="sxs-lookup"><span data-stu-id="431ad-131">You can request the display of a progress indicator by passing a pointer to your [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implementation or NULL if you do not have an implementation.</span></span> <span data-ttu-id="431ad-132">また、ulUIParam パラメーターでウィンドウ ハンドルを指定し  _、ulFlags_ パラメーター ATTACH_DIALOGフラグ  _を指定する必要_ があります。</span><span class="sxs-lookup"><span data-stu-id="431ad-132">You must also specify a window handle in the  _ulUIParam_ parameter and the ATTACH_DIALOG flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="431ad-133">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="431ad-133">MFCMAPI reference</span></span>

<span data-ttu-id="431ad-134">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="431ad-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="431ad-135">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="431ad-135">**File**</span></span>|<span data-ttu-id="431ad-136">**関数**</span><span class="sxs-lookup"><span data-stu-id="431ad-136">**Function**</span></span>|<span data-ttu-id="431ad-137">**コメント**</span><span class="sxs-lookup"><span data-stu-id="431ad-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="431ad-138">AttachmentsDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="431ad-138">AttachmentsDlg.cpp</span></span>  <br/> |<span data-ttu-id="431ad-139">CAttachmentsDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="431ad-139">CAttachmentsDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="431ad-140">MFCMAPI は **、IMessage::D eleteAttach** メソッドを使用して、選択した添付ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="431ad-140">MFCMAPI uses the **IMessage::DeleteAttach** method to delete the selected attachment.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="431ad-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="431ad-141">See also</span></span>



[<span data-ttu-id="431ad-142">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="431ad-142">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="431ad-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="431ad-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


<span data-ttu-id="431ad-144">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="431ad-144">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

