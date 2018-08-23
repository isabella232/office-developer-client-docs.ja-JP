---
title: MAPI レポート メッセージ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 824eb670-16b7-49bf-9992-39fe0586a552
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: addf93cadae418017a40ba448328d2e1fc1decf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801438"
---
# <a name="mapi-report-messages"></a>MAPI レポート メッセージ

  
  
**適用対象**: Outlook 
  
送信者へのメッセージのステータス情報を表示メッセージを報告します。
  
レポート メッセージの 2 つの一般的な種類があります。
  
- 進捗レポートを参照してください。
    
- ステータス レポートを配信します。
    
## <a name="read-status-reports"></a>ステータス レポート」を参照します。

読み取りステータス レポートは、 [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md)メソッドを呼び出すことによって、メッセージ ストア プロバイダーによって開始され、 **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) のエントリの識別子によって表される受信者に送信されます。プロパティです。 読み取りステータス レポートが自動的に生成されません。そのメッセージを受信するクライアント アプリケーションがそれらを明示的に要求する必要があります。
  
リードのレポートでは、メッセージを開く、印刷、移動、またはコピーするときに発生する、メッセージの読み取りのフラグが設定されていることを示します。 メッセージ ストア プロバイダーでは、移動への応答の読み取りのレポートを生成するか、コピー操作は、メッセージがどこに依存するかどうか。 移動されたり、常に読み取りのレポートは、通常、別のメッセージ ストアにコピーが送信されます。 されている場合、移動やコピーを現在のメッセージ ・ ストアに読み取りレポートもありますが送信されません。 
  
Nonread レポートは、メッセージの読み取りのフラグが設定されていないことと、削除済みアイテム フォルダー内に配置する前に、または制限時間の有効期限が切れる前に、メッセージが開いていないことを示します。 クライアントは、メッセージの読み取りのフラグを設定または[IMessage::SetReadFlag](imessage-setreadflag.md)または[IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)メソッドを呼び出すことができます。 
  
## <a name="delivery-status-reports"></a>配信ステータス レポート

配信のステータスは、配信レポート、メッセージがその受信者に達したときに送信されると、メッセージが受信者に到達できないときに送信される、配信不能レポートに反映されます。 配信状態レポートは、このプロパティが存在しない場合、 **PR_REPORT_ENTRYID**プロパティのエントリの識別子によって表される受信者または送信者に送信されます。 
  
配信レポートは、要求のみが送信され、元のメッセージが含まれていません。 配信不能レポートは、それらを非表示にするが要求される場合を除き、自動的に送信されます。 配信不能レポートには、レポートの受信者に配信がブロックされているどのような問題は、不要になった場合に、メッセージを再送信するを有効にするのには添付ファイルとして元のメッセージが含まれます。 添付されたメッセージでは、最初に送信するのには、 [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドが呼び出されたときに存在していた、元が似ています。 
  
1 つまたは複数の配信状態レポートは、 [IMAPISupport::StatusRecips](imapisupport-statusrecips.md)メソッドを呼び出すときに、トランスポート プロバイダーによって生成されます。 トランスポート プロバイダーは、メッセージの受信者の一覧を作成します。 受信者がレポートされ、生成されるレポートの種類を受信するかどうかは、次に依存します。 
  
- 配信レポートは、受信者、メッセージは、メッセージ ・ ストアに格納された前に、 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) プロパティを TRUE に設定するに進んでください。
    
- **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) のプロパティを FALSE に設定しませんでしたの受信者に配信不能レポートが移動します。 
    
ほぼすべての配信不能レポートを表示するために必要な情報は、添付されたメッセージの受信者テーブルに含まれています。 レポート自体は、いくつかのプロパティです。 配信レポートの場合は、レポートの受信者テーブルでは、いくつかのレポートのプロパティで、必要な情報が含まれています。 
  
レポートは、個別のメッセージ クラスでは、送信済みメッセージのクラスに基づくメッセージです。 ほとんどのサービス プロバイダーは、メッセージ クラスがピリオドで区切られたいくつかの要素で構成される、名前付け規則を使用します。 最初の部分は、「レポート」と、最後の部分は、レポート種類を表す定数です。 中央部は、送信済みメッセージのクラスに予約されています。 たとえば、配信レポートは、一定の DR を使用するため配信のメッセージ クラスは、IPM について報告します。注意のメッセージを" **Report.IPM.Note.DR**"となります。
  
レポートの種類を表す定数を次の表に示します。
  
|**レポートの種類**|**メッセージ クラスで使用される定数**|
|:-----|:-----|
|Read  <br/> |IPNRN  <br/> |
|Nonread  <br/> |IPNNRN  <br/> |
|配信  <br/> |災害復旧  <br/> |
|配信不能  <br/> |NDR  <br/> |
   
対話型クライアントは、MAPI によって提供される標準のフォームまたはレポートのメッセージ クラスのフォーム マネージャーに登録されているユーザー設定のフォームを使用して、レポート メッセージを表示できます。 IPM の配信不能レポートを受信するクライアントです。たとえば、注意のメッセージは、失敗した受信者と、エラーの推奨される理由の一覧が表示される標準の MAPI フォームを表示できます。 フォームでは、必要な場合、ユーザーは、メッセージを再送信も可能です。 
  
## <a name="see-also"></a>関連項目



[MAPI メッセージ](mapi-messages.md)

