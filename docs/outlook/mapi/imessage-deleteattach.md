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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 93f264cc91118e40f7a2869d29e7e53d404ae381
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800897"
---
# <a name="imessagedeleteattach"></a><span data-ttu-id="ee5d2-103">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="ee5d2-103">IMessage::DeleteAttach</span></span>

  
  
<span data-ttu-id="ee5d2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee5d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee5d2-105">添付ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-105">Deletes an attachment.</span></span>
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ee5d2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ee5d2-106">Parameters</span></span>

 <span data-ttu-id="ee5d2-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="ee5d2-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="ee5d2-108">[in]削除する添付ファイルのインデックス番号です。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-108">[in] Index number of the attachment to delete.</span></span> <span data-ttu-id="ee5d2-109">これは、添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のプロパティの値です。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-109">This is the value for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="ee5d2-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ee5d2-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="ee5d2-111">[in]すべてのダイアログ ボックスの親ウィンドウまたは windows のこのメソッドは、表示を処理します。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-111">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="ee5d2-112">_UlFlags_パラメーターに ATTACH_DIALOG フラグが設定されていない限り、 _ulUIParam_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-112">The  _ulUIParam_ parameter is ignored unless the ATTACH_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="ee5d2-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="ee5d2-113">_lpProgress_</span></span>
  
> <span data-ttu-id="ee5d2-114">[in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-114">[in] Pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="ee5d2-115">_LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーには、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator using the MAPI progress object implementation.</span></span> <span data-ttu-id="ee5d2-116">_UlFlags_に ATTACH_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-116">The  _lpProgress_ parameter is ignored unless the ATTACH_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="ee5d2-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee5d2-117">_ulFlags_</span></span>
  
> <span data-ttu-id="ee5d2-118">[in]ユーザー インターフェイスの表示を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-118">[in] Bitmask of flags that controls the display of a user interface.</span></span> <span data-ttu-id="ee5d2-119">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-119">The following flag can be set:</span></span>
    
<span data-ttu-id="ee5d2-120">ATTACH_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ee5d2-120">ATTACH_DIALOG</span></span> 
  
> <span data-ttu-id="ee5d2-121">操作の進行中は、進行状況インジケーターの表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-121">Requests the display of a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ee5d2-122">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ee5d2-122">Return value</span></span>

<span data-ttu-id="ee5d2-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee5d2-123">S_OK</span></span> 
  
> <span data-ttu-id="ee5d2-124">添付ファイルが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-124">The attachment was successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee5d2-125">備考</span><span class="sxs-lookup"><span data-stu-id="ee5d2-125">Remarks</span></span>

<span data-ttu-id="ee5d2-126">**IMessage::DeleteAttach**メソッドは、メッセージ内から添付ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-126">The **IMessage::DeleteAttach** method deletes an attachment from within a message.</span></span> 
  
<span data-ttu-id="ee5d2-127">メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されるまで、削除された添付ファイルは完全に削除されません。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-127">A deleted attachment is not permanently deleted until the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ee5d2-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ee5d2-128">Notes to callers</span></span>

<span data-ttu-id="ee5d2-129">**DeleteAttach**を呼び出す前に、添付ファイルとそのストリームのそれぞれ**が**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-129">Before calling **DeleteAttach**, call the **IUnknown::Release** method for the attachment and each of its streams.</span></span> 
  
<span data-ttu-id="ee5d2-130">添付ファイルを削除できますが、手間がかかりますので、 **DeleteAttach**は進行状況インジケーターを表示するメカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-130">Because deleting an attachment can be a lengthy process, **DeleteAttach** provides the mechanism that displays a progress indicator.</span></span> <span data-ttu-id="ee5d2-131">ポインターを渡すことによって、進行状況インジケーターの表示を要求することができます、 [IMAPIProgress: IUnknown](imapiprogressiunknown.md)実装、または NULL の場合は、実装する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-131">You can request the display of a progress indicator by passing a pointer to your [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implementation or NULL if you do not have an implementation.</span></span> <span data-ttu-id="ee5d2-132">_UlUIParam_パラメーターと、ATTACH_DIALOG のフラグ、 _ulFlags_パラメーターにウィンドウ ハンドルを指定することもする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-132">You must also specify a window handle in the  _ulUIParam_ parameter and the ATTACH_DIALOG flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ee5d2-133">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ee5d2-133">MFCMAPI reference</span></span>

<span data-ttu-id="ee5d2-134">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ee5d2-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ee5d2-135">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ee5d2-135">**File**</span></span>|<span data-ttu-id="ee5d2-136">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ee5d2-136">**Function**</span></span>|<span data-ttu-id="ee5d2-137">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ee5d2-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ee5d2-138">AttachmentsDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ee5d2-138">AttachmentsDlg.cpp</span></span>  <br/> |<span data-ttu-id="ee5d2-139">CAttachmentsDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="ee5d2-139">CAttachmentsDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="ee5d2-140">MFCMAPI では、 **IMessage::DeleteAttach**メソッドを使用して、選択した添付ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="ee5d2-140">MFCMAPI uses the **IMessage::DeleteAttach** method to delete the selected attachment.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee5d2-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee5d2-141">See also</span></span>



[<span data-ttu-id="ee5d2-142">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="ee5d2-142">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="ee5d2-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ee5d2-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


<span data-ttu-id="ee5d2-144">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ee5d2-144">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

