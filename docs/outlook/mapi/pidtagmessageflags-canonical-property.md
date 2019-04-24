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
ms.openlocfilehash: 5b660b592e77279a4d60f3a036724341352c9b6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325744"
---
# <a name="pidtagmessageflags-canonical-property"></a><span data-ttu-id="1de26-103">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1de26-103">PidTagMessageFlags Canonical Property</span></span>

  
  
<span data-ttu-id="1de26-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1de26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1de26-105">メッセージの送信元と現在の状態を示すフラグのビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="1de26-105">Contains a bitmask of flags that indicate the origin and current state of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1de26-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1de26-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1de26-107">PR_MESSAGE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="1de26-107">PR_MESSAGE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="1de26-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1de26-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1de26-109">0x0E07</span><span class="sxs-lookup"><span data-stu-id="1de26-109">0x0E07</span></span>  <br/> |
|<span data-ttu-id="1de26-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1de26-110">Data type:</span></span>  <br/> |<span data-ttu-id="1de26-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1de26-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1de26-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1de26-112">Area:</span></span>  <br/> |<span data-ttu-id="1de26-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="1de26-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1de26-114">解説</span><span class="sxs-lookup"><span data-stu-id="1de26-114">Remarks</span></span>

<span data-ttu-id="1de26-115">このプロパティは、送信側と受信側の両方で公開されている、クライアントアプリケーションまたはストアプロバイダーによって異なる値を持つ、送信側と受信側のメッセージプロパティです。</span><span class="sxs-lookup"><span data-stu-id="1de26-115">This property is a nontransmittable message property exposed at both the sending and receiving ends of a transmission, with different values depending upon the client application or store provider involved.</span></span> <span data-ttu-id="1de26-116">このプロパティは、メッセージが最初に作成されて保存されてから、メッセージストアプロバイダー、トランスポートプロバイダー、およびメッセージが処理されるときに MAPI スプーラーによって定期的に更新されるときに、クライアントまたはメッセージストアプロバイダーによって初期化されます。メッセージの処理とその状態変更.</span><span class="sxs-lookup"><span data-stu-id="1de26-116">This property is initialized by the client or message store provider when a message is created and saved for the first time and then updated periodically by the message store provider, a transport provider, and the MAPI spooler as the message is processed and its state changes.</span></span> 
  
<span data-ttu-id="1de26-117">このプロパティは、送信前と送信後のメッセージ、および受信したメッセージのすべてのコピーに存在します。</span><span class="sxs-lookup"><span data-stu-id="1de26-117">This property exists on a message both before and after submission, and on all copies of the received message.</span></span> <span data-ttu-id="1de26-118">受信者のプロパティではありませんが、受信者によって開封または変更されたかどうかに応じて、各受信者に公開されます。</span><span class="sxs-lookup"><span data-stu-id="1de26-118">Although it is not a recipient property, it is exposed differently to each recipient according to whether it has been read or modified by that recipient.</span></span> 
  
<span data-ttu-id="1de26-119">このプロパティには、次の1つ以上のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1de26-119">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="1de26-120">MSGFLAG_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="1de26-120">MSGFLAG_ASSOCIATED</span></span> 
  
> <span data-ttu-id="1de26-121">メッセージはフォルダーの関連付けられたメッセージです。</span><span class="sxs-lookup"><span data-stu-id="1de26-121">The message is an associated message of a folder.</span></span> <span data-ttu-id="1de26-122">クライアントまたはプロバイダーは、このフラグに対して読み取り専用アクセス権を持っています。</span><span class="sxs-lookup"><span data-stu-id="1de26-122">The client or provider has read-only access to this flag.</span></span> <span data-ttu-id="1de26-123">関連付けられたメッセージの場合、MSGFLAG_READ フラグは無視されます。読み取り/未開封の状態は保持されません。</span><span class="sxs-lookup"><span data-stu-id="1de26-123">The MSGFLAG_READ flag is ignored for associated messages, which do not retain a read/unread state.</span></span> 
    
<span data-ttu-id="1de26-124">MSGFLAG_FROMME</span><span class="sxs-lookup"><span data-stu-id="1de26-124">MSGFLAG_FROMME</span></span> 
  
> <span data-ttu-id="1de26-125">メッセージを送信したメッセージングユーザーがメッセージを受信しました。</span><span class="sxs-lookup"><span data-stu-id="1de26-125">The messaging user sending was the messaging user receiving the message.</span></span> <span data-ttu-id="1de26-126">クライアントまたはプロバイダーは、このフラグへの読み取り/書き込みアクセス権を持ちます。その後、最初の[imapiprop:: SaveChanges](imapiprop-savechanges.md)呼び出しに対しては読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="1de26-126">The client or provider has read/write access to this flag until the first [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call and read-only thereafter.</span></span> <span data-ttu-id="1de26-127">このフラグは、トランスポートプロバイダーによって設定されることを目的としています。</span><span class="sxs-lookup"><span data-stu-id="1de26-127">This flag is meant to be set by the transport provider.</span></span> 
    
<span data-ttu-id="1de26-128">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="1de26-128">MSGFLAG_HASATTACH</span></span> 
  
> <span data-ttu-id="1de26-129">メッセージに添付ファイルが1つ以上ある。</span><span class="sxs-lookup"><span data-stu-id="1de26-129">The message has at least one attachment.</span></span> <span data-ttu-id="1de26-130">このフラグは、メッセージの**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="1de26-130">This flag corresponds to the message's **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) property.</span></span> <span data-ttu-id="1de26-131">クライアントは、このフラグへの読み取り専用アクセス権を持っています。</span><span class="sxs-lookup"><span data-stu-id="1de26-131">The client has read-only access to this flag.</span></span> 
    
<span data-ttu-id="1de26-132">MSGFLAG_NRN_PENDING</span><span class="sxs-lookup"><span data-stu-id="1de26-132">MSGFLAG_NRN_PENDING</span></span> 
  
> <span data-ttu-id="1de26-133">メッセージに対して未読レポートを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1de26-133">A nonread report needs to be sent for the message.</span></span> <span data-ttu-id="1de26-134">クライアントまたはプロバイダーは、このフラグに対して読み取り専用アクセス権を持っています。</span><span class="sxs-lookup"><span data-stu-id="1de26-134">The client or provider has read-only access to this flag.</span></span> 
    
<span data-ttu-id="1de26-135">MSGFLAG_ORIGIN_INTERNET</span><span class="sxs-lookup"><span data-stu-id="1de26-135">MSGFLAG_ORIGIN_INTERNET</span></span> 
  
> <span data-ttu-id="1de26-136">受信メッセージがインターネット経由で到着しました。</span><span class="sxs-lookup"><span data-stu-id="1de26-136">The incoming message arrived over the Internet.</span></span> <span data-ttu-id="1de26-137">これは、組織外またはソースからのものであり、ゲートウェイは信頼を考慮できません。</span><span class="sxs-lookup"><span data-stu-id="1de26-137">It originated either outside the organization or from a source the gateway cannot consider trusted.</span></span> <span data-ttu-id="1de26-138">クライアントは、ユーザーに適切なメッセージを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1de26-138">The client should display an appropriate message to the user.</span></span> <span data-ttu-id="1de26-139">トランスポートプロバイダーはこのフラグを設定します。クライアントは読み取り専用のアクセス権を持っています。</span><span class="sxs-lookup"><span data-stu-id="1de26-139">Transport providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="1de26-140">MSGFLAG_ORIGIN_MISC_EXT</span><span class="sxs-lookup"><span data-stu-id="1de26-140">MSGFLAG_ORIGIN_MISC_EXT</span></span> 
  
> <span data-ttu-id="1de26-141">受信メッセージが、X またはインターネット以外の外部リンク経由で到着しました。</span><span class="sxs-lookup"><span data-stu-id="1de26-141">The incoming message arrived over an external link other than X.400 or the Internet.</span></span> <span data-ttu-id="1de26-142">これは、組織外またはソースからのものであり、ゲートウェイは信頼を考慮できません。</span><span class="sxs-lookup"><span data-stu-id="1de26-142">It originated either outside the organization or from a source the gateway cannot consider trusted.</span></span> <span data-ttu-id="1de26-143">クライアントは、ユーザーに適切なメッセージを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1de26-143">The client should display an appropriate message to the user.</span></span> <span data-ttu-id="1de26-144">トランスポートプロバイダーはこのフラグを設定します。クライアントは読み取り専用のアクセス権を持っています。</span><span class="sxs-lookup"><span data-stu-id="1de26-144">Transport providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="1de26-145">MSGFLAG_ORIGIN_X400</span><span class="sxs-lookup"><span data-stu-id="1de26-145">MSGFLAG_ORIGIN_X400</span></span> 
  
> <span data-ttu-id="1de26-146">受信したメッセージが、X. 400 リンクを介して到着しました。</span><span class="sxs-lookup"><span data-stu-id="1de26-146">The incoming message arrived over an X.400 link.</span></span> <span data-ttu-id="1de26-147">これは、組織外またはソースからのものであり、ゲートウェイは信頼を考慮できません。</span><span class="sxs-lookup"><span data-stu-id="1de26-147">It originated either outside the organization or from a source the gateway cannot consider trusted.</span></span> <span data-ttu-id="1de26-148">クライアントは、ユーザーに適切なメッセージを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1de26-148">The client should display an appropriate message to the user.</span></span> <span data-ttu-id="1de26-149">トランスポートプロバイダーはこのフラグを設定します。クライアントは読み取り専用のアクセス権を持っています。</span><span class="sxs-lookup"><span data-stu-id="1de26-149">Transport providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="1de26-150">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="1de26-150">MSGFLAG_READ</span></span> 
  
> <span data-ttu-id="1de26-151">メッセージに開封済みのマークが付けられています。</span><span class="sxs-lookup"><span data-stu-id="1de26-151">The message is marked as having been read.</span></span> <span data-ttu-id="1de26-152">これは、いつでも[IMessage:: setreadflag](imessage-setreadflag.md)または[imapifolder:: setreadflag](imapifolder-setreadflags.md)への呼び出しの結果として発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="1de26-152">This can occur as the result of a call at any time to [IMessage::SetReadFlag](imessage-setreadflag.md) or [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span> <span data-ttu-id="1de26-153">また、クライアントは、メッセージが初めて保存される前に、メッセージの**imapiprop:: setprops**メソッドを呼び出して、このフラグを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="1de26-153">Clients can also set this flag by calling a message's **IMAPIProp::SetProps** method before the message has been saved for the first time.</span></span> <span data-ttu-id="1de26-154">**MSGFLAG_ASSOCIATED**フラグが設定されている場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1de26-154">This flag is ignored if the **MSGFLAG_ASSOCIATED** flag is set.</span></span> 
    
<span data-ttu-id="1de26-155">MSGFLAG_RESEND</span><span class="sxs-lookup"><span data-stu-id="1de26-155">MSGFLAG_RESEND</span></span> 
  
> <span data-ttu-id="1de26-156">メッセージには、配信不能レポートを伴う再送信操作の要求が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1de26-156">The message includes a request for a resend operation with a nondelivery report.</span></span> <span data-ttu-id="1de26-157">クライアントまたはプロバイダーは、このフラグへの読み取り/書き込みアクセス権を持ちます。その後、最初の[imapiprop:: SaveChanges](imapiprop-savechanges.md)呼び出しに対しては読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="1de26-157">The client or provider has read/write access to this flag until the first [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call and read-only thereafter.</span></span> 
    
<span data-ttu-id="1de26-158">MSGFLAG_RN_PENDING</span><span class="sxs-lookup"><span data-stu-id="1de26-158">MSGFLAG_RN_PENDING</span></span> 
  
> <span data-ttu-id="1de26-159">メッセージに対して閲覧レポートを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1de26-159">A read report needs to be sent for the message.</span></span> <span data-ttu-id="1de26-160">クライアントまたはプロバイダーは、このフラグに対して読み取り専用アクセス権を持っています。</span><span class="sxs-lookup"><span data-stu-id="1de26-160">The client or provider has read-only access to this flag.</span></span> 
    
<span data-ttu-id="1de26-161">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="1de26-161">MSGFLAG_SUBMIT</span></span> 
  
> <span data-ttu-id="1de26-162">このメッセージは、 [IMessage:: submitmessage](imessage-submitmessage.md)の呼び出しの結果として送信するようにマークされています。</span><span class="sxs-lookup"><span data-stu-id="1de26-162">The message is marked for sending as a result of a call to [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> <span data-ttu-id="1de26-163">メッセージストアプロバイダーはこのフラグを設定します。クライアントは読み取り専用のアクセス権を持っています。</span><span class="sxs-lookup"><span data-stu-id="1de26-163">Message store providers set this flag; the client has read-only access.</span></span> 
    
<span data-ttu-id="1de26-164">MSGFLAG_UNMODIFIED</span><span class="sxs-lookup"><span data-stu-id="1de26-164">MSGFLAG_UNMODIFIED</span></span> 
  
> <span data-ttu-id="1de26-165">送信メッセージは、最初に保存された時点以降変更されていません。受信メッセージは、配信されてから変更されていません。</span><span class="sxs-lookup"><span data-stu-id="1de26-165">The outgoing message has not been modified since the first time that it was saved; the incoming message has not been modified since it was delivered.</span></span> 
    
<span data-ttu-id="1de26-166">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="1de26-166">MSGFLAG_UNSENT</span></span> 
  
> <span data-ttu-id="1de26-167">メッセージがまだ構成されています。</span><span class="sxs-lookup"><span data-stu-id="1de26-167">The message is still being composed.</span></span> <span data-ttu-id="1de26-168">このファイルは保存されますが、送信されていません。</span><span class="sxs-lookup"><span data-stu-id="1de26-168">It is saved, but has not been sent.</span></span> <span data-ttu-id="1de26-169">クライアントまたはプロバイダーは、このフラグへの読み取り/書き込みアクセス権を持ちます。その後、最初の[imapiprop:: SaveChanges](imapiprop-savechanges.md)呼び出しに対しては読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="1de26-169">The client or provider has read/write access to this flag until the first [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call and read-only thereafter.</span></span> <span data-ttu-id="1de26-170">クライアントがメッセージの送信時にこのフラグを設定していない場合、メッセージストアプロバイダーは**IMessage:: submitmessage**が呼び出されたときにこのフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="1de26-170">If a client doesn't set this flag by the time the message is sent, the message store provider sets it when **IMessage::SubmitMessage** is called.</span></span> <span data-ttu-id="1de26-171">通常、このフラグはメッセージが送信された後にクリアされます。</span><span class="sxs-lookup"><span data-stu-id="1de26-171">Typically, this flag is cleared after the message is sent.</span></span> 
    
<span data-ttu-id="1de26-172">クライアントまたはメッセージストアプロバイダーは、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出してフラグ値を読み取ることによって、メッセージの現在の状態をいつでも確認できます。</span><span class="sxs-lookup"><span data-stu-id="1de26-172">A client or message store provider can check the current state of the message at any time by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method to read the flag values.</span></span> <span data-ttu-id="1de26-173">クライアントまたはプロバイダーは、 [imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、現在読み取り/書き込みアクセス権を持つフラグを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="1de26-173">The client or provider can also call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to change any flags that currently have read/write access.</span></span> 
  
<span data-ttu-id="1de26-174">フラグのいくつかは常に値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="1de26-174">Several of the flags are always read-only.</span></span> <span data-ttu-id="1de26-175">一部のプロパティは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを最初に呼び出したときまでは読み取り/書き込みが行われ、それ以降は**imapiprop:: setprops**に関しては読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="1de26-175">Some are read/write until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and thereafter become read-only as far as **IMAPIProp::SetProps** is concerned.</span></span> <span data-ttu-id="1de26-176">MSGFLAG_READ の1つは、後で[IMessage:: setreadflag](imessage-setreadflag.md)または[imapifolder:: setreadflag](imapifolder-setreadflags.md)を使用して変更できます。</span><span class="sxs-lookup"><span data-stu-id="1de26-176">One of these, MSGFLAG_READ, can be changed later through [IMessage::SetReadFlag](imessage-setreadflag.md) or [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span> 
  
<span data-ttu-id="1de26-177">通常、このプロパティの初期値は MSGFLAG_UNSENT と MSGFLAG_UNMODIFIED で、まだ送信または変更されていないメッセージを示します。</span><span class="sxs-lookup"><span data-stu-id="1de26-177">The initial values for this property are typically MSGFLAG_UNSENT and MSGFLAG_UNMODIFIED to indicate a message that has not yet been sent or changed.</span></span> <span data-ttu-id="1de26-178">メッセージが2回目に保存されると、メッセージストアプロバイダーは MSGFLAG_UNMODIFIED フラグをクリアします。</span><span class="sxs-lookup"><span data-stu-id="1de26-178">When a message is saved for the second time, the message store provider clears the MSGFLAG_UNMODIFIED flag.</span></span> <span data-ttu-id="1de26-179">メッセージを保存するときにメッセージストアプロバイダーが設定できるもう1つの値は、MSGFLAG_HASATTACH フラグで、メッセージに1つ以上の添付ファイルがあることを示します。</span><span class="sxs-lookup"><span data-stu-id="1de26-179">Another value that a message store provider can set when a message is saved is the MSGFLAG_HASATTACH flag, indicating that the message has one or more attachments.</span></span> <span data-ttu-id="1de26-180">**PR_HASATTACH**プロパティは、この設定値から計算されます。</span><span class="sxs-lookup"><span data-stu-id="1de26-180">The **PR_HASATTACH** property is computed from this setting.</span></span> 
  
<span data-ttu-id="1de26-181">クライアントが[IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出してメッセージを送信すると、メッセージストアプロバイダーは MAPI スプーラー用のコピーを作成し、MSGFLAG_SUBMIT フラグを設定してこのプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="1de26-181">When a client calls the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message, the message store provider makes a copy of it for the MAPI spooler and updates this property by setting the MSGFLAG_SUBMIT flag.</span></span> <span data-ttu-id="1de26-182">まだ設定されていない場合、メッセージストアプロバイダーは MSGFLAG_UNSENT も設定します。</span><span class="sxs-lookup"><span data-stu-id="1de26-182">The message store provider also sets MSGFLAG_UNSENT if it is not yet set.</span></span> <span data-ttu-id="1de26-183">MSGFLAG_SUBMIT は、 \*\*\*\* 送信処理を開始し、メッセージがクライアントに対して読み取り専用になっていることを示します。</span><span class="sxs-lookup"><span data-stu-id="1de26-183">MSGFLAG_SUBMIT indicates that **SubmitMessage** has been called, beginning the send process, and that the message is now read-only to the client.</span></span> <span data-ttu-id="1de26-184">MSGFLAG_UNSENT は、MAPI スプーラーがメッセージを処理していることを示します。</span><span class="sxs-lookup"><span data-stu-id="1de26-184">MSGFLAG_UNSENT indicates that the MAPI spooler is handling the message.</span></span> <span data-ttu-id="1de26-185">送信プロセスが取り消されると、メッセージストアプロバイダーはこのフラグをリセットします。</span><span class="sxs-lookup"><span data-stu-id="1de26-185">If the send process is canceled, the message store provider resets this flag.</span></span> 
  
<span data-ttu-id="1de26-186">メッセージが配信のためにトランスポートプロバイダーに渡されると、送信者がメッセージの受信時にメッセージングサーバーと同じアカウントを持っていた場合、トランスポートプロバイダーは MSGFLAG_FROMME フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="1de26-186">When the message is given to a transport provider for delivery, the transport provider sets the MSGFLAG_FROMME flag if the sender had the same account on the messaging server as the message was received on.</span></span> <span data-ttu-id="1de26-187">トランスポートプロバイダー現在ログオンしているユーザーによって送信された受信メッセージに対して MSGFLAG_FROMME を設定します。</span><span class="sxs-lookup"><span data-stu-id="1de26-187">Transport providers set MSGFLAG_FROMME for an incoming message that was sent by the currently logged on user.</span></span> <span data-ttu-id="1de26-188">クライアントは、この値を使用して、[送信済みアイテム] フォルダーのコンテンツテーブルに [送信者名] よりも、受信者名を表示することが適切であるかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="1de26-188">A client can use this value to determine that it is more appropriate to show recipient names in the contents table of the Sent Items folder than sender names.</span></span> <span data-ttu-id="1de26-189">構成処理中に保存されてまだ送信されていないメッセージも、送信者名ではなく受信者名で表示されます。</span><span class="sxs-lookup"><span data-stu-id="1de26-189">Messages that have been saved during the composition process and not yet sent should also be displayed with recipient names rather than sender names.</span></span> 
  
<span data-ttu-id="1de26-190">受信メッセージの場合、メッセージストアプロバイダーは、MSGFLAG_READ フラグをクリアしてその読み取り状態をリセットします。</span><span class="sxs-lookup"><span data-stu-id="1de26-190">For an incoming message, a message store provider clears the MSGFLAG_READ flag to reset its read status.</span></span> <span data-ttu-id="1de26-191">クライアントは、メッセージの[IMessage:: setreadflag](imessage-setreadflag.md)メソッドまたはそのフォルダーの imapifolder を呼び出して、読み取り状態を変更し、読み取りおよび非開封レポートの送信を制御する必要がある場合に、MSGFLAG_READ フラグを設定またはクリアできます[。setreadflags](imapifolder-setreadflags.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="1de26-191">A client can set or clear the MSGFLAG_READ flag when it is necessary to change the read status and control the sending of read and nonread reports, by calling either the message's [IMessage::SetReadFlag](imessage-setreadflag.md) method or its folder's [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) method.</span></span> <span data-ttu-id="1de26-192">これらのメソッドの主な違いは、フォルダーメソッドがフォルダー内の1つ、複数、またはすべてのメッセージに影響する可能性があることです。</span><span class="sxs-lookup"><span data-stu-id="1de26-192">The main difference between these methods, other than the object implementing them, is that the folder method can affect one, several, or all of the messages in the folder.</span></span> <span data-ttu-id="1de26-193">message メソッドは、1つのメッセージに影響します。</span><span class="sxs-lookup"><span data-stu-id="1de26-193">The message method affects a single message.</span></span> 
  
<span data-ttu-id="1de26-194">クライアントは、MSGFLAG_ORIGIN_X400、MSGFLAG_ORIGIN_INTERNET、および MSGFLAG_ORIGIN_MISC_EXT フラグの受信メッセージもテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1de26-194">A client should also test an incoming message for the MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET, and MSGFLAG_ORIGIN_MISC_EXT flags.</span></span> <span data-ttu-id="1de26-195">これらのフラグは、受信トランスポートプロバイダーによって設定され、ゲートウェイが信頼を考慮できない送信元から届いたメッセージを示します。</span><span class="sxs-lookup"><span data-stu-id="1de26-195">These flags are set by the inbound transport provider and indicate that the message arrived from a source that the gateway cannot consider trusted.</span></span> <span data-ttu-id="1de26-196">これは、メッセージが組織外にあるか、内部ではゲートウェイで認識されないワークステーションから発信されたことを意味します。</span><span class="sxs-lookup"><span data-stu-id="1de26-196">This means the message originated either outside the organization, or internally but from a workstation not known to the gateway.</span></span> <span data-ttu-id="1de26-197">いずれの場合も、送信者の id は確認されず、コンピューターウイルスが組織に導入される危険性があります。</span><span class="sxs-lookup"><span data-stu-id="1de26-197">In any case, the identity of the sender may not be confirmed, and there is a risk of introducing a computer virus into the organization.</span></span> <span data-ttu-id="1de26-198">クライアントは警告メッセージをユーザーに表示し、それを開かずにメッセージを削除するオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="1de26-198">The client should display a warning message to the user and offer an option of deleting the message without opening it.</span></span> 
  
<span data-ttu-id="1de26-199">メッセージストアプロバイダーは、受信メッセージの MSGFLAG_UNMODIFIED フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="1de26-199">Message store providers set the MSGFLAG_UNMODIFIED flag for incoming messages.</span></span> <span data-ttu-id="1de26-200">MSGFLAG_UNMODIFIED は、メッセージが配信後に変更されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="1de26-200">MSGFLAG_UNMODIFIED indicates that a message has not been changed since delivery.</span></span> <span data-ttu-id="1de26-201">クライアントは、メッセージストアプロバイダーによって設定された後に、この値をクリアすることはできません。</span><span class="sxs-lookup"><span data-stu-id="1de26-201">A client cannot clear this value after it has been set by a message store provider.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1de26-202">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1de26-202">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1de26-203">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1de26-203">Protocol specifications</span></span>

<span data-ttu-id="1de26-204">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1de26-204">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1de26-205">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1de26-205">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1de26-206">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1de26-206">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1de26-207">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="1de26-207">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1de26-208">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1de26-208">Header files</span></span>

<span data-ttu-id="1de26-209">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1de26-209">Mapidefs.h</span></span>
  
> <span data-ttu-id="1de26-210">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1de26-210">Provides data type definitions.</span></span>
    
<span data-ttu-id="1de26-211">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1de26-211">Mapitags.h</span></span>
  
> <span data-ttu-id="1de26-212">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1de26-212">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1de26-213">関連項目</span><span class="sxs-lookup"><span data-stu-id="1de26-213">See also</span></span>



[<span data-ttu-id="1de26-214">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="1de26-214">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)


[<span data-ttu-id="1de26-215">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1de26-215">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1de26-216">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1de26-216">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1de26-217">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1de26-217">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1de26-218">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1de26-218">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

