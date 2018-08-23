---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 074a806a710ce8c11adba815951c93c25d8cae7c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579257"
---
# <a name="imapimessagesitecopymessage"></a><span data-ttu-id="dadd8-103">IMAPIMessageSite::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="dadd8-103">IMAPIMessageSite::CopyMessage</span></span>

  
  
<span data-ttu-id="dadd8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dadd8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dadd8-105">現在のメッセージをフォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="dadd8-105">Copies the current message to a folder.</span></span>
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a><span data-ttu-id="dadd8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dadd8-106">Parameters</span></span>

 <span data-ttu-id="dadd8-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="dadd8-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="dadd8-108">[in]メッセージのコピー先フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="dadd8-108">[in] A pointer to the folder where the message is to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dadd8-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="dadd8-109">Return value</span></span>

<span data-ttu-id="dadd8-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="dadd8-110">S_OK</span></span> 
  
> <span data-ttu-id="dadd8-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="dadd8-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="dadd8-112">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="dadd8-112">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="dadd8-113">このメッセージのサイトでは、操作はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="dadd8-113">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dadd8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="dadd8-114">Remarks</span></span>

<span data-ttu-id="dadd8-115">フォーム オブジェクトは、現在のメッセージを新しいフォルダーにコピーするのには**IMAPIMessageSite::CopyMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dadd8-115">Form objects call the **IMAPIMessageSite::CopyMessage** method to copy the current message to a new folder.</span></span> <span data-ttu-id="dadd8-116">**CopyMessage**では、ユーザーに現在表示されているメッセージは変更されませんし、フォームを新しく作成したメッセージのインターフェイスは返されません。</span><span class="sxs-lookup"><span data-stu-id="dadd8-116">**CopyMessage** does not change the message currently being displayed to the user, and no interface for the newly created message is returned to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="dadd8-117">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="dadd8-117">Notes to implementers</span></span>

<span data-ttu-id="dadd8-118">**CopyMessage**メソッドの一般的な実装では、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="dadd8-118">A typical implementation of the **CopyMessage** method performs the following tasks:</span></span> 
  
1. <span data-ttu-id="dadd8-119">現在のメッセージにコピーするための新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="dadd8-119">Creates a new message for the current message to be copied to.</span></span>
    
2. <span data-ttu-id="dadd8-120">_PMessage_パラメーターおよび FALSE で、 _fSameAsLoad_パラメーターでの新しいメッセージへのポインターで[IPersistMessage::Save](ipersistmessage-save.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dadd8-120">Calls the [IPersistMessage::Save](ipersistmessage-save.md) method with a pointer to the new message in the  _pMessage_ parameter and FALSE in the  _fSameAsLoad_ parameter.</span></span> 
    
3. <span data-ttu-id="dadd8-121">_PMessage_パラメーターに NULL を渡して、 [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dadd8-121">Calls the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method, passing NULL in the  _pMessage_ parameter.</span></span> 
    
4. <span data-ttu-id="dadd8-122">新しいメッセージで、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dadd8-122">Calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the new message.</span></span> 
    
<span data-ttu-id="dadd8-123">フォームのサーバーに関連付けられているインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dadd8-123">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dadd8-124">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="dadd8-124">MFCMAPI reference</span></span>

<span data-ttu-id="dadd8-125">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="dadd8-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dadd8-126">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="dadd8-126">**File**</span></span>|<span data-ttu-id="dadd8-127">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="dadd8-127">**Function**</span></span>|<span data-ttu-id="dadd8-128">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="dadd8-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dadd8-129">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="dadd8-129">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="dadd8-130">CMyMAPIFormViewer::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="dadd8-130">CMyMAPIFormViewer::CopyMessage</span></span>  <br/> |<span data-ttu-id="dadd8-131">実装されていません。</span><span class="sxs-lookup"><span data-stu-id="dadd8-131">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dadd8-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="dadd8-132">See also</span></span>



[<span data-ttu-id="dadd8-133">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="dadd8-133">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="dadd8-134">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="dadd8-134">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="dadd8-135">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="dadd8-135">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="dadd8-136">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dadd8-136">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="dadd8-137">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="dadd8-137">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="dadd8-138">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="dadd8-138">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

