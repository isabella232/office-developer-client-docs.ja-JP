---
title: 情報更新および完全な更新としての会議出席依頼について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: 会議出席依頼は、メッセージ クラスとして IPM.Schedule.Meeting.Request が設定された電子メールです。 既定では、会議出席依頼を受信する出席者が、依頼に直接応答します。
ms.openlocfilehash: 8e7ab7a85d3f9f7c0a67245b8d8ad27442f5c5e4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316997"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a><span data-ttu-id="f6006-104">情報更新または完全更新としての会議出席依頼について</span><span class="sxs-lookup"><span data-stu-id="f6006-104">About meeting requests as informational updates and full updates</span></span>

<span data-ttu-id="f6006-105">会議出席依頼は、メッセージ クラスとして **IPM.Schedule.Meeting.Request** が設定された電子メールです。</span><span class="sxs-lookup"><span data-stu-id="f6006-105">A meeting request is an email that has **IPM.Schedule.Meeting.Request** as the message class.</span></span> <span data-ttu-id="f6006-106">既定では、会議出席依頼を受信した参加者は、その依頼に直接応答します。</span><span class="sxs-lookup"><span data-stu-id="f6006-106">By default, an attendee receiving a meeting request responds to it directly.</span></span> <span data-ttu-id="f6006-107">Outlook では、プリンシパル受信者の代わりに会議出席依頼に応答できる代理人を設定できます。</span><span class="sxs-lookup"><span data-stu-id="f6006-107">Outlook supports setting up delegates who can respond to meeting requests on behalf of the principal recipient.</span></span> <span data-ttu-id="f6006-108">Outlook は、現在の更新状態を識別するために、会議出席依頼の名前付きプロパティ [PidLidMeetingType](https://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) をプログラムによって設定します。</span><span class="sxs-lookup"><span data-stu-id="f6006-108">Programmatically, Outlook sets the named property [PidLidMeetingType](https://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) of a meeting request to identify the current update status.</span></span> 
  
## <a name="recipients-without-delegates"></a><span data-ttu-id="f6006-109">代理人のいない受信者</span><span class="sxs-lookup"><span data-stu-id="f6006-109">Recipients without delegates</span></span>

<span data-ttu-id="f6006-p103">Outlook が新たな会議出席依頼を受信すると、その会議出席依頼項目の **PidLidMeetingType** プロパティを **mtgRequest** に設定します。この会議のその後の更新は、更新の原因と、Outlook に設定されている **PidLidMeetingType** に応じて、 **mtgFullUpdate** (完全な更新) または **mtgInfoUpdate** (情報更新) になります。完全な更新の場合、出席者は会議出席依頼に明示的に応答する必要があり、情報更新の場合にはその必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f6006-p103">When Outlook receives a new meeting request, Outlook sets the **PidLidMeetingType** property of the meeting request item to **mtgRequest**. Any subsequent update of that meeting is either **mtgFullUpdate** (a full update) or **mtgInfoUpdate** (an informational update) depending on the cause of the update, with Outlook setting **PidLidMeetingType** accordingly. A full update requires an attendee to explicitly respond to the meeting request, and an informational update does not.</span></span> 
  
## <a name="full-updates"></a><span data-ttu-id="f6006-113">完全更新</span><span class="sxs-lookup"><span data-stu-id="f6006-113">Full updates</span></span>

<span data-ttu-id="f6006-114">完全更新の結果になるシナリオは、2 つあります。</span><span class="sxs-lookup"><span data-stu-id="f6006-114">There are two scenarios that result in a full update:</span></span>
  
- <span data-ttu-id="f6006-p104">開催者が以前の会議出席依頼の日付、時刻、時間帯、パターンを変更する場合、開催者はすべての出席者に更新を送信しなければなりません。この更新は完全な更新で、出席者は明示的に応答し、出席の可否を開催者に通知する必要があります。Outlook は以前の応答をすべて無視するからです。</span><span class="sxs-lookup"><span data-stu-id="f6006-p104">When an organizer changes the date, time, time zones, or recurrence of a prior meeting request, the organizer must send an update to all the attendees. This update is a full update to which an attendee must explicitly respond to notify the organizer of attendance, because Outlook ignores any previous responses.</span></span>
    
- <span data-ttu-id="f6006-117">出席者が最初の会議出席依頼に応答せず、その後に更新を受け取る場合、最初の会議出席依頼は期限切れになり、更新の原因に関係なくその更新は完全な更新となります。</span><span class="sxs-lookup"><span data-stu-id="f6006-117">If an attendee has not responded to an initial meeting request and receives a subsequent update, the initial meeting request becomes out-of-date and the update is a full update, regardless of the cause of the update.</span></span>
    
## <a name="informational-updates"></a><span data-ttu-id="f6006-118">情報更新</span><span class="sxs-lookup"><span data-stu-id="f6006-118">Informational updates</span></span>

<span data-ttu-id="f6006-p105">Outlook が情報更新を生成するシナリオは 4 つあります。これらのシナリオでは、情報更新への応答はオプションとなります。</span><span class="sxs-lookup"><span data-stu-id="f6006-p105">There are four scenarios in which Outlook generates an informational update. In these scenarios, responding to the informational update is optional.</span></span>
  
- <span data-ttu-id="f6006-p106">開催者が以前の会議出席依頼の場所を変更する場合、開催者はすべての出席者に更新を送信しなければなりません。出席者が既に最初の会議出席依頼を承諾している場合、出席者は更新を情報更新として受け取ります。</span><span class="sxs-lookup"><span data-stu-id="f6006-p106">If an organizer changes the location of a prior meeting request, the organizer must send an update to all the attendees. If an attendee already accepted the initial meeting request, the attendee receives the update as an informational update.</span></span>
    
- <span data-ttu-id="f6006-p107">開催者が以前の会議出席依頼に出席者を追加する場合、開催者は新しく追加した出席者に会議出席依頼を送信する必要があります。その場合、その更新に既存の出席者を含めることもできます。新しく追加された出席者は会議出席依頼を新しい依頼として受信します。開催者が既存の出席者にも更新を送信することを選択する場合、出席者は更新を情報更新として受け取ります。</span><span class="sxs-lookup"><span data-stu-id="f6006-p107">If an organizer adds an attendee to a prior meeting request, the organizer must send the meeting request to the newly added attendee, and has the option to include existing attendees on the update. The newly added attendee receives the meeting request as a new request. If the organizer chooses to send an update to existing attendees, the attendees receive the update as an informational update.</span></span>
    
- <span data-ttu-id="f6006-p108">開催者が以前の会議出席依頼から出席者をI削除する場合、開催者は会議出席依頼から削除した出席者に更新を送信する必要があります。その場合、その更新に既存の出席者を含めることもできます。出席者は更新を情報更新として受け取ります。</span><span class="sxs-lookup"><span data-stu-id="f6006-p108">If an organizer removes an attendee from a prior meeting request, the organizer must send an update to the attendee who was removed from the meeting request and has an option to include existing attendees on the update. Attendees receive the update as an informational update.</span></span>
    
- <span data-ttu-id="f6006-p109">開催者が以前の会議出席依頼の件名または本文を変更する場合、開催者は出席者に更新を送信することもできますし、その変更内容を開催者自身の会議出席依頼のコピーに保存のみ行うこともできます。開催者が更新を送信することにする場合、出席者は更新を情報更新として受け取ります。</span><span class="sxs-lookup"><span data-stu-id="f6006-p109">If an organizer changes the subject or body of a prior meeting request, the organizer has the option to send an update to the attendees or just save the changes to the organizer's own copy of the meeting request. If the organizer chooses to send an update, attendees receive the update as an informational update.</span></span>
    
## <a name="recipients-set-up-with-delegates"></a><span data-ttu-id="f6006-130">代理人が設定された受信者</span><span class="sxs-lookup"><span data-stu-id="f6006-130">Recipients set up with delegates</span></span>

<span data-ttu-id="f6006-p110">代理人を設定するよう選択した受信者は、[非公開] というマークが付いていない会議出席依頼に対して代理人に応答させることができます。既定では、プリンシパルが受信するのは会議出席依頼のコピーまたは以前の会議出席依頼に対する更新のコピーのみで、代理人は必ずオリジナルの会議出席依頼、またはオリジナルの完全な更新/情報更新を受け取ります。この既定の構成の場合、プリンシパルは委任した会議出席依頼と更新を必ず受信し、プリンシパルの代理人は「代理人のいない受信者」のセクションで代理人が設定されていない受信者に関する説明のとおりに、要求を新しい会議出席依頼、完全な更新、または情報更新として受け取ります。</span><span class="sxs-lookup"><span data-stu-id="f6006-p110">Recipients who choose to set up delegates can have delegates respond to meeting requests that are not marked Private. By default, the principal receives only a copy of a meeting request or a copy of an update to a prior meeting request, and the delegates always receive the original meeting request or original full or informational update. In this default configuration, the principal always receives delegated meeting requests and updates; delegates of the principal receive meeting requests as new meeting requests, full updates, or informational updates, as described for recipients without delegates in the section "Recipients Without Delegates."</span></span>
  
<span data-ttu-id="f6006-p111">代理人がプリンシパルの代わりに応答するように設定されていても、既定では、プリンシパルは非公開ではない会議出席依頼と更新に応答するように選択できます。ただし、管理者は、プリンシパル受信者が応答できないように設定することも可能です。</span><span class="sxs-lookup"><span data-stu-id="f6006-p111">By default, principals can choose to respond to non-private meeting requests and updates, even though delegates are set up to do that on their behalf. However, as an alternative, administrators can set up a policy to prevent principal recipients from responding.</span></span>
  

