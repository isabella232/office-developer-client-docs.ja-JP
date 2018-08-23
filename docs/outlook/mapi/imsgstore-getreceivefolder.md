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
ms.openlocfilehash: a8cd211cc16b620ac47357271070e0b45b867bea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579943"
---
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="2c5b9-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="2c5b9-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="2c5b9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c5b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c5b9-105">または、指定したメッセージ クラスの既定値として受信したメッセージの送信先には、メッセージ ストアのフォルダーが表示されるように設定されているフォルダーを取得します。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="2c5b9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2c5b9-106">Parameters</span></span>

 <span data-ttu-id="2c5b9-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="2c5b9-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="2c5b9-108">[in]受信フォルダーに関連付けられているメッセージ クラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="2c5b9-109">返します_lpszMessageClass_パラメーターが NULL または空の文字列を**GetReceiveFolder**に設定、既定ではメッセージ ストアのフォルダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="2c5b9-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2c5b9-110">_ulFlags_</span></span>
  
> <span data-ttu-id="2c5b9-111">[in]渡されると、返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="2c5b9-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-112">The following flag can be set:</span></span>
    
<span data-ttu-id="2c5b9-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2c5b9-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2c5b9-114">メッセージ クラスの文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="2c5b9-115">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のメッセージ クラスの文字列です。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="2c5b9-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2c5b9-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="2c5b9-117">[out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2c5b9-118">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="2c5b9-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="2c5b9-119">[out]要求されたエントリの識別子へのポインターへのポインターでは、フォルダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="2c5b9-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="2c5b9-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="2c5b9-121">[out]として明示的に設定するメッセージ クラスへのポインターへのポインターの_lppEntryID_で指定されたフォルダーのフォルダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="2c5b9-122">このメッセージ クラスでは、 _lpszMessageClass_パラメーターにクラスまたはそのクラスの基本クラスと同じする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="2c5b9-123">NULL を渡すことは、 _lppEntryID_が指すフォルダーは、既定値には、メッセージ ストアのフォルダーが表示されることを示します。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2c5b9-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="2c5b9-124">Return value</span></span>

<span data-ttu-id="2c5b9-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="2c5b9-125">S_OK</span></span> 
  
> <span data-ttu-id="2c5b9-126">受信フォルダーが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2c5b9-127">注釈</span><span class="sxs-lookup"><span data-stu-id="2c5b9-127">Remarks</span></span>

<span data-ttu-id="2c5b9-128">**IMsgStore::GetReceiveFolder**メソッドは、特定のメッセージ クラスのメッセージを受信する指定されたフォルダー、受信フォルダーのエントリ id を取得します。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="2c5b9-129">呼び出し元が_lpszMessageClass_パラメーターでは、メッセージ クラスまたは NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="2c5b9-130">_LpszMessageClass_が NULL の場合は、 **GetReceiveFolder**は、次の値を返します。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="2c5b9-131">_LppszExplicitClass_、メッセージ クラスの 1 つ目の基本クラスの名前で示される_lpszMessageClass_は、受信フォルダーを明示的に設定します。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="2c5b9-132">_LppEntryID_、基本クラスの受信フォルダーのエントリ id は、 _lppszExplicitClass_パラメーターを参照できます。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="2c5b9-133">たとえば、メッセージ クラス IPM の**の受信フォルダーがあるとします。注**が設定されているエントリに、受信トレイと**GetReceiveFolder**の識別子と呼ばれる_lpszMessageClass_ **IPM に設定の内容とします。Note.Phone**。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="2c5b9-134">場合**IPM。Note.Phone**はありませんが、明示的な受信フォルダー セット、 **GetReceiveFolder**は、 _lppEntryID_と**IPM で、[受信トレイ] のエントリ id を返します。注** _lppszExplicitClass_にします。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="2c5b9-135">_LppszExplicitClass_は長さ 0 の文字列、Unicode 形式で文字列またはかどうかによって、ANSI 形式の文字列のいずれかのクライアントは、メッセージ クラスの**GetReceiveFolder**を呼び出すし、そのメッセージ クラス用の受信フォルダーを設定していない、する場合、クライアントは、 _ulFlags_パラメーターに MAPI_UNICODE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="2c5b9-136">既定では、 _lpszMessageClass_パラメーターに NULL を渡すことによって取得したフォルダーが表示される、メッセージ ・ ストアごとに常に存在します。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="2c5b9-137">クライアントは、そのエントリの識別子を保持するメモリを解放するのには_lppEntryID_で返されるエントリの識別子を使用して登録が完了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="2c5b9-138">**MAPIFreeBuffer**は、その文字列を保持しているメモリを解放するのには_lppszExplicitClass_で返されるメッセージ クラスの文字列の処理が終わったらそれも呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2c5b9-139">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="2c5b9-139">MFCMAPI reference</span></span>

<span data-ttu-id="2c5b9-140">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="2c5b9-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2c5b9-141">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="2c5b9-141">**File**</span></span>|<span data-ttu-id="2c5b9-142">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="2c5b9-142">**Function**</span></span>|<span data-ttu-id="2c5b9-143">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="2c5b9-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2c5b9-144">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="2c5b9-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2c5b9-145">GetInbox</span><span class="sxs-lookup"><span data-stu-id="2c5b9-145">GetInbox</span></span>  <br/> |<span data-ttu-id="2c5b9-146">MFCMAPI では、 **IMsgStore::GetReceiveFolder**メソッドを使用して、受信トレイ フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="2c5b9-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c5b9-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c5b9-147">See also</span></span>



[<span data-ttu-id="2c5b9-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2c5b9-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2c5b9-149">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2c5b9-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="2c5b9-150">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2c5b9-150">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

