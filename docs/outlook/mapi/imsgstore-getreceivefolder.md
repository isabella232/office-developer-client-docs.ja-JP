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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ab21dcfb9011b675e3db4e4df29cb6ecafa6e7c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435349"
---
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="ad575-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="ad575-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="ad575-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad575-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad575-105">指定したメッセージ クラスの受信メッセージの送信先として、またはメッセージ ストアの既定の受信フォルダーとして確立されたフォルダーを取得します。</span><span class="sxs-lookup"><span data-stu-id="ad575-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="ad575-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ad575-106">Parameters</span></span>

 <span data-ttu-id="ad575-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="ad575-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="ad575-108">[in]受信フォルダーに関連付けられているメッセージ クラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ad575-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="ad575-109">_lpszMessageClass_ パラメーターが NULL または空の文字列に設定されている場合 **、GetReceiveFolder** はメッセージ ストアの既定の受信フォルダーを返します。</span><span class="sxs-lookup"><span data-stu-id="ad575-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="ad575-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ad575-110">_ulFlags_</span></span>
  
> <span data-ttu-id="ad575-111">[in]渡された文字列と返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ad575-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="ad575-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ad575-112">The following flag can be set:</span></span>
    
<span data-ttu-id="ad575-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ad575-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ad575-114">メッセージ クラスの文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="ad575-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="ad575-115">メッセージ クラスMAPI_UNICODEが設定されていない場合、メッセージ クラス文字列は ANSI 形式です。</span><span class="sxs-lookup"><span data-stu-id="ad575-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="ad575-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ad575-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="ad575-117">[out]  _lppEntryID_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ad575-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ad575-118">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="ad575-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="ad575-119">[out]要求された受信フォルダーのエントリ識別子へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="ad575-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="ad575-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="ad575-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="ad575-121">[out]  _lppEntryID_ が指すフォルダーを受信フォルダーとして明示的に設定するメッセージ クラスへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="ad575-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="ad575-122">このメッセージ クラスは  _、lpszMessageClass_ パラメーターのクラスと同じか、そのクラスの基本クラスのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad575-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="ad575-123">NULL を渡す場合は  _、lppEntryID_ が指すフォルダーがメッセージ ストアの既定の受信フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="ad575-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ad575-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="ad575-124">Return value</span></span>

<span data-ttu-id="ad575-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad575-125">S_OK</span></span> 
  
> <span data-ttu-id="ad575-126">受信フォルダーが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="ad575-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad575-127">注釈</span><span class="sxs-lookup"><span data-stu-id="ad575-127">Remarks</span></span>

<span data-ttu-id="ad575-128">**IMsgStore::GetReceiveFolder** メソッドは、受信フォルダー (特定のメッセージ クラスの受信メッセージを受信するために指定されたフォルダー) のエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="ad575-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="ad575-129">呼び出し元は  _、lpszMessageClass_ パラメーターでメッセージ クラスまたは NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ad575-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="ad575-130">_lpszMessageClass が_ NULL の場合 **、GetReceiveFolder は次** の値を返します。</span><span class="sxs-lookup"><span data-stu-id="ad575-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="ad575-131">_lppszExplicitClass_ では、受信フォルダーを明示的に設定する _lpszMessageClass_ が指すメッセージ クラスの最初の基本クラスの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="ad575-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="ad575-132">_lppEntryID では__、lppszExplicitClass_ パラメーターが指す基本クラスの受信フォルダーのエントリ識別子。</span><span class="sxs-lookup"><span data-stu-id="ad575-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="ad575-133">たとえば、メッセージ クラス IPM の受信フォルダーと **します。メモ** は受信トレイのエントリ識別子に設定され **、GetReceiveFolder** は _lpszMessageClass_ の内容を IPM に設定して呼び **出されます。注。電話**.</span><span class="sxs-lookup"><span data-stu-id="ad575-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="ad575-134">**IPM の場合。注。電話** 明示的な受信フォルダー セットが存在しない場合 **、GetReceiveFolder** は _lppEntryID_ と IPM の受信トレイのエントリ **識別子を返します。** _lppszExplicitClass のメモ_。</span><span class="sxs-lookup"><span data-stu-id="ad575-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="ad575-135">クライアントがメッセージ クラスの **GetReceiveFolder** を呼び出し、そのメッセージ クラスの受信フォルダーを設定していない場合  _、lppszExplicitClass_ は、クライアントが  _ulFlags_ パラメーターに MAPI_UNICODE フラグを設定したかどうかに応じて、長さ 0 の文字列、Unicode 形式の文字列、または ANSI 形式の文字列のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="ad575-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="ad575-136">_lpszMessageClass_ パラメーターに NULL を渡して取得した既定の受信フォルダーは、すべてのメッセージ ストアに常に存在します。</span><span class="sxs-lookup"><span data-stu-id="ad575-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="ad575-137">クライアントは [、lppEntryID](mapifreebuffer.md) で返されるエントリ識別子を使用して、そのエントリ識別子を保持するメモリを解放するときに  _MAPIFreeBuffer_ 関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad575-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="ad575-138">また _、lppszExplicitClass_ で返されるメッセージ クラス文字列を使用して、その文字列を保持するメモリを解放するときに **MAPIFreeBuffer** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad575-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ad575-139">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="ad575-139">MFCMAPI reference</span></span>

<span data-ttu-id="ad575-140">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad575-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ad575-141">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="ad575-141">**File**</span></span>|<span data-ttu-id="ad575-142">**関数**</span><span class="sxs-lookup"><span data-stu-id="ad575-142">**Function**</span></span>|<span data-ttu-id="ad575-143">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ad575-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ad575-144">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ad575-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ad575-145">GetInbox</span><span class="sxs-lookup"><span data-stu-id="ad575-145">GetInbox</span></span>  <br/> |<span data-ttu-id="ad575-146">MFCMAPI は **、IMsgStore::GetReceiveFolder** メソッドを使用して受信トレイ フォルダーを検索します。</span><span class="sxs-lookup"><span data-stu-id="ad575-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad575-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad575-147">See also</span></span>



[<span data-ttu-id="ad575-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ad575-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ad575-149">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ad575-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="ad575-150">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ad575-150">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

