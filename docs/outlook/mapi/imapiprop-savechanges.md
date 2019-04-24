---
title: imapipropsavechanges
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
# <a name="imapipropsavechanges"></a><span data-ttu-id="5be46-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="5be46-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="5be46-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5be46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5be46-105">前回の保存操作以降にオブジェクトに加えられたすべての変更を永続的に行います。</span><span class="sxs-lookup"><span data-stu-id="5be46-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5be46-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5be46-106">Parameters</span></span>

 <span data-ttu-id="5be46-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5be46-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5be46-108">順番**imapiprop:: SaveChanges**メソッドが呼び出されたときに、オブジェクトに対して行われる処理を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="5be46-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="5be46-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5be46-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="5be46-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="5be46-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="5be46-111">メッセージが Microsoft Exchange サーバーから配信されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5be46-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="5be46-112">このフラグを[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドおよび ITEMPROC_FORCE フラグと組み合わせて使用して、個人用フォルダーファイル (pst) ストアが通知する前に、ルール処理の対象となるメッセージを pst ストアに示すように指定します。受信したクライアントメッセージが到着したこと。</span><span class="sxs-lookup"><span data-stu-id="5be46-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="5be46-113">このルールの処理は、exchange サーバー以外のサーバー上で[imapifolder:: CreateMessage](imapifolder-createmessage.md)を使用して作成された新しいメッセージにのみ適用されます。この場合、exchange サーバーはメッセージに対して既にルールを処理しています。</span><span class="sxs-lookup"><span data-stu-id="5be46-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="5be46-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="5be46-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="5be46-115">オブジェクトに変更を加えて、オブジェクトに対する以前の変更を上書きし、オブジェクトを閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5be46-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="5be46-116">操作を正常に行うには、読み取り/書き込みアクセス許可が設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5be46-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="5be46-117">FORCE_SAVE フラグは、以前に**SaveChanges**が MAPI_E_OBJECT_CHANGED を呼び出した後に使用されます。</span><span class="sxs-lookup"><span data-stu-id="5be46-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="5be46-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="5be46-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="5be46-119">変更を確定して、オブジェクトを読み取り用に開いたままにしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="5be46-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="5be46-120">追加の変更は行われません。</span><span class="sxs-lookup"><span data-stu-id="5be46-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="5be46-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="5be46-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="5be46-122">変更をコミットし、オブジェクトを読み取り/書き込みアクセス許可のために開いたままにしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="5be46-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="5be46-123">通常、このフラグは、オブジェクトが読み取り/書き込みアクセス許可で最初に開かれたときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="5be46-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="5be46-124">その後、オブジェクトに対する変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5be46-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="5be46-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5be46-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5be46-126">変更が完全にコミットされる前に、 **SaveChanges**が正常に戻ることができるようにします。</span><span class="sxs-lookup"><span data-stu-id="5be46-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="5be46-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="5be46-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="5be46-128">保存されているメッセージに対してスパムフィルター処理を有効にします。</span><span class="sxs-lookup"><span data-stu-id="5be46-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="5be46-129">スパムのフィルター処理に関するサポートは、送信者の電子メール アドレスの種類が簡易メール転送プロトコル (SMTP) であり、メッセージが個人用フォルダー ファイル (PST) 向けのストアに保存されている場合にのみ使用することができます。</span><span class="sxs-lookup"><span data-stu-id="5be46-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5be46-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="5be46-130">Return value</span></span>

<span data-ttu-id="5be46-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="5be46-131">S_OK</span></span> 
  
> <span data-ttu-id="5be46-132">変更のコミットメントに成功しました。</span><span class="sxs-lookup"><span data-stu-id="5be46-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="5be46-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5be46-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="5be46-134">KEEP_OPEN_READONLY が設定されている場合は読み取り専用アクセス許可、KEEP_OPEN_READWRITE が設定されている場合は読み取り/書き込みアクセス許可の場合、 **SaveChanges**ではオブジェクトを開いたままにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="5be46-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="5be46-135">変更はコミットされません。</span><span class="sxs-lookup"><span data-stu-id="5be46-135">No changes are committed.</span></span> 
    
<span data-ttu-id="5be46-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="5be46-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="5be46-137">オブジェクトが開かれた後に変更されました。</span><span class="sxs-lookup"><span data-stu-id="5be46-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="5be46-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="5be46-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="5be46-139">オブジェクトが開かれた後に削除されています。</span><span class="sxs-lookup"><span data-stu-id="5be46-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5be46-140">解説</span><span class="sxs-lookup"><span data-stu-id="5be46-140">Remarks</span></span>

<span data-ttu-id="5be46-141">**imapiprop:: SaveChanges**メソッドを使用すると、メッセージ、添付ファイル、アドレス帳コンテナー、メッセージングユーザーオブジェクトなど、処理のトランザクションモデルをサポートするオブジェクトのプロパティの変更を永続的に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5be46-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="5be46-142">フォルダー、メッセージストア、プロファイルセクションなど、トランザクションをサポートしていないオブジェクトは、直ちに変更を反映します。</span><span class="sxs-lookup"><span data-stu-id="5be46-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="5be46-143">**SaveChanges**を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5be46-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="5be46-144">すべてのプロパティが保存されるまでは、サービスプロバイダーはオブジェクトのエントリ識別子を生成する必要がないため、 **SaveChanges**メソッドの後までオブジェクトの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを使用できない場合があります。が呼び出されました。</span><span class="sxs-lookup"><span data-stu-id="5be46-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="5be46-145">一部のプロバイダーは、 **SaveChanges**呼び出しで KEEP_OPEN_READONLY フラグが設定されるまで待機します。</span><span class="sxs-lookup"><span data-stu-id="5be46-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="5be46-146">KEEP_OPEN_READONLY は、現在の呼び出しに保存される変更が、オブジェクトに対して最後に行われた変更であることを示します。</span><span class="sxs-lookup"><span data-stu-id="5be46-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="5be46-147">メッセージストアの実装によっては、クライアントが**SaveChanges**を使用してメッセージの変更を保存し、 [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを使用してメッセージオブジェクトを解放するまで、新しく作成されたメッセージがフォルダーに表示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="5be46-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="5be46-148">また、一部のオブジェクト実装では、 **savechanges**が呼び出されるまで、新しく作成されたオブジェクトの**PR_ENTRYID**プロパティを生成できません。また、KEEP_OPEN_READONLY を使用して**savechanges**が呼び出された後にのみ実行できるものもあります。_ulflags_で設定します。</span><span class="sxs-lookup"><span data-stu-id="5be46-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5be46-149">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="5be46-149">Notes to implementers</span></span>

<span data-ttu-id="5be46-150">KEEP_OPEN_READONLY フラグを受信した場合は、オブジェクトのアクセスを読み取り/書き込み可能にするオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="5be46-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="5be46-151">ただし、KEEP_OPEN_READWRITE フラグが渡された場合、プロバイダーはオブジェクトを読み取り専用状態にしておくことはできません。</span><span class="sxs-lookup"><span data-stu-id="5be46-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="5be46-152">クライアントが複数のメッセージに複数の添付ファイルを保存すると、すべての添付ファイルとすべてのメッセージに対して**SaveChanges**メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5be46-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="5be46-153">多くの場合、クライアントは、これらの呼び出しごとに MAPI_DEFERRED_ERRORS を設定します (最後の呼び出しを除く)。</span><span class="sxs-lookup"><span data-stu-id="5be46-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="5be46-154">前回の通話または以前の呼び出しでエラーを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="5be46-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="5be46-155">フラグは無視してもかまいません。</span><span class="sxs-lookup"><span data-stu-id="5be46-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="5be46-156">KEEP_OPEN_READWRITE または KEEP_OPEN_READONLY のどちらかが MAPI_DEFERRED_ERRORS と共に設定されている場合は、エラー繰延要求を無視できます。</span><span class="sxs-lookup"><span data-stu-id="5be46-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="5be46-157">_ulflags_に MAPI_DEFERRED_ERRORS が設定されていない場合は、以前に遅延したエラーの1つを**SaveChanges**呼び出しに対して返すことができます。</span><span class="sxs-lookup"><span data-stu-id="5be46-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="5be46-158">リモートトランスポートプロバイダーがこのメソッドの機能実装を提供するかどうかはオプションであり、実装での他の設計上の選択によって異なります。</span><span class="sxs-lookup"><span data-stu-id="5be46-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="5be46-159">このメソッドを実装する場合は、ここに記載されているドキュメントに従ってください。</span><span class="sxs-lookup"><span data-stu-id="5be46-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="5be46-160">folder オブジェクトと status オブジェクトは処理されないため、少なくともリモートトランスポートプロバイダーの**SaveChanges**の実装は、実際には何も作業を行わずに S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5be46-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5be46-161">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5be46-161">Notes to callers</span></span>

<span data-ttu-id="5be46-162">クライアントが KEEP_OPEN_READONLY に合格した場合は、 [imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出してから、再度**SaveChanges**を呼び出すと、同じ実装が失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5be46-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="5be46-163">KEEP_OPEN_READWRITE を設定した呼び出しから MAPI_E_NO_ACCESS を受信した後、そのオブジェクトに対する読み取り/書き込みアクセス許可が引き続き付与されます。</span><span class="sxs-lookup"><span data-stu-id="5be46-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="5be46-164">再度、 **SaveChanges**を呼び出すことができます。 KEEP_OPEN_READONLY フラグを渡すか、KEEP_OPEN_SUFFIX を使用してフラグを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5be46-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="5be46-165">プロバイダーが KEEP_OPEN_READWRITE フラグをサポートしているかどうかは、プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="5be46-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="5be46-166">**SaveChanges**が**IUnknown:: Release**の後にのみオブジェクトで行われる呼び出しを示すには、 _ulflags_パラメーターにフラグを設定しません。</span><span class="sxs-lookup"><span data-stu-id="5be46-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="5be46-167">**SaveChanges**からのエラーは、保留中の変更を永続的にできないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5be46-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="5be46-168">さまざまなプロバイダーが、 **SaveChanges**呼び出しでのフラグの欠落を異なる方法で処理します。</span><span class="sxs-lookup"><span data-stu-id="5be46-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="5be46-169">プロバイダーによっては、この状態を KEEP_OPEN_READONLY と同じものとして扱います。他のプロバイダーは、KEEP_OPEN_READWRITE と同じように解釈します。</span><span class="sxs-lookup"><span data-stu-id="5be46-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="5be46-170">その他のプロバイダーは、 **SaveChanges**呼び出しでフラグを受信しない場合、そのオブジェクトをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="5be46-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="5be46-171">一部のプロパティ (通常は計算プロパティ) は、 **SaveChanges**を呼び出し、場合によっては**解放**されるまで処理できません。</span><span class="sxs-lookup"><span data-stu-id="5be46-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="5be46-172">添付ファイルを複数のメッセージに保存するなどの一括変更を行う場合は、 _ulflags_で MAPI_DEFERRED_ERRORS フラグを設定することにより、エラー処理を延期します。</span><span class="sxs-lookup"><span data-stu-id="5be46-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="5be46-173">複数の添付ファイルを複数のメッセージに保存する場合は、各添付ファイルに**savechanges**呼び出しを1つずつ、各メッセージに**savechanges**呼び出しを1つ行います。</span><span class="sxs-lookup"><span data-stu-id="5be46-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="5be46-174">添付ファイルの各呼び出しに対して MAPI_DEFERRED_ERRORS フラグを設定し、最後のメッセージ以外のすべてのメッセージに対して設定します。</span><span class="sxs-lookup"><span data-stu-id="5be46-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="5be46-175">**SaveChanges**が MAPI_E_OBJECT_CHANGED を返す場合は、元のオブジェクトが変更されていないかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="5be46-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="5be46-176">その場合は、変更によって以前の変更を上書きするか、別の場所に保存するかをユーザーに警告します。</span><span class="sxs-lookup"><span data-stu-id="5be46-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="5be46-177">元のオブジェクトが削除されている場合は、オブジェクトを別の場所に保存する機会をユーザーに提供するようにユーザーに警告します。</span><span class="sxs-lookup"><span data-stu-id="5be46-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="5be46-178">開いているオブジェクトが削除されている場合、FORCE_SAVE フラグを使用して**SaveChanges**を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="5be46-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="5be46-179">**SaveChanges**がエラーを返す場合、 _ulflags_パラメーターに設定されているフラグに関係なく、変更を保存しようとしたオブジェクトは開いたままになります。</span><span class="sxs-lookup"><span data-stu-id="5be46-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5be46-180">_ulflags_ NON_EMS_XP_SAVE および SPAMFILTER_ONSAVE は、現在のダウンロード可能なヘッダーファイルでは定義されていない場合があります。その場合は、次の値を使用してコードに追加できます。 >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="5be46-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="5be46-181">詳細については、「 [MAPI プロパティの保存](saving-mapi-properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5be46-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5be46-182">関連項目</span><span class="sxs-lookup"><span data-stu-id="5be46-182">See also</span></span>



[<span data-ttu-id="5be46-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="5be46-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="5be46-184">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5be46-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="5be46-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5be46-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="5be46-186">MAPI プロパティの保存</span><span class="sxs-lookup"><span data-stu-id="5be46-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

