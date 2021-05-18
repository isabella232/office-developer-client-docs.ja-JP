---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2c8244180a5cafedc887fa72f36f233fb5084f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316633"
---
# <a name="imapipropsavechanges"></a><span data-ttu-id="67f25-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="67f25-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="67f25-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67f25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67f25-105">最後の保存操作以降にオブジェクトに加えた変更を永続的に行います。</span><span class="sxs-lookup"><span data-stu-id="67f25-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="67f25-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="67f25-106">Parameters</span></span>

 <span data-ttu-id="67f25-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="67f25-107">_ulFlags_</span></span>
  
> <span data-ttu-id="67f25-108">[in] **IMAPIProp::SaveChanges** メソッドが呼び出された場合にオブジェクトに何が起こるかを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="67f25-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="67f25-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="67f25-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="67f25-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="67f25-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="67f25-111">メッセージがサーバーから配信されていないMicrosoft Exchange Server。</span><span class="sxs-lookup"><span data-stu-id="67f25-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="67f25-112">このフラグは [、IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドと ITEMPROC_FORCE フラグを組み合わせて使用して、メッセージが個人用フォルダー ファイル (PST) ストアが受信したリッスン クライアントに通知する前に、メッセージがルール処理の対象となるかどうかを PST ストアに示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="67f25-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="67f25-113">このルール処理は、Exchange Server ではないサーバー上で[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を使用して作成された新しいメッセージにのみ適用されます。その場合、Exchange Server はメッセージのルールを既に処理している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="67f25-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="67f25-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="67f25-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="67f25-115">変更はオブジェクトに書き込み、オブジェクトに対して行われた以前の変更を上書きし、オブジェクトを閉じるべきです。</span><span class="sxs-lookup"><span data-stu-id="67f25-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="67f25-116">操作が成功するには、読み取り/書き込みアクセス許可を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67f25-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="67f25-117">**SaveChanges** FORCE_SAVE呼び出しが返された後に、このフラグがMAPI_E_OBJECT_CHANGED。</span><span class="sxs-lookup"><span data-stu-id="67f25-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="67f25-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="67f25-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="67f25-119">変更はコミットする必要があります。オブジェクトは読み取り用に開いたままにしてください。</span><span class="sxs-lookup"><span data-stu-id="67f25-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="67f25-120">追加の変更は行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="67f25-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="67f25-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="67f25-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="67f25-122">変更はコミットする必要があります。オブジェクトは読み取り/書き込みアクセス許可のために開いた状態に保つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="67f25-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="67f25-123">このフラグは、通常、オブジェクトが読み取り/書き込みアクセス許可のために最初に開かされたときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="67f25-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="67f25-124">オブジェクトに対するそれ以降の変更は許可されます。</span><span class="sxs-lookup"><span data-stu-id="67f25-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="67f25-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="67f25-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="67f25-126">**変更が完全に** コミットされる前に、SaveChanges が正常に返されるのを許可します。</span><span class="sxs-lookup"><span data-stu-id="67f25-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="67f25-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="67f25-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="67f25-128">保存中のメッセージに対するスパム フィルターを有効にする。</span><span class="sxs-lookup"><span data-stu-id="67f25-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="67f25-129">スパムのフィルター処理に関するサポートは、送信者の電子メール アドレスの種類が簡易メール転送プロトコル (SMTP) であり、メッセージが個人用フォルダー ファイル (PST) 向けのストアに保存されている場合にのみ使用することができます。</span><span class="sxs-lookup"><span data-stu-id="67f25-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="67f25-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="67f25-130">Return value</span></span>

<span data-ttu-id="67f25-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="67f25-131">S_OK</span></span> 
  
> <span data-ttu-id="67f25-132">変更のコミットメントは成功しました。</span><span class="sxs-lookup"><span data-stu-id="67f25-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="67f25-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="67f25-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="67f25-134">**SaveChanges は** 、オブジェクトが設定されている場合は読み取り専用KEEP_OPEN_READONLY開いた状態にしたり、設定されている場合は読み取り/書きKEEP_OPEN_READWRITEできません。</span><span class="sxs-lookup"><span data-stu-id="67f25-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="67f25-135">変更はコミットされません。</span><span class="sxs-lookup"><span data-stu-id="67f25-135">No changes are committed.</span></span> 
    
<span data-ttu-id="67f25-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="67f25-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="67f25-137">オブジェクトは開いた後に変更されました。</span><span class="sxs-lookup"><span data-stu-id="67f25-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="67f25-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="67f25-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="67f25-139">オブジェクトは開いた後に削除されています。</span><span class="sxs-lookup"><span data-stu-id="67f25-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="67f25-140">注釈</span><span class="sxs-lookup"><span data-stu-id="67f25-140">Remarks</span></span>

<span data-ttu-id="67f25-141">**IMAPIProp::SaveChanges** メソッドは、メッセージ、添付ファイル、アドレス帳コンテナー、メッセージング ユーザー オブジェクトなど、処理のトランザクション モデルをサポートするオブジェクトに対してプロパティの変更を永続的に行います。</span><span class="sxs-lookup"><span data-stu-id="67f25-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="67f25-142">フォルダー、メッセージ ストア、プロファイル セクションなど、トランザクションをサポートしないオブジェクトは、直ちに変更を永続的に行います。</span><span class="sxs-lookup"><span data-stu-id="67f25-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="67f25-143">**SaveChanges への呼び出しは** 必要ありません。</span><span class="sxs-lookup"><span data-stu-id="67f25-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="67f25-144">サービス プロバイダーは、すべてのプロパティが保存されるまでオブジェクトのエントリ識別子を生成する必要はないので、 **オブジェクトの PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティは **、SaveChanges** メソッドが呼び出されるまで使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="67f25-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="67f25-145">一部のプロバイダーは **、SaveChanges** KEEP_OPEN_READONLYに設定されるまで待機します。</span><span class="sxs-lookup"><span data-stu-id="67f25-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="67f25-146">KEEP_OPEN_READONLYは、現在の呼び出しに保存する変更が、オブジェクトに対して行われる最後の変更になります。</span><span class="sxs-lookup"><span data-stu-id="67f25-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="67f25-147">一部のメッセージ ストアの実装では、クライアントが **SaveChanges** を使用してメッセージの変更を保存し [、IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) メソッドを使用してメッセージ オブジェクトを解放するまで、新しく作成されたメッセージをフォルダーに表示しません。</span><span class="sxs-lookup"><span data-stu-id="67f25-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="67f25-148">さらに、一部のオブジェクト実装では **、SaveChanges** が呼び出されるまで、新しく作成されたオブジェクトの PR_ENTRYID プロパティを生成できません。また、一部のオブジェクトは _、ulFlags_ で **KEEP_OPEN_READONLY** セットを使用して **SaveChanges** が呼び出された後にのみ生成できます。</span><span class="sxs-lookup"><span data-stu-id="67f25-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="67f25-149">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="67f25-149">Notes to implementers</span></span>

<span data-ttu-id="67f25-150">このフラグを受けKEEP_OPEN_READONLY、オブジェクトのアクセスを読み取り/書き込みとして残すオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="67f25-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="67f25-151">ただし、プロバイダーは、オブジェクトフラグが渡された場合、オブジェクトを読み取り専用KEEP_OPEN_READWRITEすることはできません。</span><span class="sxs-lookup"><span data-stu-id="67f25-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="67f25-152">クライアントは、複数の添付ファイルを複数のメッセージに保存すると、すべての添付ファイルとすべてのメッセージに対して **SaveChanges** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="67f25-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="67f25-153">多くの場合、クライアントはMAPI_DEFERRED_ERRORSを除き、これらの各呼び出しに対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="67f25-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="67f25-154">最後の呼び出しまたは以前の呼び出しでエラーを返す場合があります。</span><span class="sxs-lookup"><span data-stu-id="67f25-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="67f25-155">フラグは無視できます。</span><span class="sxs-lookup"><span data-stu-id="67f25-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="67f25-156">エラーのKEEP_OPEN_READWRITEまたはKEEP_OPEN_READONLYが一緒に設定されている場合MAPI_DEFERRED_ERRORS、エラー延期要求を無視できます。</span><span class="sxs-lookup"><span data-stu-id="67f25-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="67f25-157">_ulFlags_ MAPI_DEFERRED_ERRORS設定されていない場合 **、SaveChanges** 呼び出しで以前に延期されたエラーの 1 つを返す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="67f25-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="67f25-158">リモート トランスポート プロバイダーがこのメソッドの機能実装を提供するかどうかはオプションであり、実装の他の設計上の選択肢に依存します。</span><span class="sxs-lookup"><span data-stu-id="67f25-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="67f25-159">このメソッドを実装する場合は、ここでのドキュメントに従って実行します。</span><span class="sxs-lookup"><span data-stu-id="67f25-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="67f25-160">フォルダー オブジェクトと状態オブジェクトは処理されないので、少なくともリモート トランスポート プロバイダーによる **SaveChanges** の実装では、実際に作業を行わずに S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="67f25-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="67f25-161">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="67f25-161">Notes to callers</span></span>

<span data-ttu-id="67f25-162">クライアントがメソッドを渡KEEP_OPEN_READONLY [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出し、再び **SaveChanges** を呼び出した場合、同じ実装が失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="67f25-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="67f25-163">ユーザーがMAPI_E_NO_ACCESS設定した呼び出しからKEEP_OPEN_READWRITEを受け取った後、オブジェクトに対する読み取り/書き込みアクセス許可を持ち続ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="67f25-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="67f25-164">SaveChanges を **再度呼び** 出して、KEEP_OPEN_READONLYフラグを渡したり、フラグを指定KEEP_OPEN_SUFFIX。</span><span class="sxs-lookup"><span data-stu-id="67f25-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="67f25-165">プロバイダーがアプリケーション フラグをKEEP_OPEN_READWRITEかどうかは、プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="67f25-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="67f25-166">**SaveChanges** の後にオブジェクトに対して行う唯一の呼び出しが **IUnknown::Release** かどうかを示すために _、ulFlags_ パラメーターにフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="67f25-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="67f25-167">**SaveChanges のエラーは**、保留中の変更を永続的に行えなかねない状況を示します。</span><span class="sxs-lookup"><span data-stu-id="67f25-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="67f25-168">SaveChanges 呼び出しのフラグがない場合は、プロバイダー **によって処理** が異なります。</span><span class="sxs-lookup"><span data-stu-id="67f25-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="67f25-169">一部のプロバイダーは、この状態をユーザーと同KEEP_OPEN_READONLY。他のプロバイダーは、このプロバイダーと同じKEEP_OPEN_READWRITE。</span><span class="sxs-lookup"><span data-stu-id="67f25-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="67f25-170">それでも他のプロバイダーは **、SaveChanges** 呼び出しでフラグを受信しない場合にオブジェクトをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="67f25-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="67f25-171">一部のプロパティ (通常は計算されたプロパティ) は **、SaveChanges** を呼び出し、場合によっては Release を呼び出すまで処理 **できません**。</span><span class="sxs-lookup"><span data-stu-id="67f25-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="67f25-172">添付ファイルを複数のメッセージに保存するなどの一括変更を行う場合は  _、ulFlags_ で MAPI_DEFERRED_ERRORSフラグを設定してエラー処理を延期します。</span><span class="sxs-lookup"><span data-stu-id="67f25-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="67f25-173">複数の添付ファイルを複数のメッセージに保存する場合は、各添付ファイルに対して **1 つの SaveChanges** 呼び出しを行い、各メッセージに対して **1 つの SaveChanges** 呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="67f25-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="67f25-174">添付ファイル呼びMAPI_DEFERRED_ERRORS最後のメッセージを除くすべてのメッセージに対して、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="67f25-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="67f25-175">**SaveChanges が** オブジェクトをMAPI_E_OBJECT_CHANGED場合は、元のオブジェクトが変更されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="67f25-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="67f25-176">その場合は、変更が以前の変更を上書きするか、オブジェクトを別の場所に保存するかどうかを要求できるユーザーに警告します。</span><span class="sxs-lookup"><span data-stu-id="67f25-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="67f25-177">元のオブジェクトが削除されている場合は、別の場所にオブジェクトを保存する機会を与えるユーザーに警告します。</span><span class="sxs-lookup"><span data-stu-id="67f25-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="67f25-178">削除された開いているオブジェクトの FORCE_SAVEフラグを使用して **SaveChanges** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="67f25-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="67f25-179">**SaveChanges が** エラーを返す場合、変更を保存するオブジェクトは _、ulFlags_ パラメーターで設定されたフラグに関係なく開いたままです。</span><span class="sxs-lookup"><span data-stu-id="67f25-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="67f25-180">_ulFlags_ NON_EMS_XP_SAVE および SPAMFILTER_ONSAVE は、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は、次の値を使用してコードに追加>`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="67f25-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="67f25-181">詳細については、「MAPI プロパティの [保存」を参照してください](saving-mapi-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="67f25-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="67f25-182">関連項目</span><span class="sxs-lookup"><span data-stu-id="67f25-182">See also</span></span>



[<span data-ttu-id="67f25-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="67f25-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="67f25-184">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="67f25-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="67f25-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="67f25-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="67f25-186">MAPI プロパティの保存</span><span class="sxs-lookup"><span data-stu-id="67f25-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

