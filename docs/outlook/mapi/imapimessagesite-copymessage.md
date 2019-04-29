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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430001"
---
# <a name="imapimessagesitecopymessage"></a><span data-ttu-id="3cf3d-103">IMAPIMessageSite::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="3cf3d-103">IMAPIMessageSite::CopyMessage</span></span>

  
  
<span data-ttu-id="3cf3d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cf3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cf3d-105">現在のメッセージをフォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="3cf3d-105">Copies the current message to a folder.</span></span>
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a><span data-ttu-id="3cf3d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3cf3d-106">Parameters</span></span>

 <span data-ttu-id="3cf3d-107">_pfolderdestination_</span><span class="sxs-lookup"><span data-stu-id="3cf3d-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="3cf3d-108">順番メッセージがコピーされるフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3cf3d-108">[in] A pointer to the folder where the message is to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3cf3d-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="3cf3d-109">Return value</span></span>

<span data-ttu-id="3cf3d-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3cf3d-110">S_OK</span></span> 
  
> <span data-ttu-id="3cf3d-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="3cf3d-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3cf3d-112">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3cf3d-112">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="3cf3d-113">操作は、このメッセージサイトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3cf3d-113">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3cf3d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3cf3d-114">Remarks</span></span>

<span data-ttu-id="3cf3d-115">Form オブジェクトは**IMAPIMessageSite:: copymessage**メソッドを呼び出して、現在のメッセージを新しいフォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="3cf3d-115">Form objects call the **IMAPIMessageSite::CopyMessage** method to copy the current message to a new folder.</span></span> <span data-ttu-id="3cf3d-116">**copymessage**は、現在ユーザーに表示されているメッセージを変更しません。また、新しく作成されたメッセージのインターフェイスはフォームに返されません。</span><span class="sxs-lookup"><span data-stu-id="3cf3d-116">**CopyMessage** does not change the message currently being displayed to the user, and no interface for the newly created message is returned to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3cf3d-117">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="3cf3d-117">Notes to implementers</span></span>

<span data-ttu-id="3cf3d-118">**copymessage**メソッドの一般的な実装では、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="3cf3d-118">A typical implementation of the **CopyMessage** method performs the following tasks:</span></span> 
  
1. <span data-ttu-id="3cf3d-119">現在のメッセージをコピーする新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="3cf3d-119">Creates a new message for the current message to be copied to.</span></span>
    
2. <span data-ttu-id="3cf3d-120">[IPersistMessage:: Save](ipersistmessage-save.md)メソッドを呼び出して、 _pmessage_パラメーターに新しいメッセージへのポインターを指定し、 _fsameasload_パラメーターに FALSE を指定します。</span><span class="sxs-lookup"><span data-stu-id="3cf3d-120">Calls the [IPersistMessage::Save](ipersistmessage-save.md) method with a pointer to the new message in the  _pMessage_ parameter and FALSE in the  _fSameAsLoad_ parameter.</span></span> 
    
3. <span data-ttu-id="3cf3d-121">_pmessage_パラメーターに NULL を渡す[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3cf3d-121">Calls the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method, passing NULL in the  _pMessage_ parameter.</span></span> 
    
4. <span data-ttu-id="3cf3d-122">新しいメッセージに対して[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3cf3d-122">Calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the new message.</span></span> 
    
<span data-ttu-id="3cf3d-123">フォームサーバーに関連するインターフェイスの一覧については、「 [MAPI フォームインターフェイス](mapi-form-interfaces.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cf3d-123">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3cf3d-124">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="3cf3d-124">MFCMAPI reference</span></span>

<span data-ttu-id="3cf3d-125">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cf3d-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3cf3d-126">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="3cf3d-126">**File**</span></span>|<span data-ttu-id="3cf3d-127">**関数**</span><span class="sxs-lookup"><span data-stu-id="3cf3d-127">**Function**</span></span>|<span data-ttu-id="3cf3d-128">**コメント**</span><span class="sxs-lookup"><span data-stu-id="3cf3d-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3cf3d-129">MyMAPIFormViewer</span><span class="sxs-lookup"><span data-stu-id="3cf3d-129">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="3cf3d-130">cmymapiformviewer:: copymessage</span><span class="sxs-lookup"><span data-stu-id="3cf3d-130">CMyMAPIFormViewer::CopyMessage</span></span>  <br/> |<span data-ttu-id="3cf3d-131">実装されていません。</span><span class="sxs-lookup"><span data-stu-id="3cf3d-131">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3cf3d-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="3cf3d-132">See also</span></span>



[<span data-ttu-id="3cf3d-133">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="3cf3d-133">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="3cf3d-134">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="3cf3d-134">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="3cf3d-135">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="3cf3d-135">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="3cf3d-136">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3cf3d-136">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="3cf3d-137">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="3cf3d-137">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="3cf3d-138">MAPI フォームインターフェイス</span><span class="sxs-lookup"><span data-stu-id="3cf3d-138">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

