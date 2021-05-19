---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: efa5d60098fd5f16328669249a8445a124d9878b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434089"
---
# <a name="imsgstoresetreceivefolder"></a><span data-ttu-id="8c625-103">IMsgStore::SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="8c625-103">IMsgStore::SetReceiveFolder</span></span>

  
  
<span data-ttu-id="8c625-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c625-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c625-105">特定のメッセージ クラスの受信メッセージの宛先としてフォルダーを確立します。</span><span class="sxs-lookup"><span data-stu-id="8c625-105">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="8c625-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8c625-106">Parameters</span></span>

 <span data-ttu-id="8c625-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="8c625-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="8c625-108">[in]新しい受信フォルダーに関連付けるメッセージ クラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8c625-108">[in] A pointer to the message class that is to be associated with the new receive folder.</span></span> <span data-ttu-id="8c625-109">_lpszMessageClass_ パラメーターが NULL または空の文字列に設定されている場合 **、SetReceiveFolder** はメッセージ ストアの既定の受信フォルダーを設定します。</span><span class="sxs-lookup"><span data-stu-id="8c625-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **SetReceiveFolder** sets the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="8c625-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8c625-110">_ulFlags_</span></span>
  
> <span data-ttu-id="8c625-111">[in]渡された文字列内のテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8c625-111">[in] A bitmask of flags that controls the type of the text in the passed-in strings.</span></span> <span data-ttu-id="8c625-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8c625-112">The following flag can be set:</span></span>
    
<span data-ttu-id="8c625-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8c625-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8c625-114">メッセージ クラスの文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="8c625-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="8c625-115">メッセージ クラスMAPI_UNICODEが設定されていない場合、メッセージ クラス文字列は ANSI 形式です。</span><span class="sxs-lookup"><span data-stu-id="8c625-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="8c625-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8c625-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="8c625-117">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="8c625-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8c625-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8c625-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="8c625-119">[in]受信フォルダーとして確立するフォルダーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8c625-119">[in] A pointer to the entry identifier of the folder to establish as the receive folder.</span></span> <span data-ttu-id="8c625-120">_lpEntryID_ パラメーターが NULL に設定されている場合 **、SetReceiveFolder** は現在の受信フォルダーをメッセージ ストアの既定値に置き換える。</span><span class="sxs-lookup"><span data-stu-id="8c625-120">If the  _lpEntryID_ parameter is set to NULL, **SetReceiveFolder** replaces the current receive folder with the message store's default.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8c625-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="8c625-121">Return value</span></span>

<span data-ttu-id="8c625-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="8c625-122">S_OK</span></span> 
  
> <span data-ttu-id="8c625-123">受信フォルダーが正常に確立されました。</span><span class="sxs-lookup"><span data-stu-id="8c625-123">A receive folder was successfully established.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8c625-124">注釈</span><span class="sxs-lookup"><span data-stu-id="8c625-124">Remarks</span></span>

<span data-ttu-id="8c625-125">**IMsgStore::SetReceiveFolder** メソッドは、特定のメッセージ クラスの受信フォルダーを設定または変更します。</span><span class="sxs-lookup"><span data-stu-id="8c625-125">The **IMsgStore::SetReceiveFolder** method sets or changes the receive folder for a particular message class.</span></span> <span data-ttu-id="8c625-126">**SetReceiveFolder** を使用すると、クライアントは、連続する呼び出しを使用して、定義されたメッセージ クラスごとに異なる受信フォルダーを指定するか、複数のメッセージ クラスの受信メッセージがすべて同じフォルダーに移動することを指定できます。</span><span class="sxs-lookup"><span data-stu-id="8c625-126">With **SetReceiveFolder**, a client can, by using successive calls, specify a different receive folder for each defined message class or specify that incoming messages for multiple message classes all go to the same folder.</span></span> <span data-ttu-id="8c625-127">たとえば、クライアントは独自のクラスのメッセージを独自のフォルダーに到着できます。</span><span class="sxs-lookup"><span data-stu-id="8c625-127">For example, a client can have its own class of messages arrive in its own folder.</span></span> <span data-ttu-id="8c625-128">FAX アプリケーションは、ストア プロバイダーが受信 FAX を置く 1 つのフォルダーと、プロバイダーが送信 FAX を置く別のフォルダーを指定できます。</span><span class="sxs-lookup"><span data-stu-id="8c625-128">A fax application can designate one folder in which the store provider puts incoming faxes and another folder in which the provider puts outgoing faxes.</span></span>
  
<span data-ttu-id="8c625-129">**SetReceiveFolder** の呼び出し中にエラーが発生した場合、受信フォルダーの設定は変更されません。</span><span class="sxs-lookup"><span data-stu-id="8c625-129">If an error occurs during the call to **SetReceiveFolder**, the receive folder setting remains unchanged.</span></span> 
  
<span data-ttu-id="8c625-130">**SetReceiveFolder** が _lpEntryID_ を NULL に設定して受信フォルダーの設定を変更すると、既定の受信フォルダーを設定する必要がある場合 **、SetReceiveFolder** は、指定されたメッセージ クラスに既存の設定が存在しない場合でも、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="8c625-130">If **SetReceiveFolder** changes the receive folder setting with  _lpEntryID_ set to NULL, indicating that the default receive folder should be set, **SetReceiveFolder** returns S_OK even if there was no existing setting for the indicated message class.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8c625-131">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="8c625-131">MFCMAPI reference</span></span>

<span data-ttu-id="8c625-132">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c625-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8c625-133">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="8c625-133">**File**</span></span>|<span data-ttu-id="8c625-134">**関数**</span><span class="sxs-lookup"><span data-stu-id="8c625-134">**Function**</span></span>|<span data-ttu-id="8c625-135">**コメント**</span><span class="sxs-lookup"><span data-stu-id="8c625-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8c625-136">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="8c625-136">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="8c625-137">CMsgStoreDlg::OnSetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="8c625-137">CMsgStoreDlg::OnSetReceiveFolder</span></span>  <br/> |<span data-ttu-id="8c625-138">MFCMAPI は **、IMsgStore::SetReceiveFolder** メソッドを使用して、フォルダーを特定のメッセージ クラスの受信フォルダーとして設定します。</span><span class="sxs-lookup"><span data-stu-id="8c625-138">MFCMAPI uses the **IMsgStore::SetReceiveFolder** method to set a folder as the receive folder for a particular message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8c625-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c625-139">See also</span></span>



[<span data-ttu-id="8c625-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8c625-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="8c625-141">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="8c625-141">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

