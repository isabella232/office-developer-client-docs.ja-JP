---
title: PidTagMessageFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageFlags
api_type:
- HeaderDef
ms.assetid: 7561112b-ca72-4c49-a8a0-cc1879a4e151
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f2e565dc8137edee441643a5d02a154f78737099
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802990"
---
# <a name="pidtagmessageflags-canonical-property"></a><span data-ttu-id="626ed-103">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="626ed-103">PidTagMessageFlags Canonical Property</span></span>

  
  
<span data-ttu-id="626ed-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="626ed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="626ed-105">原点とメッセージの現在の状態を示すフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="626ed-105">Contains a bitmask of flags that indicate the origin and current state of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="626ed-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="626ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="626ed-107">PR_MESSAGE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="626ed-107">PR_MESSAGE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="626ed-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="626ed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="626ed-109">0x0E07</span><span class="sxs-lookup"><span data-stu-id="626ed-109">0x0E07</span></span>  <br/> |
|<span data-ttu-id="626ed-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="626ed-110">Data type:</span></span>  <br/> |<span data-ttu-id="626ed-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="626ed-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="626ed-112">領域:</span><span class="sxs-lookup"><span data-stu-id="626ed-112">Area:</span></span>  <br/> |<span data-ttu-id="626ed-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="626ed-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="626ed-114">注釈</span><span class="sxs-lookup"><span data-stu-id="626ed-114">Remarks</span></span>

<span data-ttu-id="626ed-115">このプロパティは、送信側と関連するクライアント アプリケーションまたはストア プロバイダーによって値が異なると、転送の終了を受信の両方で公開されている nontransmittable メッセージ プロパティです。</span><span class="sxs-lookup"><span data-stu-id="626ed-115">This property is a nontransmittable message property exposed at both the sending and receiving ends of a transmission, with different values depending upon the client application or store provider involved.</span></span> <span data-ttu-id="626ed-116">このプロパティは、状態メッセージが作成され、最初に保存しし、定期的に更新されるメッセージ ストア プロバイダー、トランスポート プロバイダーでは、MAPI スプーラーによってメッセージが処理されるときにクライアントまたはメッセージのストア プロバイダーを初期化します。変更します。</span><span class="sxs-lookup"><span data-stu-id="626ed-116">This property is initialized by the client or message store provider when a message is created and saved for the first time and then updated periodically by the message store provider, a transport provider, and the MAPI spooler as the message is processed and its state changes.</span></span> 
  
<span data-ttu-id="626ed-117">このプロパティには、両方の前後に、送信メッセージと受信したメッセージのすべてのコピーが存在しています。</span><span class="sxs-lookup"><span data-stu-id="626ed-117">This property exists on a message both before and after submission, and on all copies of the received message.</span></span> <span data-ttu-id="626ed-118">受信者のプロパティではありませんが、方法が異なるかどうかを読み取るまたはされた受取人が変更に従って、各受信者に公開されます。</span><span class="sxs-lookup"><span data-stu-id="626ed-118">Although it is not a recipient property, it is exposed differently to each recipient according to whether it has been read or modified by that recipient.</span></span> 
  
<span data-ttu-id="626ed-119">次のフラグの 1 つ以上は、このプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="626ed-119">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="626ed-120">MSGFLAG_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="626ed-120">MSGFLAG_ASSOCIATED</span></span> 
  
> <span data-ttu-id="626ed-121">メッセージは、フォルダーの関連するメッセージです。</span><span class="sxs-lookup"><span data-stu-id="626ed-121">The message is an associated message of a folder.</span></span> <span data-ttu-id="626ed-122">クライアントまたはプロバイダーは、このフラグを読み取り専用のアクセスを持っています。</span><span class="sxs-lookup"><span data-stu-id="626ed-122">The client or provider has read-only access to this flag.</span></span> <span data-ttu-id="626ed-123">開封/未開封状態は保持されません、関連付けられているメッセージでは、MSGFLAG_READ フラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="626ed-123">The MSGFLAG_READ flag is ignored for associated messages, which do not retain a read/unread state.</span></span> 
    
<span data-ttu-id="626ed-124">MSGFLAG_FROMME</span><span class="sxs-lookup"><span data-stu-id="626ed-124">MSGFLAG_FROMME</span></span> 
  
> <span data-ttu-id="626ed-125">メッセージング ユーザーの送信メッセージを受信するメッセージング ユーザーがいました。</span><span class="sxs-lookup"><span data-stu-id="626ed-125">The messaging user sending was the messaging user receiving the message.</span></span> <span data-ttu-id="626ed-126">クライアントまたはプロバイダーがこのフラグを読み取り/書き込みアクセス読み取り専用と[IMAPIProp::SaveChanges](imapiprop-savechanges.md)の最初の呼び出しまでその後。</span><span class="sxs-lookup"><span data-stu-id="626ed-126">The client or provider has read/write access to this flag until the first [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call and read-only thereafter.</span></span> <span data-ttu-id="626ed-127">このフラグは、トランスポート プロバイダーによって設定されるものです。</span><span class="sxs-lookup"><span data-stu-id="626ed-127">This flag is meant to be set by the transport provider.</span></span> 
    
<span data-ttu-id="626ed-128">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="626ed-128">MSGFLAG_HASATTACH</span></span> 
  
> <span data-ttu-id="626ed-129">メッセージには、少なくとも 1 つの添付ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="626ed-129">The message has at least one attachment.</span></span> <span data-ttu-id="626ed-130">このフラグは、メッセージの**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) のプロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="626ed-130">This flag corresponds to the message's **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) property.</span></span> <span data-ttu-id="626ed-131">クライアントでは、このフラグを読み取り専用のアクセスがあります。</span><span class="sxs-lookup"><span data-stu-id="626ed-131">The client has read-only access to this flag.</span></span> 
    
<span data-ttu-id="626ed-132">MSGFLAG_NRN_PENDING</span><span class="sxs-lookup"><span data-stu-id="626ed-132">MSGFLAG_NRN_PENDING</span></span> 
  
> <span data-ttu-id="626ed-133">Nonread レポートは、メッセージを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="626ed-133">A nonread report needs to be sent for the message.</span></span> <span data-ttu-id="626ed-134">クライアントまたはプロバイダーは、このフラグを読み取り専用のアクセスを持っています。</span><span class="sxs-lookup"><span data-stu-id="626ed-134">The client or provider has read-only access to this flag.</span></span> 
    
<span data-ttu-id="626ed-135">MSGFLAG_ORIGIN_INTERNET</span><span class="sxs-lookup"><span data-stu-id="626ed-135">MSGFLAG_ORIGIN_INTERNET</span></span> 
  
> <span data-ttu-id="626ed-136">インターネット経由で受信したメッセージが到着しました。</span><span class="sxs-lookup"><span data-stu-id="626ed-136">The incoming message arrived over the Internet.</span></span> <span data-ttu-id="626ed-137">組織の外部またはゲートウェイが考えることはできません信頼できるソースから発生します。</span><span class="sxs-lookup"><span data-stu-id="626ed-137">It originated either outside the organization or from a source the gateway cannot consider trusted.</span></span> <span data-ttu-id="626ed-138">クライアントは、ユーザーに適切なメッセージを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="626ed-138">The client should display an appropriate message to the user.</span></span> <span data-ttu-id="626ed-139">トランスポート プロバイダーは、このフラグを設定します。クライアントでは、読み取り専用アクセスがあります。</span><span class="sxs-lookup"><span data-stu-id="626ed-139">Transport providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="626ed-140">MSGFLAG_ORIGIN_MISC_EXT</span><span class="sxs-lookup"><span data-stu-id="626ed-140">MSGFLAG_ORIGIN_MISC_EXT</span></span> 
  
> <span data-ttu-id="626ed-141">外部リンク以外は、X.400、またはインターネット経由で受信したメッセージが到着しました。</span><span class="sxs-lookup"><span data-stu-id="626ed-141">The incoming message arrived over an external link other than X.400 or the Internet.</span></span> <span data-ttu-id="626ed-142">組織の外部またはゲートウェイが考えることはできません信頼できるソースから発生します。</span><span class="sxs-lookup"><span data-stu-id="626ed-142">It originated either outside the organization or from a source the gateway cannot consider trusted.</span></span> <span data-ttu-id="626ed-143">クライアントは、ユーザーに適切なメッセージを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="626ed-143">The client should display an appropriate message to the user.</span></span> <span data-ttu-id="626ed-144">トランスポート プロバイダーは、このフラグを設定します。クライアントでは、読み取り専用アクセスがあります。</span><span class="sxs-lookup"><span data-stu-id="626ed-144">Transport providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="626ed-145">MSGFLAG_ORIGIN_X400</span><span class="sxs-lookup"><span data-stu-id="626ed-145">MSGFLAG_ORIGIN_X400</span></span> 
  
> <span data-ttu-id="626ed-146">X.400 リンク経由で受信したメッセージが到着しました。</span><span class="sxs-lookup"><span data-stu-id="626ed-146">The incoming message arrived over an X.400 link.</span></span> <span data-ttu-id="626ed-147">組織の外部またはゲートウェイが考えることはできません信頼できるソースから発生します。</span><span class="sxs-lookup"><span data-stu-id="626ed-147">It originated either outside the organization or from a source the gateway cannot consider trusted.</span></span> <span data-ttu-id="626ed-148">クライアントは、ユーザーに適切なメッセージを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="626ed-148">The client should display an appropriate message to the user.</span></span> <span data-ttu-id="626ed-149">トランスポート プロバイダーは、このフラグを設定します。クライアントでは、読み取り専用アクセスがあります。</span><span class="sxs-lookup"><span data-stu-id="626ed-149">Transport providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="626ed-150">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="626ed-150">MSGFLAG_READ</span></span> 
  
> <span data-ttu-id="626ed-151">メッセージは読み取りとしてマークします。</span><span class="sxs-lookup"><span data-stu-id="626ed-151">The message is marked as having been read.</span></span> <span data-ttu-id="626ed-152">これは、 [IMessage::SetReadFlag](imessage-setreadflag.md)または[IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)任意の時点の呼び出しの結果として発生します。</span><span class="sxs-lookup"><span data-stu-id="626ed-152">This can occur as the result of a call at any time to [IMessage::SetReadFlag](imessage-setreadflag.md) or [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span> <span data-ttu-id="626ed-153">クライアントは、最初にメッセージを保存する前に、メッセージの**IMAPIProp::SetProps**メソッドを呼び出すことによってこのフラグを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="626ed-153">Clients can also set this flag by calling a message's **IMAPIProp::SetProps** method before the message has been saved for the first time.</span></span> <span data-ttu-id="626ed-154">**MSGFLAG_ASSOCIATED**フラグが設定されている場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="626ed-154">This flag is ignored if the **MSGFLAG_ASSOCIATED** flag is set.</span></span> 
    
<span data-ttu-id="626ed-155">MSGFLAG_RESEND</span><span class="sxs-lookup"><span data-stu-id="626ed-155">MSGFLAG_RESEND</span></span> 
  
> <span data-ttu-id="626ed-156">メッセージには、配信不能レポートの再送信の操作の要求が含まれています。</span><span class="sxs-lookup"><span data-stu-id="626ed-156">The message includes a request for a resend operation with a nondelivery report.</span></span> <span data-ttu-id="626ed-157">クライアントまたはプロバイダーがこのフラグを読み取り/書き込みアクセス読み取り専用と[IMAPIProp::SaveChanges](imapiprop-savechanges.md)の最初の呼び出しまでその後。</span><span class="sxs-lookup"><span data-stu-id="626ed-157">The client or provider has read/write access to this flag until the first [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call and read-only thereafter.</span></span> 
    
<span data-ttu-id="626ed-158">MSGFLAG_RN_PENDING</span><span class="sxs-lookup"><span data-stu-id="626ed-158">MSGFLAG_RN_PENDING</span></span> 
  
> <span data-ttu-id="626ed-159">リードのレポートは、メッセージを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="626ed-159">A read report needs to be sent for the message.</span></span> <span data-ttu-id="626ed-160">クライアントまたはプロバイダーは、このフラグを読み取り専用のアクセスを持っています。</span><span class="sxs-lookup"><span data-stu-id="626ed-160">The client or provider has read-only access to this flag.</span></span> 
    
<span data-ttu-id="626ed-161">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="626ed-161">MSGFLAG_SUBMIT</span></span> 
  
> <span data-ttu-id="626ed-162">[IMessage::SubmitMessage](imessage-submitmessage.md)への呼び出しの結果を送信するメッセージをマークします。</span><span class="sxs-lookup"><span data-stu-id="626ed-162">The message is marked for sending as a result of a call to [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> <span data-ttu-id="626ed-163">メッセージ ストア プロバイダーは、このフラグを設定します。クライアントでは、読み取り専用アクセスがあります。</span><span class="sxs-lookup"><span data-stu-id="626ed-163">Message store providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="626ed-164">MSGFLAG_UNMODIFIED</span><span class="sxs-lookup"><span data-stu-id="626ed-164">MSGFLAG_UNMODIFIED</span></span> 
  
> <span data-ttu-id="626ed-165">送信メッセージが保存されている最初の時点から変更されていません。配信された後に受信したメッセージが変更されていません。</span><span class="sxs-lookup"><span data-stu-id="626ed-165">The outgoing message has not been modified since the first time that it was saved; the incoming message has not been modified since it was delivered.</span></span> 
    
<span data-ttu-id="626ed-166">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="626ed-166">MSGFLAG_UNSENT</span></span> 
  
> <span data-ttu-id="626ed-167">メッセージは、まだ構成されています。</span><span class="sxs-lookup"><span data-stu-id="626ed-167">The message is still being composed.</span></span> <span data-ttu-id="626ed-168">保存されますが、まだ送信されていません。</span><span class="sxs-lookup"><span data-stu-id="626ed-168">It is saved, but has not been sent.</span></span> <span data-ttu-id="626ed-169">クライアントまたはプロバイダーがこのフラグを読み取り/書き込みアクセス読み取り専用と[IMAPIProp::SaveChanges](imapiprop-savechanges.md)の最初の呼び出しまでその後。</span><span class="sxs-lookup"><span data-stu-id="626ed-169">The client or provider has read/write access to this flag until the first [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call and read-only thereafter.</span></span> <span data-ttu-id="626ed-170">クライアントがメッセージの送信時にこのフラグを設定しない場合は、メッセージ ストア プロバイダーを設定、 **IMessage::SubmitMessage**が呼び出されたときにします。</span><span class="sxs-lookup"><span data-stu-id="626ed-170">If a client doesn't set this flag by the time the message is sent, the message store provider sets it when **IMessage::SubmitMessage** is called.</span></span> <span data-ttu-id="626ed-171">通常、メッセージが送信された後、このフラグはクリアされます。</span><span class="sxs-lookup"><span data-stu-id="626ed-171">Typically, this flag is cleared after the message is sent.</span></span> 
    
<span data-ttu-id="626ed-172">クライアントまたはメッセージ ストア プロバイダーは、フラグの値を読み取るための[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すことによって、いつでも、メッセージの現在の状態を確認できます。</span><span class="sxs-lookup"><span data-stu-id="626ed-172">A client or message store provider can check the current state of the message at any time by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method to read the flag values.</span></span> <span data-ttu-id="626ed-173">クライアントまたはプロバイダーでは、現在読み取り/書き込みアクセス権を持つ任意のフラグを変更するのには[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出すこともできます。</span><span class="sxs-lookup"><span data-stu-id="626ed-173">The client or provider can also call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to change any flags that currently have read/write access.</span></span> 
  
<span data-ttu-id="626ed-174">フラグのいくつかは常に読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="626ed-174">Several of the flags are always read-only.</span></span> <span data-ttu-id="626ed-175">限り**IMAPIProp::SetProps**は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッド、およびその後の最初の呼び出しに読み取り専用になるまでは読み取り/書き込みがあります。</span><span class="sxs-lookup"><span data-stu-id="626ed-175">Some are read/write until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and thereafter become read-only as far as **IMAPIProp::SetProps** is concerned.</span></span> <span data-ttu-id="626ed-176">、MSGFLAG_READ、これらの 1 つは、 [IMessage::SetReadFlag](imessage-setreadflag.md)または[IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)を後で変更できます。</span><span class="sxs-lookup"><span data-stu-id="626ed-176">One of these, MSGFLAG_READ, can be changed later through [IMessage::SetReadFlag](imessage-setreadflag.md) or [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span> 
  
<span data-ttu-id="626ed-177">このプロパティの初期値は通常は、送信または変更されたされていないメッセージを示すには、MSGFLAG_UNSENT と MSGFLAG_UNMODIFIED。</span><span class="sxs-lookup"><span data-stu-id="626ed-177">The initial values for this property are typically MSGFLAG_UNSENT and MSGFLAG_UNMODIFIED to indicate a message that has not yet been sent or changed.</span></span> <span data-ttu-id="626ed-178">2 回目のメッセージが保存されると、メッセージ ストア プロバイダーは、MSGFLAG_UNMODIFIED フラグをクリアします。</span><span class="sxs-lookup"><span data-stu-id="626ed-178">When a message is saved for the second time, the message store provider clears the MSGFLAG_UNMODIFIED flag.</span></span> <span data-ttu-id="626ed-179">メッセージ ストア プロバイダーがメッセージを保存するときに設定できる別の値は、MSGFLAG_HASATTACH フラグをメッセージに 1 つまたは複数の添付ファイルがあることを示します。</span><span class="sxs-lookup"><span data-stu-id="626ed-179">Another value that a message store provider can set when a message is saved is the MSGFLAG_HASATTACH flag, indicating that the message has one or more attachments.</span></span> <span data-ttu-id="626ed-180">**PR_HASATTACH**プロパティは、この設定から計算されます。</span><span class="sxs-lookup"><span data-stu-id="626ed-180">The **PR_HASATTACH** property is computed from this setting.</span></span> 
  
<span data-ttu-id="626ed-181">クライアントがメッセージを送信する[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出すと、メッセージ ストア プロバイダー コピーでは、MAPI スプーラーを無効になり、MSGFLAG_SUBMIT フラグを設定することによってこのプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="626ed-181">When a client calls the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message, the message store provider makes a copy of it for the MAPI spooler and updates this property by setting the MSGFLAG_SUBMIT flag.</span></span> <span data-ttu-id="626ed-182">メッセージ ストア プロバイダーは、まだ設定されていない場合にも MSGFLAG_UNSENT を設定します。</span><span class="sxs-lookup"><span data-stu-id="626ed-182">The message store provider also sets MSGFLAG_UNSENT if it is not yet set.</span></span> <span data-ttu-id="626ed-183">MSGFLAG_SUBMIT であることを示します**SubmitMessage**が呼び出されると、送信プロセスを開始し、メッセージがクライアントに読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="626ed-183">MSGFLAG_SUBMIT indicates that **SubmitMessage** has been called, beginning the send process, and that the message is now read-only to the client.</span></span> <span data-ttu-id="626ed-184">MSGFLAG_UNSENT では、MAPI スプーラーがメッセージを処理していることを示します。</span><span class="sxs-lookup"><span data-stu-id="626ed-184">MSGFLAG_UNSENT indicates that the MAPI spooler is handling the message.</span></span> <span data-ttu-id="626ed-185">送信処理がキャンセルされた場合、メッセージ ストア プロバイダーは、このフラグをリセットします。</span><span class="sxs-lookup"><span data-stu-id="626ed-185">If the send process is canceled, the message store provider resets this flag.</span></span> 
  
<span data-ttu-id="626ed-186">配信用のトランスポート プロバイダーにメッセージを指定すると場合送信元メッセージング サーバーで同じアカウントでメッセージを受信しましたと、トランスポート プロバイダーは、MSGFLAG_FROMME フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="626ed-186">When the message is given to a transport provider for delivery, the transport provider sets the MSGFLAG_FROMME flag if the sender had the same account on the messaging server as the message was received on.</span></span> <span data-ttu-id="626ed-187">トランスポート プロバイダーは、現在ログオンしているユーザーから送信された受信メッセージの MSGFLAG_FROMME を設定します。</span><span class="sxs-lookup"><span data-stu-id="626ed-187">Transport providers set MSGFLAG_FROMME for an incoming message that was sent by the currently logged on user.</span></span> <span data-ttu-id="626ed-188">クライアントは、送信者の名前よりも [送信済みアイテム フォルダーの内容の表に受取人の名前を表示するのに方が適切であると判断するのには、この値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="626ed-188">A client can use this value to determine that it is more appropriate to show recipient names in the contents table of the Sent Items folder than sender names.</span></span> <span data-ttu-id="626ed-189">構成処理中に保存して送信されていないメッセージは、送信者の名前ではなく、受信者の名前を使用しても表示されます。</span><span class="sxs-lookup"><span data-stu-id="626ed-189">Messages that have been saved during the composition process and not yet sent should also be displayed with recipient names rather than sender names.</span></span> 
  
<span data-ttu-id="626ed-190">着信メッセージの場合は、メッセージ ストア プロバイダーは、読み取りの状態をリセットするのには MSGFLAG_READ フラグをクリアします。</span><span class="sxs-lookup"><span data-stu-id="626ed-190">For an incoming message, a message store provider clears the MSGFLAG_READ flag to reset its read status.</span></span> <span data-ttu-id="626ed-191">クライアントを設定または読み取りステータスを変更して、メッセージの[IMessage::SetReadFlag](imessage-setreadflag.md)メソッドまたはそのフォルダーの[IMAPIFolder のいずれかを呼び出すことにより、読み取りおよび nonread のレポートの送信を制御する必要がある場合、MSGFLAG_READ フラグをオフにできます。SetReadFlags](imapifolder-setreadflags.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="626ed-191">A client can set or clear the MSGFLAG_READ flag when it is necessary to change the read status and control the sending of read and nonread reports, by calling either the message's [IMessage::SetReadFlag](imessage-setreadflag.md) method or its folder's [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) method.</span></span> <span data-ttu-id="626ed-192">これらのメソッドを実装するには、オブジェクト以外のオブジェクトの主な違いは、フォルダー メソッドは、1 つ、複数、またはすべてのフォルダーにメッセージに影響ことができます。</span><span class="sxs-lookup"><span data-stu-id="626ed-192">The main difference between these methods, other than the object implementing them, is that the folder method can affect one, several, or all of the messages in the folder.</span></span> <span data-ttu-id="626ed-193">メッセージのメソッドでは、1 つのメッセージに影響します。</span><span class="sxs-lookup"><span data-stu-id="626ed-193">The message method affects a single message.</span></span> 
  
<span data-ttu-id="626ed-194">クライアントも MSGFLAG_ORIGIN_X400、MSGFLAG_ORIGIN_INTERNET、および MSGFLAG_ORIGIN_MISC_EXT のフラグを受信したメッセージをテストしてください。</span><span class="sxs-lookup"><span data-stu-id="626ed-194">A client should also test an incoming message for the MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET, and MSGFLAG_ORIGIN_MISC_EXT flags.</span></span> <span data-ttu-id="626ed-195">これらのフラグは、受信トランスポート プロバイダーによって設定され、ゲートウェイが信頼関係を考慮することはできませんが、ソースからメッセージが到着したことを示します。</span><span class="sxs-lookup"><span data-stu-id="626ed-195">These flags are set by the inbound transport provider and indicate that the message arrived from a source that the gateway cannot consider trusted.</span></span> <span data-ttu-id="626ed-196">つまり、メッセージの送信元組織外にあるか、または内部的にですが、ゲートウェイとわかっていないワークステーションから。</span><span class="sxs-lookup"><span data-stu-id="626ed-196">This means the message originated either outside the organization, or internally but from a workstation not known to the gateway.</span></span> <span data-ttu-id="626ed-197">どのような場合は、送信者の身元を確認することがない可能性がありますと、組織内にコンピューター ウイルスを導入する際のリスクがあります。</span><span class="sxs-lookup"><span data-stu-id="626ed-197">In any case, the identity of the sender may not be confirmed, and there is a risk of introducing a computer virus into the organization.</span></span> <span data-ttu-id="626ed-198">クライアントは、ユーザーに警告メッセージを表示し、開かずにメッセージを削除するオプションを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="626ed-198">The client should display a warning message to the user and offer an option of deleting the message without opening it.</span></span> 
  
<span data-ttu-id="626ed-199">メッセージ ストア プロバイダーは、受信メッセージの MSGFLAG_UNMODIFIED フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="626ed-199">Message store providers set the MSGFLAG_UNMODIFIED flag for incoming messages.</span></span> <span data-ttu-id="626ed-200">MSGFLAG_UNMODIFIED は、メッセージが配信以降変更されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="626ed-200">MSGFLAG_UNMODIFIED indicates that a message has not been changed since delivery.</span></span> <span data-ttu-id="626ed-201">メッセージ ストア プロバイダーによって設定された後、クライアントはこの値をクリアできません。</span><span class="sxs-lookup"><span data-stu-id="626ed-201">A client cannot clear this value after it has been set by a message store provider.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="626ed-202">関連リソース</span><span class="sxs-lookup"><span data-stu-id="626ed-202">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="626ed-203">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="626ed-203">Protocol specifications</span></span>

<span data-ttu-id="626ed-204">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="626ed-204">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="626ed-205">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="626ed-205">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="626ed-206">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="626ed-206">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="626ed-207">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="626ed-207">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="626ed-208">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="626ed-208">Header files</span></span>

<span data-ttu-id="626ed-209">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="626ed-209">Mapidefs.h</span></span>
  
> <span data-ttu-id="626ed-210">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="626ed-210">Provides data type definitions.</span></span>
    
<span data-ttu-id="626ed-211">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="626ed-211">Mapitags.h</span></span>
  
> <span data-ttu-id="626ed-212">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="626ed-212">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="626ed-213">関連項目</span><span class="sxs-lookup"><span data-stu-id="626ed-213">See also</span></span>



[<span data-ttu-id="626ed-214">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="626ed-214">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)


[<span data-ttu-id="626ed-215">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="626ed-215">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="626ed-216">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="626ed-216">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="626ed-217">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="626ed-217">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="626ed-218">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="626ed-218">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

