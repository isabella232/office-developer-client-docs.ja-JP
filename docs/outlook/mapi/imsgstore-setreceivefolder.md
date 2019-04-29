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
# <a name="imsgstoresetreceivefolder"></a><span data-ttu-id="bae3b-103">IMsgStore::SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="bae3b-103">IMsgStore::SetReceiveFolder</span></span>

  
  
<span data-ttu-id="bae3b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bae3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bae3b-105">特定のメッセージクラスの受信メッセージの送信先としてフォルダーを確立します。</span><span class="sxs-lookup"><span data-stu-id="bae3b-105">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="bae3b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bae3b-106">Parameters</span></span>

 <span data-ttu-id="bae3b-107">_lpszmessageclass_</span><span class="sxs-lookup"><span data-stu-id="bae3b-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="bae3b-108">順番新しい受信フォルダーに関連付けられるメッセージクラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bae3b-108">[in] A pointer to the message class that is to be associated with the new receive folder.</span></span> <span data-ttu-id="bae3b-109">_lpszmessageclass_パラメーターが NULL または空の文字列に設定されている場合、 **setreceivefolder**は、メッセージストアの既定の受信フォルダーを設定します。</span><span class="sxs-lookup"><span data-stu-id="bae3b-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **SetReceiveFolder** sets the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="bae3b-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bae3b-110">_ulFlags_</span></span>
  
> <span data-ttu-id="bae3b-111">順番渡された文字列内のテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="bae3b-111">[in] A bitmask of flags that controls the type of the text in the passed-in strings.</span></span> <span data-ttu-id="bae3b-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="bae3b-112">The following flag can be set:</span></span>
    
<span data-ttu-id="bae3b-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bae3b-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bae3b-114">メッセージクラスの文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="bae3b-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="bae3b-115">MAPI_UNICODE フラグが設定されていない場合、メッセージクラスの文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="bae3b-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="bae3b-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="bae3b-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="bae3b-117">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="bae3b-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="bae3b-118">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="bae3b-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="bae3b-119">順番受信フォルダーとして確立するフォルダーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bae3b-119">[in] A pointer to the entry identifier of the folder to establish as the receive folder.</span></span> <span data-ttu-id="bae3b-120">_lpentryid_パラメーターが NULL に設定されている場合、 **setreceivefolder**は現在の受信フォルダーをメッセージストアの既定値で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="bae3b-120">If the  _lpEntryID_ parameter is set to NULL, **SetReceiveFolder** replaces the current receive folder with the message store's default.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bae3b-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="bae3b-121">Return value</span></span>

<span data-ttu-id="bae3b-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="bae3b-122">S_OK</span></span> 
  
> <span data-ttu-id="bae3b-123">受信フォルダーが正常に確立されました。</span><span class="sxs-lookup"><span data-stu-id="bae3b-123">A receive folder was successfully established.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bae3b-124">注釈</span><span class="sxs-lookup"><span data-stu-id="bae3b-124">Remarks</span></span>

<span data-ttu-id="bae3b-125">**IMsgStore:: setreceivefolder**メソッドは、特定のメッセージクラスの受信フォルダーを設定または変更します。</span><span class="sxs-lookup"><span data-stu-id="bae3b-125">The **IMsgStore::SetReceiveFolder** method sets or changes the receive folder for a particular message class.</span></span> <span data-ttu-id="bae3b-126">**setreceivefolder**では、クライアントは、連続した呼び出しを使用して、定義された各メッセージクラスに対して異なる受信フォルダーを指定したり、複数のメッセージクラスの受信メッセージをすべて同じフォルダーに移動するように指定したりできます。</span><span class="sxs-lookup"><span data-stu-id="bae3b-126">With **SetReceiveFolder**, a client can, by using successive calls, specify a different receive folder for each defined message class or specify that incoming messages for multiple message classes all go to the same folder.</span></span> <span data-ttu-id="bae3b-127">たとえば、クライアントは独自のフォルダーにメッセージの独自のクラスを受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="bae3b-127">For example, a client can have its own class of messages arrive in its own folder.</span></span> <span data-ttu-id="bae3b-128">fax アプリケーションは、受信 fax を格納する1つのフォルダーと、プロバイダーが発信 fax を配置する別のフォルダーを指定できます。</span><span class="sxs-lookup"><span data-stu-id="bae3b-128">A fax application can designate one folder in which the store provider puts incoming faxes and another folder in which the provider puts outgoing faxes.</span></span>
  
<span data-ttu-id="bae3b-129">**setreceivefolder**の呼び出し中にエラーが発生しても、受信フォルダーの設定は変わりません。</span><span class="sxs-lookup"><span data-stu-id="bae3b-129">If an error occurs during the call to **SetReceiveFolder**, the receive folder setting remains unchanged.</span></span> 
  
<span data-ttu-id="bae3b-130">**setreceivefolder**で、 _lpentryid_が NULL に設定されている受信フォルダーの設定を変更すると、既定の受信フォルダーが設定されていることを示します。 **setreceivefolder**は、指定されたメッセージクラス。</span><span class="sxs-lookup"><span data-stu-id="bae3b-130">If **SetReceiveFolder** changes the receive folder setting with  _lpEntryID_ set to NULL, indicating that the default receive folder should be set, **SetReceiveFolder** returns S_OK even if there was no existing setting for the indicated message class.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bae3b-131">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="bae3b-131">MFCMAPI reference</span></span>

<span data-ttu-id="bae3b-132">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bae3b-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bae3b-133">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="bae3b-133">**File**</span></span>|<span data-ttu-id="bae3b-134">**関数**</span><span class="sxs-lookup"><span data-stu-id="bae3b-134">**Function**</span></span>|<span data-ttu-id="bae3b-135">**コメント**</span><span class="sxs-lookup"><span data-stu-id="bae3b-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bae3b-136">MsgStoreDlg</span><span class="sxs-lookup"><span data-stu-id="bae3b-136">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="bae3b-137">CMsgStoreDlg:: OnSetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="bae3b-137">CMsgStoreDlg::OnSetReceiveFolder</span></span>  <br/> |<span data-ttu-id="bae3b-138">mfcmapi は、 **IMsgStore:: setreceivefolder**メソッドを使用して、特定のメッセージクラスの受信フォルダーとしてフォルダーを設定します。</span><span class="sxs-lookup"><span data-stu-id="bae3b-138">MFCMAPI uses the **IMsgStore::SetReceiveFolder** method to set a folder as the receive folder for a particular message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bae3b-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="bae3b-139">See also</span></span>



[<span data-ttu-id="bae3b-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bae3b-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="bae3b-141">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="bae3b-141">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

