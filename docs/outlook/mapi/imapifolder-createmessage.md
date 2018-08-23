---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8d7e6dfbf9e6a751845adb2319b66462bcde651f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800472"
---
# <a name="imapifoldercreatemessage"></a><span data-ttu-id="d659d-103">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="d659d-103">IMAPIFolder::CreateMessage</span></span>

  
  
<span data-ttu-id="d659d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d659d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d659d-105">新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="d659d-105">Creates a new message.</span></span>
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a><span data-ttu-id="d659d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d659d-106">Parameters</span></span>

 <span data-ttu-id="d659d-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d659d-107">_lpInterface_</span></span>
  
> <span data-ttu-id="d659d-108">[in]新しいメッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d659d-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new message.</span></span> <span data-ttu-id="d659d-109">に対する、IID_IMAPIProp、IID_IMAPIContainer、および IID_IMAPIFolder は、有効なインターフェイス識別子が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d659d-109">Valid interface identifiers include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> <span data-ttu-id="d659d-110">メッセージ ストア プロバイダーは、標準的なメッセージのインターフェイスを取得すると、NULL を渡す[IMessage: IMAPIProp](imessageimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="d659d-110">Passing NULL causes the message store provider to return the standard message interface, [IMessage : IMAPIProp](imessageimapiprop.md).</span></span> 
    
 <span data-ttu-id="d659d-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d659d-111">_ulFlags_</span></span>
  
> <span data-ttu-id="d659d-112">[in]メッセージを作成する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="d659d-112">[in] A bitmask of flags that controls how the message is created.</span></span> <span data-ttu-id="d659d-113">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d659d-113">The following flags can be set:</span></span>
    
<span data-ttu-id="d659d-114">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="d659d-114">ITEMPROC_FORCE</span></span>
  
> <span data-ttu-id="d659d-115">示す個人用フォルダー ストア (PST) の対象となるメッセージがルール ストアが、新しいメッセージの到着をリッスンしているすべてのクライアントに通知する前に処理します。</span><span class="sxs-lookup"><span data-stu-id="d659d-115">Indicates to the personal folder store (PST) that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="d659d-116">のみを処理するルールは、Exchange Server がサーバー上のメッセージのルールを処理するため、Microsoft Exchange Server のではないサーバー上に作成される新しいメッセージに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d659d-116">Rules processing only applies to new messages that are created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="d659d-117">したがって、プロバイダーまたはクライアントがメッセージを作成する渡す必要がありますこのフラグの組み合わせを[IMAPIPProp::SaveChanges](imapiprop-savechanges.md)にメッセージを保存する際にサーバーが、Exchange Server ではないことを示す、NON_EMS_XP_SAVE を使用しています。</span><span class="sxs-lookup"><span data-stu-id="d659d-117">Therefore, the provider or client creating the message must pass this flag in combination with saving a message with [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) using NON_EMS_XP_SAVE, which indicates that the server is not an Exchange Server.</span></span> 
    
<span data-ttu-id="d659d-118">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="d659d-118">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="d659d-119">メッセージを作成するのには、標準的な内容のテーブルの代わりに関連する内容の表に含まれなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d659d-119">The message to be created should be included in the associated contents table instead of the standard contents table.</span></span> <span data-ttu-id="d659d-120">ユーザーとの対話からは、関連するメッセージが表示されません。</span><span class="sxs-lookup"><span data-stu-id="d659d-120">Associated messages are hidden from user interaction.</span></span>
    
<span data-ttu-id="d659d-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d659d-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d659d-122">**メッセージ**は、作成操作が完全に完了していない場合でも成功することができます。</span><span class="sxs-lookup"><span data-stu-id="d659d-122">**CreateMessage** is allowed to succeed even if the create operation has not fully completed.</span></span> <span data-ttu-id="d659d-123">これは、新しいメッセージが使用できないことをすぐに呼び出し元にことを意味します。</span><span class="sxs-lookup"><span data-stu-id="d659d-123">This implies that the new message might not be immediately available to the caller.</span></span> 
    
 <span data-ttu-id="d659d-124">_lppMessage_</span><span class="sxs-lookup"><span data-stu-id="d659d-124">_lppMessage_</span></span>
  
> <span data-ttu-id="d659d-125">[out]新しく作成したメッセージへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d659d-125">[out] A pointer to a pointer to the newly created message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d659d-126">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d659d-126">Return value</span></span>

<span data-ttu-id="d659d-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="d659d-127">S_OK</span></span> 
  
> <span data-ttu-id="d659d-128">メッセージが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="d659d-128">The message was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d659d-129">注釈</span><span class="sxs-lookup"><span data-stu-id="d659d-129">Remarks</span></span>

<span data-ttu-id="d659d-130">**IMAPIFolder::CreateMessage**メソッドでは、ジェネリック、または関連するコンテンツを含む新しいメッセージを作成し、エントリ id を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d659d-130">The **IMAPIFolder::CreateMessage** method creates a new message with generic or associated content and assigns an entry identifier.</span></span> <span data-ttu-id="d659d-131">エントリの識別子は、メッセージ ストア プロバイダーを表す部分と個々 のメッセージを表す部分で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d659d-131">The entry identifier consists of a part that represents the message store provider and a part that represents the individual message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d659d-132">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="d659d-132">Notes to implementers</span></span>

<span data-ttu-id="d659d-133">**メッセージ**またはメッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドでは、すべての必要なメッセージ プロパティを設定するかどうかを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="d659d-133">You can choose whether to set all of the required message properties in **CreateMessage** or in the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="d659d-134">成功したセーブセットが発生するまで、これらのプロパティを使用できるようにする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d659d-134">You do not have to make these properties available until a successful save has occurred.</span></span> 
  
<span data-ttu-id="d659d-135">関連の情報を処理する方法の詳細については、 [Folder-Associated 情報のテーブル](folder-associated-information-tables.md)と[テーブルの内容](contents-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d659d-135">For more information about how to work with associated information, see [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d659d-136">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d659d-136">Notes to callers</span></span>

<span data-ttu-id="d659d-137">メッセージ ストア プロバイダーの中にすぐに**メッセージ**が返されるメッセージのエントリ id を許可します。その他のメッセージ ストア プロバイダーは、メッセージが保存されるまで、その可用性を遅延します。</span><span class="sxs-lookup"><span data-stu-id="d659d-137">Some message store providers allow the entry identifier of the new message to be available immediately after **CreateMessage** returns; other message store providers delay its availability until the message is saved.</span></span> <span data-ttu-id="d659d-138">すべてのメッセージ ストア プロバイダーは、メッセージの**IMAPIProp::SaveChanges**メソッドを呼び出してするまで、新しいメッセージのエントリ id を生成するため、できないことがあります**メッセージ**が返されるときに、エントリの識別子にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d659d-138">Because not all message store providers generate an entry identifier for a new message until you have called the message's **IMAPIProp::SaveChanges** method, you may be unable to access the entry identifier when **CreateMessage** returns.</span></span> <span data-ttu-id="d659d-139">また、新しいメッセージは含まれません、フォルダーの内容のテーブルでの保存が実行されるまで。</span><span class="sxs-lookup"><span data-stu-id="d659d-139">Also, the new message may not be included in the folder's contents table until the save occurs.</span></span> 
  
<span data-ttu-id="d659d-140">になるだけでなく、現在のメッセージ ・ ストア内で一意であるが、最も可能性の高いすべてのメッセージ ストアを同時に開いている新しいメッセージに割り当てられたエントリの識別子を期待してください。</span><span class="sxs-lookup"><span data-stu-id="d659d-140">Expect the entry identifier assigned to the new message to be unique not only in the current message store, but most likely across all of the message stores that are open at the same time.</span></span> <span data-ttu-id="d659d-141">この規則に例外が 1 つは、[プロファイルのメッセージ ストアに複数のエントリが表示されるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="d659d-141">One exception to this rule occurs when multiple entries for a message store appear in the profile.</span></span> <span data-ttu-id="d659d-142">これは、メッセージ ・ ストアを複数回開くと重複するエントリの識別子です。</span><span class="sxs-lookup"><span data-stu-id="d659d-142">This causes the message store to be opened multiple times and entry identifiers to be duplicated.</span></span> 
  
<span data-ttu-id="d659d-143">送信メッセージを作成するには、[送信トレイ] フォルダーの**IMAPIFolder::CreateMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d659d-143">To create an outgoing message, call the Outbox folder's **IMAPIFolder::CreateMessage** method.</span></span> 
  
<span data-ttu-id="d659d-144">メッセージが保存される前に、新しいメッセージを格納するフォルダーを削除した場合、結果は定義されていません。</span><span class="sxs-lookup"><span data-stu-id="d659d-144">If you delete a folder that contains a new message before the message is saved, the results are undefined.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d659d-145">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="d659d-145">MFCMAPI reference</span></span>

<span data-ttu-id="d659d-146">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="d659d-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d659d-147">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="d659d-147">**File**</span></span>|<span data-ttu-id="d659d-148">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="d659d-148">**Function**</span></span>|<span data-ttu-id="d659d-149">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="d659d-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d659d-150">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="d659d-150">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="d659d-151">CFolder::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="d659d-151">CFolder::OnNewMessage</span></span>  <br/> |<span data-ttu-id="d659d-152">MFCMAPI では、 **IMAPIFolder::CreateMessage**メソッドを使用して、作成し、新しいメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="d659d-152">MFCMAPI uses the **IMAPIFolder::CreateMessage** method to create and save a new message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d659d-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="d659d-153">See also</span></span>



[<span data-ttu-id="d659d-154">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="d659d-154">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="d659d-155">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="d659d-155">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="d659d-156">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="d659d-156">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

