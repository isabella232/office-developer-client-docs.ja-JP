---
title: MAPI レポート メッセージ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 824eb670-16b7-49bf-9992-39fe0586a552
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: addf93cadae418017a40ba448328d2e1fc1decf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801438"
---
# <a name="mapi-report-messages"></a><span data-ttu-id="b3392-103">MAPI レポート メッセージ</span><span class="sxs-lookup"><span data-stu-id="b3392-103">MAPI Report Messages</span></span>

  
  
<span data-ttu-id="b3392-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3392-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3392-105">送信者へのメッセージのステータス情報を表示メッセージを報告します。</span><span class="sxs-lookup"><span data-stu-id="b3392-105">Report messages present status information about a message to its sender.</span></span>
  
<span data-ttu-id="b3392-106">レポート メッセージの 2 つの一般的な種類があります。</span><span class="sxs-lookup"><span data-stu-id="b3392-106">There are two general types of report messages:</span></span>
  
- <span data-ttu-id="b3392-107">進捗レポートを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3392-107">Read status reports.</span></span>
    
- <span data-ttu-id="b3392-108">ステータス レポートを配信します。</span><span class="sxs-lookup"><span data-stu-id="b3392-108">Delivery status reports.</span></span>
    
## <a name="read-status-reports"></a><span data-ttu-id="b3392-109">ステータス レポート」を参照します。</span><span class="sxs-lookup"><span data-stu-id="b3392-109">Read Status Reports</span></span>

<span data-ttu-id="b3392-110">読み取りステータス レポートは、 [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md)メソッドを呼び出すことによって、メッセージ ストア プロバイダーによって開始され、 **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) のエントリの識別子によって表される受信者に送信されます。プロパティです。</span><span class="sxs-lookup"><span data-stu-id="b3392-110">Read status reports are initiated by message store providers through a call to the [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method and are sent to the recipient represented by the entry identifier in the **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="b3392-111">読み取りステータス レポートが自動的に生成されません。そのメッセージを受信するクライアント アプリケーションがそれらを明示的に要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3392-111">Read status reports are not generated automatically; client applications that want to receive them must explicitly request them.</span></span>
  
<span data-ttu-id="b3392-112">リードのレポートでは、メッセージを開く、印刷、移動、またはコピーするときに発生する、メッセージの読み取りのフラグが設定されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="b3392-112">A read report indicates that the read flag of a message has been set, which can occur when the message is opened, printed, moved, or copied.</span></span> <span data-ttu-id="b3392-113">メッセージ ストア プロバイダーでは、移動への応答の読み取りのレポートを生成するか、コピー操作は、メッセージがどこに依存するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b3392-113">Whether or not a message store provider generates a read report in response to a move or copy operation depends on where the message is going.</span></span> <span data-ttu-id="b3392-114">移動されたり、常に読み取りのレポートは、通常、別のメッセージ ストアにコピーが送信されます。</span><span class="sxs-lookup"><span data-stu-id="b3392-114">If it is being moved or copied to another message store, a read report will most likely always be sent.</span></span> <span data-ttu-id="b3392-115">されている場合、移動やコピーを現在のメッセージ ・ ストアに読み取りレポートもありますが送信されません。</span><span class="sxs-lookup"><span data-stu-id="b3392-115">If it is being moved or copied in the current message store, a read report might or might not be sent.</span></span> 
  
<span data-ttu-id="b3392-116">Nonread レポートは、メッセージの読み取りのフラグが設定されていないことと、削除済みアイテム フォルダー内に配置する前に、または制限時間の有効期限が切れる前に、メッセージが開いていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="b3392-116">A nonread report indicates that the read flag of a message is not set and that the message was not opened either before being placed in the Deleted Items folder or before the expiration of a time limit.</span></span> <span data-ttu-id="b3392-117">クライアントは、メッセージの読み取りのフラグを設定または[IMessage::SetReadFlag](imessage-setreadflag.md)または[IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="b3392-117">Clients can call the [IMessage::SetReadFlag](imessage-setreadflag.md) or [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) method to set or clear a message's read flag.</span></span> 
  
## <a name="delivery-status-reports"></a><span data-ttu-id="b3392-118">配信ステータス レポート</span><span class="sxs-lookup"><span data-stu-id="b3392-118">Delivery Status Reports</span></span>

<span data-ttu-id="b3392-119">配信のステータスは、配信レポート、メッセージがその受信者に達したときに送信されると、メッセージが受信者に到達できないときに送信される、配信不能レポートに反映されます。</span><span class="sxs-lookup"><span data-stu-id="b3392-119">Delivery status is reflected in a delivery report, which is sent when a message has reached its intended recipient, and in a nondelivery report, which is sent when a message could not reach a recipient.</span></span> <span data-ttu-id="b3392-120">配信状態レポートは、このプロパティが存在しない場合、 **PR_REPORT_ENTRYID**プロパティのエントリの識別子によって表される受信者または送信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="b3392-120">Delivery status reports are sent to the recipient represented by the entry identifier in the **PR_REPORT_ENTRYID** property or to the sender if this property is not present.</span></span> 
  
<span data-ttu-id="b3392-121">配信レポートは、要求のみが送信され、元のメッセージが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="b3392-121">Delivery reports are sent by request only and do not include the original message.</span></span> <span data-ttu-id="b3392-122">配信不能レポートは、それらを非表示にするが要求される場合を除き、自動的に送信されます。</span><span class="sxs-lookup"><span data-stu-id="b3392-122">Nondelivery reports are sent automatically unless a request is made to suppress them.</span></span> <span data-ttu-id="b3392-123">配信不能レポートには、レポートの受信者に配信がブロックされているどのような問題は、不要になった場合に、メッセージを再送信するを有効にするのには添付ファイルとして元のメッセージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3392-123">Nondelivery reports include the original message as an attachment to enable the report's recipient to resend the message in case whatever blocked the delivery is no longer a problem.</span></span> <span data-ttu-id="b3392-124">添付されたメッセージでは、最初に送信するのには、 [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドが呼び出されたときに存在していた、元が似ています。</span><span class="sxs-lookup"><span data-stu-id="b3392-124">The attached message resembles the original as it existed when the [IMessage::SubmitMessage](imessage-submitmessage.md) method was called to send it initially.</span></span> 
  
<span data-ttu-id="b3392-125">1 つまたは複数の配信状態レポートは、 [IMAPISupport::StatusRecips](imapisupport-statusrecips.md)メソッドを呼び出すときに、トランスポート プロバイダーによって生成されます。</span><span class="sxs-lookup"><span data-stu-id="b3392-125">One or more delivery status reports are generated by transport providers when they call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> <span data-ttu-id="b3392-126">トランスポート プロバイダーは、メッセージの受信者の一覧を作成します。</span><span class="sxs-lookup"><span data-stu-id="b3392-126">Transport providers compose a list of recipients for a message.</span></span> <span data-ttu-id="b3392-127">受信者がレポートされ、生成されるレポートの種類を受信するかどうかは、次に依存します。</span><span class="sxs-lookup"><span data-stu-id="b3392-127">Whether or not a recipient receives a report and the type of report that is generated depends on the following:</span></span> 
  
- <span data-ttu-id="b3392-128">配信レポートは、受信者、メッセージは、メッセージ ・ ストアに格納された前に、 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) プロパティを TRUE に設定するに進んでください。</span><span class="sxs-lookup"><span data-stu-id="b3392-128">Delivery reports go to recipients that set the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property to TRUE before the message was placed in the message store.</span></span>
    
- <span data-ttu-id="b3392-129">**PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) のプロパティを FALSE に設定しませんでしたの受信者に配信不能レポートが移動します。</span><span class="sxs-lookup"><span data-stu-id="b3392-129">Nondelivery reports go to recipients that did not set the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property to FALSE.</span></span> 
    
<span data-ttu-id="b3392-130">ほぼすべての配信不能レポートを表示するために必要な情報は、添付されたメッセージの受信者テーブルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3392-130">Almost all of the information necessary to display a nondelivery report is contained in the recipient table of the attached message.</span></span> <span data-ttu-id="b3392-131">レポート自体は、いくつかのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="b3392-131">A few properties are from the report itself.</span></span> <span data-ttu-id="b3392-132">配信レポートの場合は、レポートの受信者テーブルでは、いくつかのレポートのプロパティで、必要な情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3392-132">For delivery reports, the necessary information is contained in the recipient table of the report and in a few report properties.</span></span> 
  
<span data-ttu-id="b3392-133">レポートは、個別のメッセージ クラスでは、送信済みメッセージのクラスに基づくメッセージです。</span><span class="sxs-lookup"><span data-stu-id="b3392-133">Reports are messages with distinct message classes, based on the class of the sent message.</span></span> <span data-ttu-id="b3392-134">ほとんどのサービス プロバイダーは、メッセージ クラスがピリオドで区切られたいくつかの要素で構成される、名前付け規則を使用します。</span><span class="sxs-lookup"><span data-stu-id="b3392-134">Most service providers use a naming convention whereby the message class is composed of several parts separated by periods.</span></span> <span data-ttu-id="b3392-135">最初の部分は、「レポート」と、最後の部分は、レポート種類を表す定数です。</span><span class="sxs-lookup"><span data-stu-id="b3392-135">The first part is "Report" and the last part is a constant that represents the report type.</span></span> <span data-ttu-id="b3392-136">中央部は、送信済みメッセージのクラスに予約されています。</span><span class="sxs-lookup"><span data-stu-id="b3392-136">The middle part is reserved for the class of the sent message.</span></span> <span data-ttu-id="b3392-137">たとえば、配信レポートは、一定の DR を使用するため配信のメッセージ クラスは、IPM について報告します。注意のメッセージを" **Report.IPM.Note.DR**"となります。</span><span class="sxs-lookup"><span data-stu-id="b3392-137">For example, because a delivery report uses the constant DR, the message class for a delivery report about an IPM.Note message would be **Report.IPM.Note.DR**.</span></span>
  
<span data-ttu-id="b3392-138">レポートの種類を表す定数を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="b3392-138">The following table shows the constants that represent the types of reports.</span></span>
  
|<span data-ttu-id="b3392-139">**レポートの種類**</span><span class="sxs-lookup"><span data-stu-id="b3392-139">**Report type**</span></span>|<span data-ttu-id="b3392-140">**メッセージ クラスで使用される定数**</span><span class="sxs-lookup"><span data-stu-id="b3392-140">**Constant used in message class**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b3392-141">読み取り</span><span class="sxs-lookup"><span data-stu-id="b3392-141">Read</span></span>  <br/> |<span data-ttu-id="b3392-142">IPNRN</span><span class="sxs-lookup"><span data-stu-id="b3392-142">IPNRN</span></span>  <br/> |
|<span data-ttu-id="b3392-143">Nonread</span><span class="sxs-lookup"><span data-stu-id="b3392-143">Nonread</span></span>  <br/> |<span data-ttu-id="b3392-144">IPNNRN</span><span class="sxs-lookup"><span data-stu-id="b3392-144">IPNNRN</span></span>  <br/> |
|<span data-ttu-id="b3392-145">配信</span><span class="sxs-lookup"><span data-stu-id="b3392-145">Delivery</span></span>  <br/> |<span data-ttu-id="b3392-146">災害復旧</span><span class="sxs-lookup"><span data-stu-id="b3392-146">DR</span></span>  <br/> |
|<span data-ttu-id="b3392-147">配信不能</span><span class="sxs-lookup"><span data-stu-id="b3392-147">Nondelivery</span></span>  <br/> |<span data-ttu-id="b3392-148">NDR</span><span class="sxs-lookup"><span data-stu-id="b3392-148">NDR</span></span>  <br/> |
   
<span data-ttu-id="b3392-149">対話型クライアントは、MAPI によって提供される標準のフォームまたはレポートのメッセージ クラスのフォーム マネージャーに登録されているユーザー設定のフォームを使用して、レポート メッセージを表示できます。</span><span class="sxs-lookup"><span data-stu-id="b3392-149">Interactive clients can display report messages by using standard forms provided by MAPI, or custom forms that have been registered with the form manager for the report's message class.</span></span> <span data-ttu-id="b3392-150">IPM の配信不能レポートを受信するクライアントです。たとえば、注意のメッセージは、失敗した受信者と、エラーの推奨される理由の一覧が表示される標準の MAPI フォームを表示できます。</span><span class="sxs-lookup"><span data-stu-id="b3392-150">Clients that receive a nondelivery report for an IPM.Note message, for example, can display the standard MAPI form that presents a list of the failed recipients and a suggested reason for the failure.</span></span> <span data-ttu-id="b3392-151">フォームでは、必要な場合、ユーザーは、メッセージを再送信も可能です。</span><span class="sxs-lookup"><span data-stu-id="b3392-151">The form also enables the user to resend the message, if desired.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b3392-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="b3392-152">See also</span></span>



[<span data-ttu-id="b3392-153">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="b3392-153">MAPI Messages</span></span>](mapi-messages.md)

