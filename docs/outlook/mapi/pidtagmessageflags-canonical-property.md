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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5b660b592e77279a4d60f3a036724341352c9b6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325744"
---
# <a name="pidtagmessageflags-canonical-property"></a><span data-ttu-id="72001-103">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="72001-103">PidTagMessageFlags Canonical Property</span></span>

  
  
<span data-ttu-id="72001-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72001-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72001-105">メッセージの発生元と現在の状態を示すフラグのビットマスクが含まれる。</span><span class="sxs-lookup"><span data-stu-id="72001-105">Contains a bitmask of flags that indicate the origin and current state of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72001-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="72001-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72001-107">PR_MESSAGE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="72001-107">PR_MESSAGE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="72001-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="72001-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72001-109">0x0E07</span><span class="sxs-lookup"><span data-stu-id="72001-109">0x0E07</span></span>  <br/> |
|<span data-ttu-id="72001-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="72001-110">Data type:</span></span>  <br/> |<span data-ttu-id="72001-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="72001-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="72001-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="72001-112">Area:</span></span>  <br/> |<span data-ttu-id="72001-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="72001-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72001-114">注釈</span><span class="sxs-lookup"><span data-stu-id="72001-114">Remarks</span></span>

<span data-ttu-id="72001-115">このプロパティは、送信の送信側と受信側の両方で公開される送信不可のメッセージ プロパティで、クライアント アプリケーションまたはストア プロバイダーに応じて異なる値を使用します。</span><span class="sxs-lookup"><span data-stu-id="72001-115">This property is a nontransmittable message property exposed at both the sending and receiving ends of a transmission, with different values depending upon the client application or store provider involved.</span></span> <span data-ttu-id="72001-116">このプロパティは、メッセージが初めて作成および保存され、メッセージが処理され、状態が変更されると、メッセージ ストア プロバイダー、トランスポート プロバイダー、MAPI スプーラーによって定期的に更新されると、クライアントまたはメッセージ ストア プロバイダーによって初期化されます。</span><span class="sxs-lookup"><span data-stu-id="72001-116">This property is initialized by the client or message store provider when a message is created and saved for the first time and then updated periodically by the message store provider, a transport provider, and the MAPI spooler as the message is processed and its state changes.</span></span> 
  
<span data-ttu-id="72001-117">このプロパティは、送信の前と送信後の両方のメッセージと、受信したメッセージのすべてのコピーに存在します。</span><span class="sxs-lookup"><span data-stu-id="72001-117">This property exists on a message both before and after submission, and on all copies of the received message.</span></span> <span data-ttu-id="72001-118">受信者プロパティではありませんが、受信者によって読み取りまたは変更されたかどうかに応じて、各受信者に対して異なる方法で公開されます。</span><span class="sxs-lookup"><span data-stu-id="72001-118">Although it is not a recipient property, it is exposed differently to each recipient according to whether it has been read or modified by that recipient.</span></span> 
  
<span data-ttu-id="72001-119">このプロパティには、次のフラグを 1 つ以上設定できます。</span><span class="sxs-lookup"><span data-stu-id="72001-119">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="72001-120">MSGFLAG_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="72001-120">MSGFLAG_ASSOCIATED</span></span> 
  
> <span data-ttu-id="72001-121">メッセージは、フォルダーの関連付けられたメッセージです。</span><span class="sxs-lookup"><span data-stu-id="72001-121">The message is an associated message of a folder.</span></span> <span data-ttu-id="72001-122">クライアントまたはプロバイダーには、このフラグへの読み取り専用アクセス権があります。</span><span class="sxs-lookup"><span data-stu-id="72001-122">The client or provider has read-only access to this flag.</span></span> <span data-ttu-id="72001-123">関連MSGFLAG_READ、読み取り/未読状態を保持しない場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="72001-123">The MSGFLAG_READ flag is ignored for associated messages, which do not retain a read/unread state.</span></span> 
    
<span data-ttu-id="72001-124">MSGFLAG_FROMME</span><span class="sxs-lookup"><span data-stu-id="72001-124">MSGFLAG_FROMME</span></span> 
  
> <span data-ttu-id="72001-125">送信するメッセージング ユーザーは、メッセージを受信するメッセージング ユーザーでした。</span><span class="sxs-lookup"><span data-stu-id="72001-125">The messaging user sending was the messaging user receiving the message.</span></span> <span data-ttu-id="72001-126">クライアントまたはプロバイダーは、最初の [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 呼び出しまでこのフラグへの読み取り/書き込みアクセス権を持ち、その後は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="72001-126">The client or provider has read/write access to this flag until the first [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call and read-only thereafter.</span></span> <span data-ttu-id="72001-127">このフラグは、トランスポート プロバイダーによって設定することを意図しています。</span><span class="sxs-lookup"><span data-stu-id="72001-127">This flag is meant to be set by the transport provider.</span></span> 
    
<span data-ttu-id="72001-128">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="72001-128">MSGFLAG_HASATTACH</span></span> 
  
> <span data-ttu-id="72001-129">メッセージには少なくとも 1 つの添付ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="72001-129">The message has at least one attachment.</span></span> <span data-ttu-id="72001-130">このフラグは、メッセージのプロパティ ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md) **)** PR_HASATTACHに対応します。</span><span class="sxs-lookup"><span data-stu-id="72001-130">This flag corresponds to the message's **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) property.</span></span> <span data-ttu-id="72001-131">クライアントには、このフラグへの読み取り専用アクセス権があります。</span><span class="sxs-lookup"><span data-stu-id="72001-131">The client has read-only access to this flag.</span></span> 
    
<span data-ttu-id="72001-132">MSGFLAG_NRN_PENDING</span><span class="sxs-lookup"><span data-stu-id="72001-132">MSGFLAG_NRN_PENDING</span></span> 
  
> <span data-ttu-id="72001-133">メッセージに対して読み取り以外のレポートを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72001-133">A nonread report needs to be sent for the message.</span></span> <span data-ttu-id="72001-134">クライアントまたはプロバイダーには、このフラグへの読み取り専用アクセス権があります。</span><span class="sxs-lookup"><span data-stu-id="72001-134">The client or provider has read-only access to this flag.</span></span> 
    
<span data-ttu-id="72001-135">MSGFLAG_ORIGIN_INTERNET</span><span class="sxs-lookup"><span data-stu-id="72001-135">MSGFLAG_ORIGIN_INTERNET</span></span> 
  
> <span data-ttu-id="72001-136">受信メッセージがインターネット上に到着しました。</span><span class="sxs-lookup"><span data-stu-id="72001-136">The incoming message arrived over the Internet.</span></span> <span data-ttu-id="72001-137">これは、組織外またはゲートウェイが信頼できると見なすソースのいずれかから発生します。</span><span class="sxs-lookup"><span data-stu-id="72001-137">It originated either outside the organization or from a source the gateway cannot consider trusted.</span></span> <span data-ttu-id="72001-138">クライアントは、ユーザーに適切なメッセージを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72001-138">The client should display an appropriate message to the user.</span></span> <span data-ttu-id="72001-139">トランスポート プロバイダーは、このフラグを設定します。クライアントには読み取り専用アクセス権があります。</span><span class="sxs-lookup"><span data-stu-id="72001-139">Transport providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="72001-140">MSGFLAG_ORIGIN_MISC_EXT</span><span class="sxs-lookup"><span data-stu-id="72001-140">MSGFLAG_ORIGIN_MISC_EXT</span></span> 
  
> <span data-ttu-id="72001-141">受信メッセージは、X.400 またはインターネット以外の外部リンクを通して届きました。</span><span class="sxs-lookup"><span data-stu-id="72001-141">The incoming message arrived over an external link other than X.400 or the Internet.</span></span> <span data-ttu-id="72001-142">これは、組織外またはゲートウェイが信頼できると見なすソースのいずれかから発生します。</span><span class="sxs-lookup"><span data-stu-id="72001-142">It originated either outside the organization or from a source the gateway cannot consider trusted.</span></span> <span data-ttu-id="72001-143">クライアントは、ユーザーに適切なメッセージを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72001-143">The client should display an appropriate message to the user.</span></span> <span data-ttu-id="72001-144">トランスポート プロバイダーは、このフラグを設定します。クライアントには読み取り専用アクセス権があります。</span><span class="sxs-lookup"><span data-stu-id="72001-144">Transport providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="72001-145">MSGFLAG_ORIGIN_X400</span><span class="sxs-lookup"><span data-stu-id="72001-145">MSGFLAG_ORIGIN_X400</span></span> 
  
> <span data-ttu-id="72001-146">受信メッセージが X.400 リンクを越え到着しました。</span><span class="sxs-lookup"><span data-stu-id="72001-146">The incoming message arrived over an X.400 link.</span></span> <span data-ttu-id="72001-147">これは、組織外またはゲートウェイが信頼できると見なすソースのいずれかから発生します。</span><span class="sxs-lookup"><span data-stu-id="72001-147">It originated either outside the organization or from a source the gateway cannot consider trusted.</span></span> <span data-ttu-id="72001-148">クライアントは、ユーザーに適切なメッセージを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72001-148">The client should display an appropriate message to the user.</span></span> <span data-ttu-id="72001-149">トランスポート プロバイダーは、このフラグを設定します。クライアントには読み取り専用アクセス権があります。</span><span class="sxs-lookup"><span data-stu-id="72001-149">Transport providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="72001-150">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="72001-150">MSGFLAG_READ</span></span> 
  
> <span data-ttu-id="72001-151">メッセージは読み取り済みとしてマークされます。</span><span class="sxs-lookup"><span data-stu-id="72001-151">The message is marked as having been read.</span></span> <span data-ttu-id="72001-152">これは [、IMessage::SetReadFlag](imessage-setreadflag.md) または [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)への呼び出しの結果として発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="72001-152">This can occur as the result of a call at any time to [IMessage::SetReadFlag](imessage-setreadflag.md) or [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span> <span data-ttu-id="72001-153">クライアントは、メッセージが初めて保存される前に、メッセージの **IMAPIProp::SetProps** メソッドを呼び出すことによって、このフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="72001-153">Clients can also set this flag by calling a message's **IMAPIProp::SetProps** method before the message has been saved for the first time.</span></span> <span data-ttu-id="72001-154">このフラグは、このフラグ **がMSGFLAG_ASSOCIATED設定** されている場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="72001-154">This flag is ignored if the **MSGFLAG_ASSOCIATED** flag is set.</span></span> 
    
<span data-ttu-id="72001-155">MSGFLAG_RESEND</span><span class="sxs-lookup"><span data-stu-id="72001-155">MSGFLAG_RESEND</span></span> 
  
> <span data-ttu-id="72001-156">メッセージには、非送信レポートを使用した再送信操作の要求が含まれます。</span><span class="sxs-lookup"><span data-stu-id="72001-156">The message includes a request for a resend operation with a nondelivery report.</span></span> <span data-ttu-id="72001-157">クライアントまたはプロバイダーは、最初の [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 呼び出しまでこのフラグへの読み取り/書き込みアクセス権を持ち、その後は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="72001-157">The client or provider has read/write access to this flag until the first [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call and read-only thereafter.</span></span> 
    
<span data-ttu-id="72001-158">MSGFLAG_RN_PENDING</span><span class="sxs-lookup"><span data-stu-id="72001-158">MSGFLAG_RN_PENDING</span></span> 
  
> <span data-ttu-id="72001-159">メッセージの読み取りレポートを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72001-159">A read report needs to be sent for the message.</span></span> <span data-ttu-id="72001-160">クライアントまたはプロバイダーには、このフラグへの読み取り専用アクセス権があります。</span><span class="sxs-lookup"><span data-stu-id="72001-160">The client or provider has read-only access to this flag.</span></span> 
    
<span data-ttu-id="72001-161">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="72001-161">MSGFLAG_SUBMIT</span></span> 
  
> <span data-ttu-id="72001-162">メッセージは [、IMessage::SubmitMessage](imessage-submitmessage.md)への呼び出しの結果として送信用にマークされます。</span><span class="sxs-lookup"><span data-stu-id="72001-162">The message is marked for sending as a result of a call to [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> <span data-ttu-id="72001-163">メッセージ ストア プロバイダーは、このフラグを設定します。クライアントには読み取り専用アクセス権があります。</span><span class="sxs-lookup"><span data-stu-id="72001-163">Message store providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="72001-164">MSGFLAG_UNMODIFIED</span><span class="sxs-lookup"><span data-stu-id="72001-164">MSGFLAG_UNMODIFIED</span></span> 
  
> <span data-ttu-id="72001-165">送信メッセージは、最初に保存された時から変更されていない。受信メッセージは配信後に変更されていない。</span><span class="sxs-lookup"><span data-stu-id="72001-165">The outgoing message has not been modified since the first time that it was saved; the incoming message has not been modified since it was delivered.</span></span> 
    
<span data-ttu-id="72001-166">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="72001-166">MSGFLAG_UNSENT</span></span> 
  
> <span data-ttu-id="72001-167">メッセージはまだ構成中です。</span><span class="sxs-lookup"><span data-stu-id="72001-167">The message is still being composed.</span></span> <span data-ttu-id="72001-168">保存されますが、送信されていない。</span><span class="sxs-lookup"><span data-stu-id="72001-168">It is saved, but has not been sent.</span></span> <span data-ttu-id="72001-169">クライアントまたはプロバイダーは、最初の [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 呼び出しまでこのフラグへの読み取り/書き込みアクセス権を持ち、その後は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="72001-169">The client or provider has read/write access to this flag until the first [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call and read-only thereafter.</span></span> <span data-ttu-id="72001-170">メッセージが送信される時点でクライアントがこのフラグを設定しない場合、メッセージ ストア プロバイダーは **IMessage::SubmitMessage** が呼び出されたときにこのフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="72001-170">If a client doesn't set this flag by the time the message is sent, the message store provider sets it when **IMessage::SubmitMessage** is called.</span></span> <span data-ttu-id="72001-171">通常、このフラグはメッセージの送信後にクリアされます。</span><span class="sxs-lookup"><span data-stu-id="72001-171">Typically, this flag is cleared after the message is sent.</span></span> 
    
<span data-ttu-id="72001-172">クライアントまたはメッセージ ストア プロバイダーは [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出してフラグ値を読み取って、いつでもメッセージの現在の状態を確認できます。</span><span class="sxs-lookup"><span data-stu-id="72001-172">A client or message store provider can check the current state of the message at any time by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method to read the flag values.</span></span> <span data-ttu-id="72001-173">クライアントまたはプロバイダーは [、IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出して、現在読み取り/書き込みアクセス権を持つフラグを変更できます。</span><span class="sxs-lookup"><span data-stu-id="72001-173">The client or provider can also call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to change any flags that currently have read/write access.</span></span> 
  
<span data-ttu-id="72001-174">フラグのいくつかは、常に読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="72001-174">Several of the flags are always read-only.</span></span> <span data-ttu-id="72001-175">一部は [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドの最初の呼び出しまで読み取り/書き込みであり、 **その後、IMAPIProp::SetProps** に関する限り読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="72001-175">Some are read/write until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and thereafter become read-only as far as **IMAPIProp::SetProps** is concerned.</span></span> <span data-ttu-id="72001-176">これらの 1 つは、MSGFLAG_READ [IMessage::SetReadFlag](imessage-setreadflag.md) または [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)を使用して変更できます。</span><span class="sxs-lookup"><span data-stu-id="72001-176">One of these, MSGFLAG_READ, can be changed later through [IMessage::SetReadFlag](imessage-setreadflag.md) or [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span> 
  
<span data-ttu-id="72001-177">通常、このプロパティの初期値は、MSGFLAG_UNSENT変更されていないMSGFLAG_UNMODIFIEDメッセージを示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="72001-177">The initial values for this property are typically MSGFLAG_UNSENT and MSGFLAG_UNMODIFIED to indicate a message that has not yet been sent or changed.</span></span> <span data-ttu-id="72001-178">メッセージが 2 度目に保存される場合、メッセージ ストア プロバイダーはメッセージ MSGFLAG_UNMODIFIEDします。</span><span class="sxs-lookup"><span data-stu-id="72001-178">When a message is saved for the second time, the message store provider clears the MSGFLAG_UNMODIFIED flag.</span></span> <span data-ttu-id="72001-179">メッセージの保存時にメッセージ ストア プロバイダーが設定できるもう 1 つの値は、MSGFLAG_HASATTACH フラグで、メッセージに 1 つ以上の添付ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="72001-179">Another value that a message store provider can set when a message is saved is the MSGFLAG_HASATTACH flag, indicating that the message has one or more attachments.</span></span> <span data-ttu-id="72001-180">プロパティ **PR_HASATTACH** この設定から計算されます。</span><span class="sxs-lookup"><span data-stu-id="72001-180">The **PR_HASATTACH** property is computed from this setting.</span></span> 
  
<span data-ttu-id="72001-181">クライアントが [IMessage::SubmitMessage](imessage-submitmessage.md) メソッドを呼び出してメッセージを送信すると、メッセージ ストア プロバイダーは MAPI スプーラーのコピーを作成し、MSGFLAG_SUBMIT フラグを設定してこのプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="72001-181">When a client calls the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message, the message store provider makes a copy of it for the MAPI spooler and updates this property by setting the MSGFLAG_SUBMIT flag.</span></span> <span data-ttu-id="72001-182">メッセージ ストア プロバイダーは、まだ設定されていないMSGFLAG_UNSENTメッセージ ストア プロバイダーも設定します。</span><span class="sxs-lookup"><span data-stu-id="72001-182">The message store provider also sets MSGFLAG_UNSENT if it is not yet set.</span></span> <span data-ttu-id="72001-183">MSGFLAG_SUBMIT **SubmitMessage** が呼び出され、送信プロセスが開始され、メッセージがクライアントに対して読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="72001-183">MSGFLAG_SUBMIT indicates that **SubmitMessage** has been called, beginning the send process, and that the message is now read-only to the client.</span></span> <span data-ttu-id="72001-184">MSGFLAG_UNSENT MAPI スプーラーがメッセージを処理中かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="72001-184">MSGFLAG_UNSENT indicates that the MAPI spooler is handling the message.</span></span> <span data-ttu-id="72001-185">送信プロセスが取り消された場合、メッセージ ストア プロバイダーは、このフラグをリセットします。</span><span class="sxs-lookup"><span data-stu-id="72001-185">If the send process is canceled, the message store provider resets this flag.</span></span> 
  
<span data-ttu-id="72001-186">メッセージがトランスポート プロバイダーに配信用に与えられると、メッセージが受信されたのと同じアカウントを送信者がメッセージング サーバーに持っていた場合、トランスポート プロバイダーは MSGFLAG_FROMME フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="72001-186">When the message is given to a transport provider for delivery, the transport provider sets the MSGFLAG_FROMME flag if the sender had the same account on the messaging server as the message was received on.</span></span> <span data-ttu-id="72001-187">トランスポート プロバイダーは、MSGFLAG_FROMMEログオンしているユーザーによって送信された受信メッセージのデータを設定します。</span><span class="sxs-lookup"><span data-stu-id="72001-187">Transport providers set MSGFLAG_FROMME for an incoming message that was sent by the currently logged on user.</span></span> <span data-ttu-id="72001-188">クライアントは、この値を使用して、送信者名よりも送信アイテム フォルダーのコンテンツ テーブルに受信者名を表示する方が適切かどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="72001-188">A client can use this value to determine that it is more appropriate to show recipient names in the contents table of the Sent Items folder than sender names.</span></span> <span data-ttu-id="72001-189">構成プロセス中に保存され、まだ送信されていないメッセージは、送信者名ではなく受信者名と一緒に表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72001-189">Messages that have been saved during the composition process and not yet sent should also be displayed with recipient names rather than sender names.</span></span> 
  
<span data-ttu-id="72001-190">受信メッセージの場合、メッセージ ストア プロバイダーは、MSGFLAG_READフラグをクリアして、読み取り状態をリセットします。</span><span class="sxs-lookup"><span data-stu-id="72001-190">For an incoming message, a message store provider clears the MSGFLAG_READ flag to reset its read status.</span></span> <span data-ttu-id="72001-191">クライアントは、メッセージの [IMessage::SetReadFlag](imessage-setreadflag.md) メソッドまたはフォルダーの [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) メソッドを呼び出すことによって、読み取り状態を変更し、読み取りレポートと非読み取りレポートの送信を制御する必要がある場合に、MSGFLAG_READ フラグを設定またはクリアできます。</span><span class="sxs-lookup"><span data-stu-id="72001-191">A client can set or clear the MSGFLAG_READ flag when it is necessary to change the read status and control the sending of read and nonread reports, by calling either the message's [IMessage::SetReadFlag](imessage-setreadflag.md) method or its folder's [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) method.</span></span> <span data-ttu-id="72001-192">これらのメソッドの主な違いは、それらを実装するオブジェクト以外は、フォルダー メソッドがフォルダー内の 1 つ、複数、またはすべてのメッセージに影響を与える可能性がある点です。</span><span class="sxs-lookup"><span data-stu-id="72001-192">The main difference between these methods, other than the object implementing them, is that the folder method can affect one, several, or all of the messages in the folder.</span></span> <span data-ttu-id="72001-193">message メソッドは、1 つのメッセージに影響します。</span><span class="sxs-lookup"><span data-stu-id="72001-193">The message method affects a single message.</span></span> 
  
<span data-ttu-id="72001-194">クライアントは、受信メッセージをテストして、MSGFLAG_ORIGIN_X400、MSGFLAG_ORIGIN_INTERNET、MSGFLAG_ORIGIN_MISC_EXTする必要があります。</span><span class="sxs-lookup"><span data-stu-id="72001-194">A client should also test an incoming message for the MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET, and MSGFLAG_ORIGIN_MISC_EXT flags.</span></span> <span data-ttu-id="72001-195">これらのフラグは、受信トランスポート プロバイダーによって設定され、ゲートウェイが信頼できると見なできないソースからメッセージが到着したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="72001-195">These flags are set by the inbound transport provider and indicate that the message arrived from a source that the gateway cannot consider trusted.</span></span> <span data-ttu-id="72001-196">つまり、メッセージは組織外または内部的に発信されますが、ゲートウェイに対して既知ではないワークステーションから発信されます。</span><span class="sxs-lookup"><span data-stu-id="72001-196">This means the message originated either outside the organization, or internally but from a workstation not known to the gateway.</span></span> <span data-ttu-id="72001-197">いずれにしても、送信者の身元が確認されない可能性があります。また、コンピューター ウイルスを組織に導入するリスクがあります。</span><span class="sxs-lookup"><span data-stu-id="72001-197">In any case, the identity of the sender may not be confirmed, and there is a risk of introducing a computer virus into the organization.</span></span> <span data-ttu-id="72001-198">クライアントはユーザーに警告メッセージを表示し、メッセージを開かなくても削除するオプションを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72001-198">The client should display a warning message to the user and offer an option of deleting the message without opening it.</span></span> 
  
<span data-ttu-id="72001-199">メッセージ ストア プロバイダーは、受信メッセージMSGFLAG_UNMODIFIEDフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="72001-199">Message store providers set the MSGFLAG_UNMODIFIED flag for incoming messages.</span></span> <span data-ttu-id="72001-200">MSGFLAG_UNMODIFIEDは、配信後にメッセージが変更されていないかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="72001-200">MSGFLAG_UNMODIFIED indicates that a message has not been changed since delivery.</span></span> <span data-ttu-id="72001-201">クライアントは、メッセージ ストア プロバイダーによって設定された後、この値をクリアできません。</span><span class="sxs-lookup"><span data-stu-id="72001-201">A client cannot clear this value after it has been set by a message store provider.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="72001-202">関連リソース</span><span class="sxs-lookup"><span data-stu-id="72001-202">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72001-203">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="72001-203">Protocol specifications</span></span>

<span data-ttu-id="72001-204">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72001-204">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72001-205">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="72001-205">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="72001-206">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72001-206">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72001-207">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="72001-207">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72001-208">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="72001-208">Header files</span></span>

<span data-ttu-id="72001-209">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72001-209">Mapidefs.h</span></span>
  
> <span data-ttu-id="72001-210">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="72001-210">Provides data type definitions.</span></span>
    
<span data-ttu-id="72001-211">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="72001-211">Mapitags.h</span></span>
  
> <span data-ttu-id="72001-212">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="72001-212">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72001-213">関連項目</span><span class="sxs-lookup"><span data-stu-id="72001-213">See also</span></span>



[<span data-ttu-id="72001-214">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="72001-214">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)


[<span data-ttu-id="72001-215">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="72001-215">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72001-216">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="72001-216">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72001-217">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="72001-217">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72001-218">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="72001-218">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

