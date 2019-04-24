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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c14ccac0addbc1288e3507cf549344f75e69cc28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351080"
---
# <a name="imessagedeleteattach"></a><span data-ttu-id="7d0bf-103">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="7d0bf-103">IMessage::DeleteAttach</span></span>

  
  
<span data-ttu-id="7d0bf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d0bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d0bf-105">添付ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-105">Deletes an attachment.</span></span>
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7d0bf-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7d0bf-106">Parameters</span></span>

 <span data-ttu-id="7d0bf-107">_ulattachmentnum_</span><span class="sxs-lookup"><span data-stu-id="7d0bf-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="7d0bf-108">順番削除する添付ファイルのインデックス番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-108">[in] Index number of the attachment to delete.</span></span> <span data-ttu-id="7d0bf-109">これは、添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティの値です。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-109">This is the value for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="7d0bf-110">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="7d0bf-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="7d0bf-111">順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-111">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="7d0bf-112">_uluiparam_パラメーターは、 _ulflags_パラメーターで ATTACH_DIALOG フラグが設定されていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-112">The  _ulUIParam_ parameter is ignored unless the ATTACH_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="7d0bf-113">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="7d0bf-113">_lpProgress_</span></span>
  
> <span data-ttu-id="7d0bf-114">順番進行状況インジケーターを表示する progress オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-114">[in] Pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="7d0bf-115">_lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI progress オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator using the MAPI progress object implementation.</span></span> <span data-ttu-id="7d0bf-116">ATTACH_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-116">The  _lpProgress_ parameter is ignored unless the ATTACH_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="7d0bf-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7d0bf-117">_ulFlags_</span></span>
  
> <span data-ttu-id="7d0bf-118">順番ユーザーインターフェイスの表示を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-118">[in] Bitmask of flags that controls the display of a user interface.</span></span> <span data-ttu-id="7d0bf-119">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-119">The following flag can be set:</span></span>
    
<span data-ttu-id="7d0bf-120">ATTACH_DIALOG</span><span class="sxs-lookup"><span data-stu-id="7d0bf-120">ATTACH_DIALOG</span></span> 
  
> <span data-ttu-id="7d0bf-121">操作が続行されると、進行状況インジケーターの表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-121">Requests the display of a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d0bf-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="7d0bf-122">Return value</span></span>

<span data-ttu-id="7d0bf-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d0bf-123">S_OK</span></span> 
  
> <span data-ttu-id="7d0bf-124">添付ファイルが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-124">The attachment was successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d0bf-125">解説</span><span class="sxs-lookup"><span data-stu-id="7d0bf-125">Remarks</span></span>

<span data-ttu-id="7d0bf-126">**IMessage::D eleteattach**メソッドは、メッセージ内から添付ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-126">The **IMessage::DeleteAttach** method deletes an attachment from within a message.</span></span> 
  
<span data-ttu-id="7d0bf-127">削除された添付ファイルは、メッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されるまで完全に削除されません。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-127">A deleted attachment is not permanently deleted until the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7d0bf-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7d0bf-128">Notes to callers</span></span>

<span data-ttu-id="7d0bf-129">**deleteattach**を呼び出す前に、添付ファイルとその各ストリームの**IUnknown:: Release**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-129">Before calling **DeleteAttach**, call the **IUnknown::Release** method for the attachment and each of its streams.</span></span> 
  
<span data-ttu-id="7d0bf-130">添付ファイルの削除は時間がかかることがあるため、 **deleteattach**には進行状況インジケーターを表示するメカニズムが用意されています。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-130">Because deleting an attachment can be a lengthy process, **DeleteAttach** provides the mechanism that displays a progress indicator.</span></span> <span data-ttu-id="7d0bf-131">進行状況インジケーターの表示を要求するには、 [imapiprogress](imapiprogressiunknown.md)へのポインターを渡します: IUnknown 実装または NULL (実装されていない場合)。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-131">You can request the display of a progress indicator by passing a pointer to your [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implementation or NULL if you do not have an implementation.</span></span> <span data-ttu-id="7d0bf-132">_uluiparam_パラメーターでウィンドウハンドルを指定し、 _ulflags_パラメーターに ATTACH_DIALOG フラグも指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-132">You must also specify a window handle in the  _ulUIParam_ parameter and the ATTACH_DIALOG flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7d0bf-133">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="7d0bf-133">MFCMAPI reference</span></span>

<span data-ttu-id="7d0bf-134">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7d0bf-135">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="7d0bf-135">**File**</span></span>|<span data-ttu-id="7d0bf-136">**関数**</span><span class="sxs-lookup"><span data-stu-id="7d0bf-136">**Function**</span></span>|<span data-ttu-id="7d0bf-137">**コメント**</span><span class="sxs-lookup"><span data-stu-id="7d0bf-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7d0bf-138">AttachmentsDlg</span><span class="sxs-lookup"><span data-stu-id="7d0bf-138">AttachmentsDlg.cpp</span></span>  <br/> |<span data-ttu-id="7d0bf-139">CAttachmentsDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="7d0bf-139">CAttachmentsDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="7d0bf-140">mfcmapi は、 **IMessage::D eleteattach**メソッドを使用して、選択されている添付ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="7d0bf-140">MFCMAPI uses the **IMessage::DeleteAttach** method to delete the selected attachment.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d0bf-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="7d0bf-141">See also</span></span>



[<span data-ttu-id="7d0bf-142">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="7d0bf-142">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="7d0bf-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7d0bf-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


<span data-ttu-id="7d0bf-144">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="7d0bf-144">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

