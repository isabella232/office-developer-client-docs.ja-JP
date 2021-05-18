---
title: MAPI レポート メッセージ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 824eb670-16b7-49bf-9992-39fe0586a552
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: aab5c76fb268729f1a50a33e4764905fe3d53405
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405766"
---
# <a name="mapi-report-messages"></a><span data-ttu-id="47f9b-103">MAPI レポート メッセージ</span><span class="sxs-lookup"><span data-stu-id="47f9b-103">MAPI Report Messages</span></span>

  
  
<span data-ttu-id="47f9b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47f9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47f9b-105">レポート メッセージは、送信者にメッセージに関する状態情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="47f9b-105">Report messages present status information about a message to its sender.</span></span>
  
<span data-ttu-id="47f9b-106">レポート メッセージには、次の 2 種類の一般的な種類があります。</span><span class="sxs-lookup"><span data-stu-id="47f9b-106">There are two general types of report messages:</span></span>
  
- <span data-ttu-id="47f9b-107">状態レポートの読み取り。</span><span class="sxs-lookup"><span data-stu-id="47f9b-107">Read status reports.</span></span>
    
- <span data-ttu-id="47f9b-108">配信状態レポート。</span><span class="sxs-lookup"><span data-stu-id="47f9b-108">Delivery status reports.</span></span>
    
## <a name="read-status-reports"></a><span data-ttu-id="47f9b-109">状態レポートの読み取り</span><span class="sxs-lookup"><span data-stu-id="47f9b-109">Read Status Reports</span></span>

<span data-ttu-id="47f9b-110">読み取り状態レポートは [、IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) メソッドへの呼び出しを通じてメッセージ ストア プロバイダーによって開始され **、PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) プロパティのエントリ識別子によって表される受信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="47f9b-110">Read status reports are initiated by message store providers through a call to the [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method and are sent to the recipient represented by the entry identifier in the **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="47f9b-111">読み取り状態レポートは自動的には生成されません。クライアント アプリケーションを受信する場合は、明示的に要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47f9b-111">Read status reports are not generated automatically; client applications that want to receive them must explicitly request them.</span></span>
  
<span data-ttu-id="47f9b-112">読み取りレポートは、メッセージの読み取りフラグが設定済みで、メッセージが開か、印刷、移動、またはコピーされた場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="47f9b-112">A read report indicates that the read flag of a message has been set, which can occur when the message is opened, printed, moved, or copied.</span></span> <span data-ttu-id="47f9b-113">移動またはコピー操作に応答してメッセージ ストア プロバイダーが読み取りレポートを生成するかどうかは、メッセージの実行場所によって異なります。</span><span class="sxs-lookup"><span data-stu-id="47f9b-113">Whether or not a message store provider generates a read report in response to a move or copy operation depends on where the message is going.</span></span> <span data-ttu-id="47f9b-114">別のメッセージ ストアに移動またはコピーされている場合は、読み取りレポートが常に送信される可能性が高い。</span><span class="sxs-lookup"><span data-stu-id="47f9b-114">If it is being moved or copied to another message store, a read report will most likely always be sent.</span></span> <span data-ttu-id="47f9b-115">現在のメッセージ ストアで移動またはコピーされている場合は、読み取りレポートが送信される場合と送信されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="47f9b-115">If it is being moved or copied in the current message store, a read report might or might not be sent.</span></span> 
  
<span data-ttu-id="47f9b-116">非読み取りレポートは、メッセージの読み取りフラグが設定されていないと、メッセージが [削除済みアイテム] フォルダーに配置される前、または期限の満了前に開かなかったかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="47f9b-116">A nonread report indicates that the read flag of a message is not set and that the message was not opened either before being placed in the Deleted Items folder or before the expiration of a time limit.</span></span> <span data-ttu-id="47f9b-117">クライアントは [、IMessage::SetReadFlag](imessage-setreadflag.md) メソッドまたは [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) メソッドを呼び出して、メッセージの読み取りフラグを設定またはクリアできます。</span><span class="sxs-lookup"><span data-stu-id="47f9b-117">Clients can call the [IMessage::SetReadFlag](imessage-setreadflag.md) or [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) method to set or clear a message's read flag.</span></span> 
  
## <a name="delivery-status-reports"></a><span data-ttu-id="47f9b-118">配信状態レポート</span><span class="sxs-lookup"><span data-stu-id="47f9b-118">Delivery Status Reports</span></span>

<span data-ttu-id="47f9b-119">配信状態は、メッセージが目的の受信者に達した場合に送信される配信レポートと、メッセージが受信者に到達できないときに送信される配信以外のレポートに反映されます。</span><span class="sxs-lookup"><span data-stu-id="47f9b-119">Delivery status is reflected in a delivery report, which is sent when a message has reached its intended recipient, and in a nondelivery report, which is sent when a message could not reach a recipient.</span></span> <span data-ttu-id="47f9b-120">配信状態レポートは **、PR_REPORT_ENTRYID** プロパティのエントリ識別子によって表される受信者に送信され、このプロパティが存在しない場合は送信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="47f9b-120">Delivery status reports are sent to the recipient represented by the entry identifier in the **PR_REPORT_ENTRYID** property or to the sender if this property is not present.</span></span> 
  
<span data-ttu-id="47f9b-121">配信レポートは要求によってのみ送信され、元のメッセージは含めされません。</span><span class="sxs-lookup"><span data-stu-id="47f9b-121">Delivery reports are sent by request only and do not include the original message.</span></span> <span data-ttu-id="47f9b-122">非送信レポートは、それらを抑制する要求が行われた場合を含め、自動的に送信されます。</span><span class="sxs-lookup"><span data-stu-id="47f9b-122">Nondelivery reports are sent automatically unless a request is made to suppress them.</span></span> <span data-ttu-id="47f9b-123">配信以外のレポートには、元のメッセージが添付ファイルとして含まれるので、配信をブロックしたメッセージに問題がなくなった場合に備え、レポートの受信者がメッセージを再送信できます。</span><span class="sxs-lookup"><span data-stu-id="47f9b-123">Nondelivery reports include the original message as an attachment to enable the report's recipient to resend the message in case whatever blocked the delivery is no longer a problem.</span></span> <span data-ttu-id="47f9b-124">添付されたメッセージは [、IMessage::SubmitMessage](imessage-submitmessage.md) メソッドが最初に送信するために呼び出された場合と同様に、元のメッセージに似て表示されます。</span><span class="sxs-lookup"><span data-stu-id="47f9b-124">The attached message resembles the original as it existed when the [IMessage::SubmitMessage](imessage-submitmessage.md) method was called to send it initially.</span></span> 
  
<span data-ttu-id="47f9b-125">1 つ以上の配信状態レポートは、トランスポート プロバイダーが [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) メソッドを呼び出す際に生成されます。</span><span class="sxs-lookup"><span data-stu-id="47f9b-125">One or more delivery status reports are generated by transport providers when they call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> <span data-ttu-id="47f9b-126">トランスポート プロバイダーは、メッセージの受信者の一覧を作成します。</span><span class="sxs-lookup"><span data-stu-id="47f9b-126">Transport providers compose a list of recipients for a message.</span></span> <span data-ttu-id="47f9b-127">受信者がレポートを受信するかどうか、および生成されるレポートの種類は、次に依存します。</span><span class="sxs-lookup"><span data-stu-id="47f9b-127">Whether or not a recipient receives a report and the type of report that is generated depends on the following:</span></span> 
  
- <span data-ttu-id="47f9b-128">配信レポートは、メッセージがメッセージ ストアに配置される前に **、PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) プロパティを TRUE に設定する受信者に移動します。</span><span class="sxs-lookup"><span data-stu-id="47f9b-128">Delivery reports go to recipients that set the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property to TRUE before the message was placed in the message store.</span></span>
    
- <span data-ttu-id="47f9b-129">配信以外のレポートは、PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) プロパティを FALSE **に** 設定していない受信者に移動します。</span><span class="sxs-lookup"><span data-stu-id="47f9b-129">Nondelivery reports go to recipients that did not set the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property to FALSE.</span></span> 
    
<span data-ttu-id="47f9b-130">配信以外のレポートを表示するために必要な情報のほとんどすべてが、添付メッセージの受信者テーブルに含まれている。</span><span class="sxs-lookup"><span data-stu-id="47f9b-130">Almost all of the information necessary to display a nondelivery report is contained in the recipient table of the attached message.</span></span> <span data-ttu-id="47f9b-131">いくつかのプロパティは、レポート自体からのものです。</span><span class="sxs-lookup"><span data-stu-id="47f9b-131">A few properties are from the report itself.</span></span> <span data-ttu-id="47f9b-132">配信レポートの場合、必要な情報はレポートの受信者テーブルといくつかのレポート プロパティに含まれる。</span><span class="sxs-lookup"><span data-stu-id="47f9b-132">For delivery reports, the necessary information is contained in the recipient table of the report and in a few report properties.</span></span> 
  
<span data-ttu-id="47f9b-133">レポートは、送信されたメッセージのクラスに基づいて、個別のメッセージ クラスを持つメッセージです。</span><span class="sxs-lookup"><span data-stu-id="47f9b-133">Reports are messages with distinct message classes, based on the class of the sent message.</span></span> <span data-ttu-id="47f9b-134">ほとんどのサービス プロバイダーは名前付け規則を使用します。この場合、メッセージ クラスはピリオドで区切られた複数の部分で構成されます。</span><span class="sxs-lookup"><span data-stu-id="47f9b-134">Most service providers use a naming convention whereby the message class is composed of several parts separated by periods.</span></span> <span data-ttu-id="47f9b-135">最初の部分は "Report" で、最後のパーツはレポートの種類を表す定数です。</span><span class="sxs-lookup"><span data-stu-id="47f9b-135">The first part is "Report" and the last part is a constant that represents the report type.</span></span> <span data-ttu-id="47f9b-136">中央の部分は、送信されたメッセージのクラス用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="47f9b-136">The middle part is reserved for the class of the sent message.</span></span> <span data-ttu-id="47f9b-137">たとえば、配信レポートは定数 DR を使用します。IPM に関する配信レポートのメッセージ クラスです。メモ メッセージは **Report.IPM.Note.DR です**。</span><span class="sxs-lookup"><span data-stu-id="47f9b-137">For example, because a delivery report uses the constant DR, the message class for a delivery report about an IPM.Note message would be **Report.IPM.Note.DR**.</span></span>
  
<span data-ttu-id="47f9b-138">次の表に、レポートの種類を表す定数を示します。</span><span class="sxs-lookup"><span data-stu-id="47f9b-138">The following table shows the constants that represent the types of reports.</span></span>
  
|<span data-ttu-id="47f9b-139">**レポートの種類**</span><span class="sxs-lookup"><span data-stu-id="47f9b-139">**Report type**</span></span>|<span data-ttu-id="47f9b-140">**メッセージ クラスで使用される定数**</span><span class="sxs-lookup"><span data-stu-id="47f9b-140">**Constant used in message class**</span></span>|
|:-----|:-----|
|<span data-ttu-id="47f9b-141">Read</span><span class="sxs-lookup"><span data-stu-id="47f9b-141">Read</span></span>  <br/> |<span data-ttu-id="47f9b-142">IPNRN</span><span class="sxs-lookup"><span data-stu-id="47f9b-142">IPNRN</span></span>  <br/> |
|<span data-ttu-id="47f9b-143">Nonread</span><span class="sxs-lookup"><span data-stu-id="47f9b-143">Nonread</span></span>  <br/> |<span data-ttu-id="47f9b-144">IPNNRN</span><span class="sxs-lookup"><span data-stu-id="47f9b-144">IPNNRN</span></span>  <br/> |
|<span data-ttu-id="47f9b-145">Delivery</span><span class="sxs-lookup"><span data-stu-id="47f9b-145">Delivery</span></span>  <br/> |<span data-ttu-id="47f9b-146">DR</span><span class="sxs-lookup"><span data-stu-id="47f9b-146">DR</span></span>  <br/> |
|<span data-ttu-id="47f9b-147">Nondelivery</span><span class="sxs-lookup"><span data-stu-id="47f9b-147">Nondelivery</span></span>  <br/> |<span data-ttu-id="47f9b-148">NDR</span><span class="sxs-lookup"><span data-stu-id="47f9b-148">NDR</span></span>  <br/> |
   
<span data-ttu-id="47f9b-149">対話型クライアントは、MAPI によって提供される標準フォーム、またはレポートのメッセージ クラスのフォーム マネージャーに登録されているカスタム フォームを使用して、レポート メッセージを表示できます。</span><span class="sxs-lookup"><span data-stu-id="47f9b-149">Interactive clients can display report messages by using standard forms provided by MAPI, or custom forms that have been registered with the form manager for the report's message class.</span></span> <span data-ttu-id="47f9b-150">IPM の非送信レポートを受け取るクライアント。メモ メッセージは、たとえば、失敗した受信者の一覧と、失敗の推奨される理由を示す標準の MAPI フォームを表示できます。</span><span class="sxs-lookup"><span data-stu-id="47f9b-150">Clients that receive a nondelivery report for an IPM.Note message, for example, can display the standard MAPI form that presents a list of the failed recipients and a suggested reason for the failure.</span></span> <span data-ttu-id="47f9b-151">フォームを使用すると、必要に応じてメッセージを再送信できます。</span><span class="sxs-lookup"><span data-stu-id="47f9b-151">The form also enables the user to resend the message, if desired.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47f9b-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="47f9b-152">See also</span></span>



[<span data-ttu-id="47f9b-153">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="47f9b-153">MAPI Messages</span></span>](mapi-messages.md)

