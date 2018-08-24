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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4e2d4f76fe436fd18b439bbbb558b1169094b438
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589463"
---
# <a name="imsgstoresetreceivefolder"></a><span data-ttu-id="3f85b-103">IMsgStore::SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="3f85b-103">IMsgStore::SetReceiveFolder</span></span>

  
  
<span data-ttu-id="3f85b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f85b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f85b-105">特定のメッセージ クラスの着信メッセージの送信先として、フォルダーを確立します。</span><span class="sxs-lookup"><span data-stu-id="3f85b-105">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="3f85b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3f85b-106">Parameters</span></span>

 <span data-ttu-id="3f85b-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="3f85b-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="3f85b-108">[in]新しいに関連するメッセージ クラスへのポインターでは、フォルダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3f85b-108">[in] A pointer to the message class that is to be associated with the new receive folder.</span></span> <span data-ttu-id="3f85b-109">セット_lpszMessageClass_パラメーターが NULL または空の文字列を**SetReceiveFolder**に設定、既定ではメッセージ ストアのフォルダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3f85b-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **SetReceiveFolder** sets the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="3f85b-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3f85b-110">_ulFlags_</span></span>
  
> <span data-ttu-id="3f85b-111">[in]渡された文字列内のテキストの種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="3f85b-111">[in] A bitmask of flags that controls the type of the text in the passed-in strings.</span></span> <span data-ttu-id="3f85b-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="3f85b-112">The following flag can be set:</span></span>
    
<span data-ttu-id="3f85b-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3f85b-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3f85b-114">メッセージ クラスの文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="3f85b-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="3f85b-115">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のメッセージ クラスの文字列です。</span><span class="sxs-lookup"><span data-stu-id="3f85b-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="3f85b-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3f85b-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="3f85b-117">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="3f85b-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="3f85b-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="3f85b-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="3f85b-119">[in]受信フォルダーとして設定するフォルダーのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3f85b-119">[in] A pointer to the entry identifier of the folder to establish as the receive folder.</span></span> <span data-ttu-id="3f85b-120">置換_lpEntryID_パラメーターが NULL の場合、 **SetReceiveFolder**に設定、現在ではメッセージ ストアの既定のフォルダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3f85b-120">If the  _lpEntryID_ parameter is set to NULL, **SetReceiveFolder** replaces the current receive folder with the message store's default.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3f85b-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="3f85b-121">Return value</span></span>

<span data-ttu-id="3f85b-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f85b-122">S_OK</span></span> 
  
> <span data-ttu-id="3f85b-123">受信フォルダーが正常に確立しました。</span><span class="sxs-lookup"><span data-stu-id="3f85b-123">A receive folder was successfully established.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f85b-124">注釈</span><span class="sxs-lookup"><span data-stu-id="3f85b-124">Remarks</span></span>

<span data-ttu-id="3f85b-125">**IMsgStore::SetReceiveFolder**メソッドは、特定のメッセージ クラスに対応する受信フォルダーを変更または設定します。</span><span class="sxs-lookup"><span data-stu-id="3f85b-125">The **IMsgStore::SetReceiveFolder** method sets or changes the receive folder for a particular message class.</span></span> <span data-ttu-id="3f85b-126">**SetReceiveFolder**とクライアント指定することも、後続の呼び出しを使用して、別に定義されたメッセージ クラスごとにフォルダーが表示されるか複数のメッセージ クラスのすべての受信メッセージが同じフォルダーに移動するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3f85b-126">With **SetReceiveFolder**, a client can, by using successive calls, specify a different receive folder for each defined message class or specify that incoming messages for multiple message classes all go to the same folder.</span></span> <span data-ttu-id="3f85b-127">などのクライアントは独自のフォルダーに到着したメッセージの独自クラスを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="3f85b-127">For example, a client can have its own class of messages arrive in its own folder.</span></span> <span data-ttu-id="3f85b-128">Fax アプリケーションには、ストア プロバイダーが着信 fax を格納する 1 つのフォルダーと、プロバイダーが発信 fax を配置する別のフォルダーを指定できます。</span><span class="sxs-lookup"><span data-stu-id="3f85b-128">A fax application can designate one folder in which the store provider puts incoming faxes and another folder in which the provider puts outgoing faxes.</span></span>
  
<span data-ttu-id="3f85b-129">**SetReceiveFolder**への呼び出し中にエラーが発生した場合、受信フォルダーの設定は変更されません。</span><span class="sxs-lookup"><span data-stu-id="3f85b-129">If an error occurs during the call to **SetReceiveFolder**, the receive folder setting remains unchanged.</span></span> 
  
<span data-ttu-id="3f85b-130">**SetReceiveFolder**が変更された場合、受信フォルダーの設定_lpEntryID_では NULL に設定をデフォルトの受信フォルダーを設定する必要があります、指定した既存の設定がない場合でも、 **SetReceiveFolder**は S_OK を返しますメッセージ クラスです。</span><span class="sxs-lookup"><span data-stu-id="3f85b-130">If **SetReceiveFolder** changes the receive folder setting with  _lpEntryID_ set to NULL, indicating that the default receive folder should be set, **SetReceiveFolder** returns S_OK even if there was no existing setting for the indicated message class.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3f85b-131">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="3f85b-131">MFCMAPI reference</span></span>

<span data-ttu-id="3f85b-132">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="3f85b-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3f85b-133">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="3f85b-133">**File**</span></span>|<span data-ttu-id="3f85b-134">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="3f85b-134">**Function**</span></span>|<span data-ttu-id="3f85b-135">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="3f85b-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3f85b-136">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="3f85b-136">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="3f85b-137">CMsgStoreDlg::OnSetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="3f85b-137">CMsgStoreDlg::OnSetReceiveFolder</span></span>  <br/> |<span data-ttu-id="3f85b-138">MFCMAPI では、 **IMsgStore::SetReceiveFolder**メソッドを使用して、特定のメッセージ クラスに対応する受信フォルダーとしてフォルダーを設定します。</span><span class="sxs-lookup"><span data-stu-id="3f85b-138">MFCMAPI uses the **IMsgStore::SetReceiveFolder** method to set a folder as the receive folder for a particular message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f85b-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="3f85b-139">See also</span></span>



[<span data-ttu-id="3f85b-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3f85b-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="3f85b-141">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="3f85b-141">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

