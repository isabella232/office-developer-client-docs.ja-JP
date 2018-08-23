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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c12750b7899403e62b9c1603615e9fd6caa95eca
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569527"
---
# <a name="imapipropsavechanges"></a><span data-ttu-id="364c6-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="364c6-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="364c6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="364c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="364c6-105">前回の保存操作以降は、オブジェクトに対して行われた変更を永続的になります。</span><span class="sxs-lookup"><span data-stu-id="364c6-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="364c6-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="364c6-106">Parameters</span></span>

 <span data-ttu-id="364c6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="364c6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="364c6-108">[in]**IMAPIProp::SaveChanges**メソッドが呼び出されたときにオブジェクトの動作を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="364c6-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="364c6-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="364c6-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="364c6-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="364c6-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="364c6-111">Microsoft Exchange Server のメッセージが配信されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="364c6-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="364c6-112">このフラグは、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを使用して組み合わせて使用する必要があり、ITEMPROC_FORCE を示すフラグを PST ストア、メッセージの対象とするルールの処理のいずれかの個人用フォルダー ファイル (PST) のストアに通知する前に到着したメッセージをリッスンしているクライアント。</span><span class="sxs-lookup"><span data-stu-id="364c6-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="364c6-113">このルールの処理で作成される[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)である場合、Exchange Server ではないサーバーで Exchange Server の新しいメッセージにのみ適用されますが既に処理が、メッセージのルール。</span><span class="sxs-lookup"><span data-stu-id="364c6-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="364c6-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="364c6-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="364c6-115">オブジェクトに加えられた直前の変更をオーバーライドする、オブジェクトに変更を書き込むし、オブジェクトを閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="364c6-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="364c6-116">操作を完了するのには、読み取り/書き込みアクセス許可を設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="364c6-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="364c6-117">**Savechanges メソッド**の呼び出し前に、MAPI_E_OBJECT_CHANGED が返された後は、FORCE_SAVE フラグを使用します。</span><span class="sxs-lookup"><span data-stu-id="364c6-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="364c6-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="364c6-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="364c6-119">変更をコミットする必要があり、オブジェクトは読み込み用にオープンして保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="364c6-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="364c6-120">追加の変更は行われません。</span><span class="sxs-lookup"><span data-stu-id="364c6-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="364c6-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="364c6-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="364c6-122">変更をコミットする必要があり、オブジェクトは、読み取り/書き込みアクセス許可も開いたまま必要があります。</span><span class="sxs-lookup"><span data-stu-id="364c6-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="364c6-123">このフラグは通常、読み取り/書き込みのアクセス許可オブジェクトを最初に開いたときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="364c6-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="364c6-124">オブジェクトへのそれ以降の変更が許可されています。</span><span class="sxs-lookup"><span data-stu-id="364c6-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="364c6-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="364c6-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="364c6-126">正常に完了が完全にコミットされた変更前に、 **SaveChanges**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="364c6-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="364c6-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="364c6-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="364c6-128">フィルターが保存されているメッセージに迷惑メールを有効に</span><span class="sxs-lookup"><span data-stu-id="364c6-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="364c6-129">スパムのフィルタ リングのサポートは、送信者の電子メール アドレスの種類は、簡易メール転送プロトコル (SMTP)、メッセージは個人用フォルダー ファイル (PST) のストアに保存されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="364c6-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="364c6-130">�߂�l</span><span class="sxs-lookup"><span data-stu-id="364c6-130">Return value</span></span>

<span data-ttu-id="364c6-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="364c6-131">S_OK</span></span> 
  
> <span data-ttu-id="364c6-132">変更のコミットに成功しました。</span><span class="sxs-lookup"><span data-stu-id="364c6-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="364c6-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="364c6-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="364c6-134">**SaveChanges**できないオブジェクトを開いたまま読み取り専用のアクセス許可の場合は KEEP_OPEN_READONLY セット、または読み取り/書き込み権限 KEEP_OPEN_READWRITE が設定されている場合。</span><span class="sxs-lookup"><span data-stu-id="364c6-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="364c6-135">変更のコミットはありません。</span><span class="sxs-lookup"><span data-stu-id="364c6-135">No changes are committed.</span></span> 
    
<span data-ttu-id="364c6-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="364c6-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="364c6-137">オブジェクトは、開かれた後に変更されました。</span><span class="sxs-lookup"><span data-stu-id="364c6-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="364c6-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="364c6-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="364c6-139">開かれた後、オブジェクトが削除されました。</span><span class="sxs-lookup"><span data-stu-id="364c6-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="364c6-140">注釈</span><span class="sxs-lookup"><span data-stu-id="364c6-140">Remarks</span></span>

<span data-ttu-id="364c6-141">**IMAPIProp::SaveChanges**メソッドでは、プロパティの変更を永続的に処理する場合、メッセージ、添付ファイル、アドレス帳コンテナー、およびメッセージングのユーザー オブジェクトのトランザクション モデルをサポートするオブジェクトになります。</span><span class="sxs-lookup"><span data-stu-id="364c6-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="364c6-142">フォルダー、メッセージ ストア、およびプロファイルのセクションなどのトランザクションをサポートしないオブジェクト変更永続的なすぐにします。</span><span class="sxs-lookup"><span data-stu-id="364c6-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="364c6-143">**Savechanges メソッド**の呼び出しは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="364c6-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="364c6-144">サービス プロバイダーは、すべてのプロパティが保存されるまで、そのオブジェクトのエントリ id を生成する必要はありません、ためオブジェクトの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) できない可能性がありますまで、 **SaveChanges**メソッドの後呼び出されました。</span><span class="sxs-lookup"><span data-stu-id="364c6-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="364c6-145">プロバイダーによって、KEEP_OPEN_READONLY フラグが設定されるまでの待機、 **SaveChanges**の呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="364c6-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="364c6-146">KEEP_OPEN_READONLY は、現在の呼び出しで保存する変更がオブジェクトに対して実行される最後の変更になることを示します。</span><span class="sxs-lookup"><span data-stu-id="364c6-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="364c6-147">メッセージ ストアの実装によって操作を行いますフォルダー内のメッセージは新しく作成された表示しないクライアントまで保存して、メッセージ**SaveChanges**を使用して変更[が](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)メソッドを使用して、メッセージ オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="364c6-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="364c6-148">さらに、いくつかのオブジェクトの実装を生成できません**PR_ENTRYID**プロパティまでの新しく作成されたオブジェクトの後、 **SaveChanges**が呼び出されると、およびいくつかは、KEEP_OPEN_READONLY を使用して、 **SaveChanges**が呼び出された後にのみ_ulFlags_で設定します。</span><span class="sxs-lookup"><span data-stu-id="364c6-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="364c6-149">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="364c6-149">Notes to implementers</span></span>

<span data-ttu-id="364c6-150">KEEP_OPEN_READONLY フラグを受信した場合は、オブジェクトの読み取り/書き込みアクセス権をそのままのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="364c6-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="364c6-151">ただし、プロバイダーできますしない状態のままにオブジェクト読み取り専用 KEEP_OPEN_READWRITE フラグが渡される。</span><span class="sxs-lookup"><span data-stu-id="364c6-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="364c6-152">クライアントは、複数のメッセージに複数の添付ファイルを保存するときに、すべての添付ファイルとすべてのメッセージの**SaveChanges**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="364c6-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="364c6-153">クライアントでは多くの場合は最後の 1 つを除いて、これらの呼び出しごとに MAPI_DEFERRED_ERRORS を設定します。</span><span class="sxs-lookup"><span data-stu-id="364c6-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="364c6-154">最後の呼び出しまたはそれ以前の呼び出しのいずれかのエラーを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="364c6-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="364c6-155">フラグを無視してもかまいません。</span><span class="sxs-lookup"><span data-stu-id="364c6-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="364c6-156">MAPI_DEFERRED_ERRORS と KEEP_OPEN_READWRITE または KEEP_OPEN_READONLY のいずれかが設定されている場合は、繰延の要求のエラーを無視できます。</span><span class="sxs-lookup"><span data-stu-id="364c6-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="364c6-157">延期されていたエラーのいずれかが返されることができます_ulFlags_で MAPI_DEFERRED_ERRORS が設定されていない場合、 **SaveChanges**の呼び出しをします。</span><span class="sxs-lookup"><span data-stu-id="364c6-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="364c6-158">リモート トランスポート プロバイダーがこのメソッドの実装の機能を提供するかどうかはオプションであり、他の実装では、設計上の選択によって異なります。</span><span class="sxs-lookup"><span data-stu-id="364c6-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="364c6-159">このメソッドを実装する場合は、次のマニュアルに従って。</span><span class="sxs-lookup"><span data-stu-id="364c6-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="364c6-160">フォルダー オブジェクトおよびオブジェクトの状態は処理されないため、少なくとも**SaveChanges**のリモート トランスポート プロバイダーの実装する必要があります S_OK を返します実際に作業を行うことがなく。</span><span class="sxs-lookup"><span data-stu-id="364c6-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="364c6-161">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="364c6-161">Notes to callers</span></span>

<span data-ttu-id="364c6-162">KEEP_OPEN_READONLY を渡す、 [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出すし、 **SaveChanges**を再度呼び出すクライアントに、同じ実装が失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="364c6-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="364c6-163">呼び出しから MAPI_E_NO_ACCESS を受信した後を設定すると KEEP_OPEN_READWRITE で引き続きオブジェクトへの読み取り/書き込み権限があります。</span><span class="sxs-lookup"><span data-stu-id="364c6-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="364c6-164">**SaveChanges** KEEP_OPEN_READONLY フラグまたは KEEP_OPEN_SUFFIX を持つフラグなしのいずれかを渡すことを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="364c6-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="364c6-165">プロバイダーが、KEEP_OPEN_READWRITE フラグをサポートしているかどうかは、プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="364c6-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="364c6-166">**SaveChanges**の後にオブジェクトに対して実行するだけの呼び出し**が**であることを示す、フラグを設定しない_ulFlags_パラメーターにします。</span><span class="sxs-lookup"><span data-stu-id="364c6-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="364c6-167">**SaveChanges**のエラーは、それを作成できませんでした、保留中の変更永続的なことを示します。</span><span class="sxs-lookup"><span data-stu-id="364c6-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="364c6-168">別のプロバイダーでは、異なる方法で**SaveChanges**の呼び出しにフラグがない場合を処理します。</span><span class="sxs-lookup"><span data-stu-id="364c6-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="364c6-169">プロバイダーによってこの状態と同様に処理 KEEP_OPEN_READONLY です。他のプロバイダーの解釈に KEEP_OPEN_READWRITE と同じです。</span><span class="sxs-lookup"><span data-stu-id="364c6-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="364c6-170">まだ他のプロバイダー、 **SaveChanges**の呼び出しフラグを受信しない場合、オブジェクトをシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="364c6-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="364c6-171">**SaveChanges**が呼び出されるまでと、場合によっては、**リリース**で、通常の計算されたプロパティは、いくつかのプロパティを処理できません。</span><span class="sxs-lookup"><span data-stu-id="364c6-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="364c6-172">複数のメッセージに添付ファイルを保存するなどの一括変更を加える場合は、 _ulFlags_で MAPI_DEFERRED_ERRORS フラグを設定することで処理中にエラーを延期します。</span><span class="sxs-lookup"><span data-stu-id="364c6-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="364c6-173">複数のメッセージに複数の添付ファイルを保存する場合は、1 つ**SaveChanges**の呼び出しの各添付ファイルと 1 つ**SaveChanges**の呼び出しの各メッセージを確認します。</span><span class="sxs-lookup"><span data-stu-id="364c6-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="364c6-174">最後の 1 つを除くすべてのメッセージの添付ファイルの呼び出しごとに MAPI_DEFERRED_ERRORS フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="364c6-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="364c6-175">**SaveChanges** MAPI_E_OBJECT_CHANGED が返された場合は、元のオブジェクトが変更されたかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="364c6-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="364c6-176">その場合は、変更が前の変更を上書きするか、オブジェクトを別の場所での保存を要求できるか、ユーザーと、ユーザーに警告します。</span><span class="sxs-lookup"><span data-stu-id="364c6-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="364c6-177">元のオブジェクトが削除されている場合は、別の場所にオブジェクトを保存する機会を与えるユーザーを警告します。</span><span class="sxs-lookup"><span data-stu-id="364c6-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="364c6-178">FORCE_SAVE のフラグが削除されているオブジェクトを開くには、 **SaveChanges**を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="364c6-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="364c6-179">**SaveChanges**がエラーを返した場合、オブジェクトの変更をしたまま保存開くには、 _ulFlags_パラメーターで設定されているフラグに関係なく。</span><span class="sxs-lookup"><span data-stu-id="364c6-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="364c6-180">_UlFlags_ダウンロード可能なヘッダー ファイルに現在ある NON_EMS_XP_SAVE および SPAMFILTER_ONSAVE を定義する可能性がない、場合に追加できます、次の値を使用してコード: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="364c6-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="364c6-181">詳細については、 [MAPI プロパティの保存](saving-mapi-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="364c6-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="364c6-182">関連項目</span><span class="sxs-lookup"><span data-stu-id="364c6-182">See also</span></span>



[<span data-ttu-id="364c6-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="364c6-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="364c6-184">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="364c6-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="364c6-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="364c6-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="364c6-186">MAPI プロパティの保存</span><span class="sxs-lookup"><span data-stu-id="364c6-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

