---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ab21dcfb9011b675e3db4e4df29cb6ecafa6e7c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348777"
---
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="062a4-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="062a4-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="062a4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="062a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="062a4-105">指定したメッセージクラスの受信メッセージの宛先として、またはメッセージストアの既定の受信フォルダーとして確立されたフォルダーを取得します。</span><span class="sxs-lookup"><span data-stu-id="062a4-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="062a4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="062a4-106">Parameters</span></span>

 <span data-ttu-id="062a4-107">_lpszmessageclass_</span><span class="sxs-lookup"><span data-stu-id="062a4-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="062a4-108">順番受信フォルダーに関連付けられているメッセージクラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="062a4-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="062a4-109">_lpszmessageclass_パラメーターが NULL または空の文字列に設定されている場合、 **getreceivefolder**はメッセージストアの既定の受信フォルダーを返します。</span><span class="sxs-lookup"><span data-stu-id="062a4-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="062a4-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="062a4-110">_ulFlags_</span></span>
  
> <span data-ttu-id="062a4-111">順番渡された文字列と返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="062a4-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="062a4-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="062a4-112">The following flag can be set:</span></span>
    
<span data-ttu-id="062a4-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="062a4-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="062a4-114">メッセージクラスの文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="062a4-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="062a4-115">MAPI_UNICODE フラグが設定されていない場合、メッセージクラスの文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="062a4-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="062a4-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="062a4-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="062a4-117">読み上げ_lppentryid_パラメーターによって指定されたエントリ識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="062a4-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="062a4-118">_lppentryid_</span><span class="sxs-lookup"><span data-stu-id="062a4-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="062a4-119">読み上げ要求された受信フォルダーのエントリ識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="062a4-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="062a4-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="062a4-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="062a4-121">読み上げ_lppentryid_によって参照されるフォルダーを受信フォルダーとして明示的に設定する、メッセージクラスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="062a4-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="062a4-122">このメッセージクラスは、 _lpszmessageclass_パラメーターのクラス、またはそのクラスの基本クラスのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="062a4-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="062a4-123">NULL を渡すと、 _lppentryid_が指すフォルダーが、メッセージストアの既定の受信フォルダーであることを示します。</span><span class="sxs-lookup"><span data-stu-id="062a4-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="062a4-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="062a4-124">Return value</span></span>

<span data-ttu-id="062a4-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="062a4-125">S_OK</span></span> 
  
> <span data-ttu-id="062a4-126">受信フォルダーが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="062a4-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="062a4-127">解説</span><span class="sxs-lookup"><span data-stu-id="062a4-127">Remarks</span></span>

<span data-ttu-id="062a4-128">**IMsgStore:: getreceivefolder**メソッドは、受信フォルダーのエントリ id を取得します。これは、特定のメッセージクラスの受信メッセージを受信するように指定されたフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="062a4-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="062a4-129">呼び出し元は、 _lpszmessageclass_パラメーターでメッセージクラスまたは NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="062a4-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="062a4-130">_lpszmessageclass_が NULL の場合、 **getreceivefolder**は次の値を返します。</span><span class="sxs-lookup"><span data-stu-id="062a4-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="062a4-131">_lppszExplicitClass_では、明示的に受信フォルダーを設定する、 _lpszmessageclass_が指すメッセージクラスの最初の基本クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="062a4-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="062a4-132">_lppentryid_の場合、 _lppszExplicitClass_パラメーターによって参照される基本クラスの受信フォルダーのエントリ識別子。</span><span class="sxs-lookup"><span data-stu-id="062a4-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="062a4-133">たとえば、メッセージクラス IPM の受信フォルダーがあるとし**ます。メモ**は、受信トレイのエントリ識別子に設定され、 _lpszmessageclass_の内容を IPM に設定して、 **getreceivefolder**が呼び出され**ます。注電話番号**</span><span class="sxs-lookup"><span data-stu-id="062a4-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="062a4-134">**IPM.メモ電話**には、明示的な受信フォルダーが設定されていません。 **getreceivefolder**は、 _lppentryid_および IPM で受信トレイのエントリ識別子を返し**ます。** _lppszExplicitClass_でメモします。</span><span class="sxs-lookup"><span data-stu-id="062a4-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="062a4-135">クライアントがメッセージクラスの**getreceivefolder**を呼び出し、そのメッセージクラスの受信フォルダーが設定されていない場合、 _lppszExplicitClass_は、長さ0の文字列、Unicode 形式の文字列、または ANSI 形式の文字列のいずれかになります。クライアントは_ulflags_パラメーターに MAPI_UNICODE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="062a4-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="062a4-136">_lpszmessageclass_パラメーターで NULL を渡すことによって取得される既定の受信フォルダーは、すべてのメッセージストアに常に存在します。</span><span class="sxs-lookup"><span data-stu-id="062a4-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="062a4-137">クライアントは、そのエントリ識別子を保持するメモリを解放するために、 _lppentryid_で返されたエントリ識別子を使用して実行されたときに[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="062a4-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="062a4-138">また、 _lppszExplicitClass_で返されたメッセージクラス文字列を使用して、その文字列を保持するメモリを解放する場合も、 **MAPIFreeBuffer**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="062a4-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="062a4-139">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="062a4-139">MFCMAPI reference</span></span>

<span data-ttu-id="062a4-140">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="062a4-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="062a4-141">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="062a4-141">**File**</span></span>|<span data-ttu-id="062a4-142">**関数**</span><span class="sxs-lookup"><span data-stu-id="062a4-142">**Function**</span></span>|<span data-ttu-id="062a4-143">**コメント**</span><span class="sxs-lookup"><span data-stu-id="062a4-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="062a4-144">MAPIFunctions</span><span class="sxs-lookup"><span data-stu-id="062a4-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="062a4-145">getinbox</span><span class="sxs-lookup"><span data-stu-id="062a4-145">GetInbox</span></span>  <br/> |<span data-ttu-id="062a4-146">mfcmapi は、 **IMsgStore:: getreceivefolder**メソッドを使用して、受信トレイフォルダーを見つけます。</span><span class="sxs-lookup"><span data-stu-id="062a4-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="062a4-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="062a4-147">See also</span></span>



[<span data-ttu-id="062a4-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="062a4-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="062a4-149">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="062a4-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="062a4-150">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="062a4-150">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

