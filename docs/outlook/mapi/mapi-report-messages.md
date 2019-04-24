---
title: MAPI レポートメッセージ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 824eb670-16b7-49bf-9992-39fe0586a552
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aab5c76fb268729f1a50a33e4764905fe3d53405
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329744"
---
# <a name="mapi-report-messages"></a><span data-ttu-id="2c275-103">MAPI レポートメッセージ</span><span class="sxs-lookup"><span data-stu-id="2c275-103">MAPI Report Messages</span></span>

  
  
<span data-ttu-id="2c275-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c275-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c275-105">レポートメッセージには、メッセージに関する状態情報が送信者に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c275-105">Report messages present status information about a message to its sender.</span></span>
  
<span data-ttu-id="2c275-106">次の2種類の一般的なレポートメッセージがあります。</span><span class="sxs-lookup"><span data-stu-id="2c275-106">There are two general types of report messages:</span></span>
  
- <span data-ttu-id="2c275-107">進捗レポートを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="2c275-107">Read status reports.</span></span>
    
- <span data-ttu-id="2c275-108">配信状態レポート</span><span class="sxs-lookup"><span data-stu-id="2c275-108">Delivery status reports.</span></span>
    
## <a name="read-status-reports"></a><span data-ttu-id="2c275-109">進捗レポートの読み取り</span><span class="sxs-lookup"><span data-stu-id="2c275-109">Read Status Reports</span></span>

<span data-ttu-id="2c275-110">読み取り状態レポートは、 [imapisupport:: readreceipt](imapisupport-readreceipt.md)メソッドへの呼び出しによって、メッセージストアプロバイダーによって開始され、 **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) のエントリ id で表される受信者に送信されます。プロパティ.</span><span class="sxs-lookup"><span data-stu-id="2c275-110">Read status reports are initiated by message store providers through a call to the [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method and are sent to the recipient represented by the entry identifier in the **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="2c275-111">読み取り状態レポートは自動的に生成されません。それらを受信するクライアントアプリケーションは、明示的に要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c275-111">Read status reports are not generated automatically; client applications that want to receive them must explicitly request them.</span></span>
  
<span data-ttu-id="2c275-112">読み取りレポートは、メッセージの読み取りフラグが設定されていることを示します。これは、メッセージを開く、印刷、移動、またはコピーするときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2c275-112">A read report indicates that the read flag of a message has been set, which can occur when the message is opened, printed, moved, or copied.</span></span> <span data-ttu-id="2c275-113">メッセージストアプロバイダーが移動またはコピー操作に対する応答で読み取りレポートを生成するかどうかは、メッセージの送信先によって異なります。</span><span class="sxs-lookup"><span data-stu-id="2c275-113">Whether or not a message store provider generates a read report in response to a move or copy operation depends on where the message is going.</span></span> <span data-ttu-id="2c275-114">別のメッセージストアに移動またはコピーされている場合、読み取りレポートは常に送信される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2c275-114">If it is being moved or copied to another message store, a read report will most likely always be sent.</span></span> <span data-ttu-id="2c275-115">現在のメッセージストアで移動またはコピーされている場合は、読み取りレポートが送信される場合もあります。</span><span class="sxs-lookup"><span data-stu-id="2c275-115">If it is being moved or copied in the current message store, a read report might or might not be sent.</span></span> 
  
<span data-ttu-id="2c275-116">非開封レポートは、メッセージの読み取りフラグが設定されていないこと、およびメッセージが [削除済みアイテム] フォルダーに配置される前、または期限切れになる前に開かれていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="2c275-116">A nonread report indicates that the read flag of a message is not set and that the message was not opened either before being placed in the Deleted Items folder or before the expiration of a time limit.</span></span> <span data-ttu-id="2c275-117">クライアントは、 [IMessage:: setreadflag](imessage-setreadflag.md)または[imapifolder:: setreadflag](imapifolder-setreadflags.md)メソッドを呼び出して、メッセージの読み取りフラグを設定またはクリアすることができます。</span><span class="sxs-lookup"><span data-stu-id="2c275-117">Clients can call the [IMessage::SetReadFlag](imessage-setreadflag.md) or [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) method to set or clear a message's read flag.</span></span> 
  
## <a name="delivery-status-reports"></a><span data-ttu-id="2c275-118">配信状態レポート</span><span class="sxs-lookup"><span data-stu-id="2c275-118">Delivery Status Reports</span></span>

<span data-ttu-id="2c275-119">配信状態は、メッセージが目的の受信者に達したときに送信される配信レポート、およびメッセージが受信者に到達できなかった場合に送信される配信不能レポートに反映されます。</span><span class="sxs-lookup"><span data-stu-id="2c275-119">Delivery status is reflected in a delivery report, which is sent when a message has reached its intended recipient, and in a nondelivery report, which is sent when a message could not reach a recipient.</span></span> <span data-ttu-id="2c275-120">配信状態レポートは、 **PR_REPORT_ENTRYID**プロパティのエントリ識別子で表される受信者、またはこのプロパティが存在しない場合は送信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="2c275-120">Delivery status reports are sent to the recipient represented by the entry identifier in the **PR_REPORT_ENTRYID** property or to the sender if this property is not present.</span></span> 
  
<span data-ttu-id="2c275-121">配信レポートは、要求のみで送信され、元のメッセージは含まれません。</span><span class="sxs-lookup"><span data-stu-id="2c275-121">Delivery reports are sent by request only and do not include the original message.</span></span> <span data-ttu-id="2c275-122">配信不能レポートは、非表示にする要求が行われない限り、自動的に送信されます。</span><span class="sxs-lookup"><span data-stu-id="2c275-122">Nondelivery reports are sent automatically unless a request is made to suppress them.</span></span> <span data-ttu-id="2c275-123">配信不能レポートには、配信が問題なくなった場合に、レポートの受信者がメッセージを再送信できるように、元のメッセージが添付ファイルとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="2c275-123">Nondelivery reports include the original message as an attachment to enable the report's recipient to resend the message in case whatever blocked the delivery is no longer a problem.</span></span> <span data-ttu-id="2c275-124">添付されたメッセージは、最初に送信するために[IMessage:: submitmessage](imessage-submitmessage.md)メソッドが呼び出されたときの元の状態と似ています。</span><span class="sxs-lookup"><span data-stu-id="2c275-124">The attached message resembles the original as it existed when the [IMessage::SubmitMessage](imessage-submitmessage.md) method was called to send it initially.</span></span> 
  
<span data-ttu-id="2c275-125">1つまたは複数の配信状態レポートは、 [imapisupport:: StatusRecips](imapisupport-statusrecips.md)メソッドを呼び出すと、トランスポートプロバイダーによって生成されます。</span><span class="sxs-lookup"><span data-stu-id="2c275-125">One or more delivery status reports are generated by transport providers when they call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> <span data-ttu-id="2c275-126">トランスポートプロバイダーは、メッセージの受信者のリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="2c275-126">Transport providers compose a list of recipients for a message.</span></span> <span data-ttu-id="2c275-127">受信者がレポートを受信するかどうか、生成されるレポートの種類は、以下によって決まります。</span><span class="sxs-lookup"><span data-stu-id="2c275-127">Whether or not a recipient receives a report and the type of report that is generated depends on the following:</span></span> 
  
- <span data-ttu-id="2c275-128">配信レポートメッセージがメッセージストアに置かれる前に、 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) プロパティが TRUE に設定されている受信者に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c275-128">Delivery reports go to recipients that set the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property to TRUE before the message was placed in the message store.</span></span>
    
- <span data-ttu-id="2c275-129">配信不能レポートは、 **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) プロパティが FALSE に設定されていない受信者に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c275-129">Nondelivery reports go to recipients that did not set the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property to FALSE.</span></span> 
    
<span data-ttu-id="2c275-130">配信不能レポートを表示するために必要な情報のほとんどは、添付されたメッセージの recipient テーブルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="2c275-130">Almost all of the information necessary to display a nondelivery report is contained in the recipient table of the attached message.</span></span> <span data-ttu-id="2c275-131">レポート自体のプロパティはいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="2c275-131">A few properties are from the report itself.</span></span> <span data-ttu-id="2c275-132">配信レポートの場合、必要な情報はレポートの recipient テーブルと、いくつかのレポートプロパティに含まれています。</span><span class="sxs-lookup"><span data-stu-id="2c275-132">For delivery reports, the necessary information is contained in the recipient table of the report and in a few report properties.</span></span> 
  
<span data-ttu-id="2c275-133">レポートは、送信されたメッセージのクラスに基づいて、個別のメッセージクラスを持つメッセージです。</span><span class="sxs-lookup"><span data-stu-id="2c275-133">Reports are messages with distinct message classes, based on the class of the sent message.</span></span> <span data-ttu-id="2c275-134">ほとんどのサービスプロバイダーは、メッセージクラスがピリオドで区切られた複数の部分で構成される名前付け規則を使用します。</span><span class="sxs-lookup"><span data-stu-id="2c275-134">Most service providers use a naming convention whereby the message class is composed of several parts separated by periods.</span></span> <span data-ttu-id="2c275-135">最初の部分は "report" で、最後の部分はレポートの種類を表す定数です。</span><span class="sxs-lookup"><span data-stu-id="2c275-135">The first part is "Report" and the last part is a constant that represents the report type.</span></span> <span data-ttu-id="2c275-136">中央の部分は、送信されたメッセージのクラスに対して予約されています。</span><span class="sxs-lookup"><span data-stu-id="2c275-136">The middle part is reserved for the class of the sent message.</span></span> <span data-ttu-id="2c275-137">たとえば、配信レポートは、IPM に関する配信レポートのメッセージクラスである定数 DR を使用しているためです。注意メッセージは、「**報告**されることを示しています。</span><span class="sxs-lookup"><span data-stu-id="2c275-137">For example, because a delivery report uses the constant DR, the message class for a delivery report about an IPM.Note message would be **Report.IPM.Note.DR**.</span></span>
  
<span data-ttu-id="2c275-138">次の表に、レポートの種類を表す定数を示します。</span><span class="sxs-lookup"><span data-stu-id="2c275-138">The following table shows the constants that represent the types of reports.</span></span>
  
|<span data-ttu-id="2c275-139">**レポートの種類**</span><span class="sxs-lookup"><span data-stu-id="2c275-139">**Report type**</span></span>|<span data-ttu-id="2c275-140">**メッセージクラスで使用される定数**</span><span class="sxs-lookup"><span data-stu-id="2c275-140">**Constant used in message class**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2c275-141">読み取り</span><span class="sxs-lookup"><span data-stu-id="2c275-141">Read</span></span>  <br/> |<span data-ttu-id="2c275-142">IPNRN</span><span class="sxs-lookup"><span data-stu-id="2c275-142">IPNRN</span></span>  <br/> |
|<span data-ttu-id="2c275-143">未開封</span><span class="sxs-lookup"><span data-stu-id="2c275-143">Nonread</span></span>  <br/> |<span data-ttu-id="2c275-144">ipnnrn</span><span class="sxs-lookup"><span data-stu-id="2c275-144">IPNNRN</span></span>  <br/> |
|<span data-ttu-id="2c275-145">Delivery</span><span class="sxs-lookup"><span data-stu-id="2c275-145">Delivery</span></span>  <br/> |<span data-ttu-id="2c275-146">DR</span><span class="sxs-lookup"><span data-stu-id="2c275-146">DR</span></span>  <br/> |
|<span data-ttu-id="2c275-147">配信不能</span><span class="sxs-lookup"><span data-stu-id="2c275-147">Nondelivery</span></span>  <br/> |<span data-ttu-id="2c275-148">NDR</span><span class="sxs-lookup"><span data-stu-id="2c275-148">NDR</span></span>  <br/> |
   
<span data-ttu-id="2c275-149">対話クライアントは、MAPI で提供される標準のフォームまたはレポートのメッセージクラスに対してフォームマネージャーに登録されているユーザー設定フォームを使用して、レポートメッセージを表示できます。</span><span class="sxs-lookup"><span data-stu-id="2c275-149">Interactive clients can display report messages by using standard forms provided by MAPI, or custom forms that have been registered with the form manager for the report's message class.</span></span> <span data-ttu-id="2c275-150">IPM の配信不能レポートを受信するクライアント。注メッセージでは、エラーが発生した受信者の一覧を示す標準の MAPI 形式と、エラーの提案された理由を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="2c275-150">Clients that receive a nondelivery report for an IPM.Note message, for example, can display the standard MAPI form that presents a list of the failed recipients and a suggested reason for the failure.</span></span> <span data-ttu-id="2c275-151">また、必要に応じて、ユーザーがメッセージを再送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="2c275-151">The form also enables the user to resend the message, if desired.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c275-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c275-152">See also</span></span>



[<span data-ttu-id="2c275-153">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="2c275-153">MAPI Messages</span></span>](mapi-messages.md)

