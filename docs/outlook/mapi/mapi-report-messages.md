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
# <a name="mapi-report-messages"></a>MAPI レポート メッセージ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
レポート メッセージは、送信者にメッセージに関する状態情報を表示します。
  
レポート メッセージには、次の 2 種類の一般的な種類があります。
  
- 状態レポートの読み取り。
    
- 配信状態レポート。
    
## <a name="read-status-reports"></a>状態レポートの読み取り

読み取り状態レポートは [、IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) メソッドへの呼び出しを通じてメッセージ ストア プロバイダーによって開始され **、PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) プロパティのエントリ識別子によって表される受信者に送信されます。 読み取り状態レポートは自動的には生成されません。クライアント アプリケーションを受信する場合は、明示的に要求する必要があります。
  
読み取りレポートは、メッセージの読み取りフラグが設定済みで、メッセージが開か、印刷、移動、またはコピーされた場合に発生する可能性があります。 移動またはコピー操作に応答してメッセージ ストア プロバイダーが読み取りレポートを生成するかどうかは、メッセージの実行場所によって異なります。 別のメッセージ ストアに移動またはコピーされている場合は、読み取りレポートが常に送信される可能性が高い。 現在のメッセージ ストアで移動またはコピーされている場合は、読み取りレポートが送信される場合と送信されない場合があります。 
  
非読み取りレポートは、メッセージの読み取りフラグが設定されていないと、メッセージが [削除済みアイテム] フォルダーに配置される前、または期限の満了前に開かなかったかどうかを示します。 クライアントは [、IMessage::SetReadFlag](imessage-setreadflag.md) メソッドまたは [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) メソッドを呼び出して、メッセージの読み取りフラグを設定またはクリアできます。 
  
## <a name="delivery-status-reports"></a>配信状態レポート

配信状態は、メッセージが目的の受信者に達した場合に送信される配信レポートと、メッセージが受信者に到達できないときに送信される配信以外のレポートに反映されます。 配信状態レポートは **、PR_REPORT_ENTRYID** プロパティのエントリ識別子によって表される受信者に送信され、このプロパティが存在しない場合は送信者に送信されます。 
  
配信レポートは要求によってのみ送信され、元のメッセージは含めされません。 非送信レポートは、それらを抑制する要求が行われた場合を含め、自動的に送信されます。 配信以外のレポートには、元のメッセージが添付ファイルとして含まれるので、配信をブロックしたメッセージに問題がなくなった場合に備え、レポートの受信者がメッセージを再送信できます。 添付されたメッセージは [、IMessage::SubmitMessage](imessage-submitmessage.md) メソッドが最初に送信するために呼び出された場合と同様に、元のメッセージに似て表示されます。 
  
1 つ以上の配信状態レポートは、トランスポート プロバイダーが [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) メソッドを呼び出す際に生成されます。 トランスポート プロバイダーは、メッセージの受信者の一覧を作成します。 受信者がレポートを受信するかどうか、および生成されるレポートの種類は、次に依存します。 
  
- 配信レポートは、メッセージがメッセージ ストアに配置される前に **、PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) プロパティを TRUE に設定する受信者に移動します。
    
- 配信以外のレポートは、PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) プロパティを FALSE **に** 設定していない受信者に移動します。 
    
配信以外のレポートを表示するために必要な情報のほとんどすべてが、添付メッセージの受信者テーブルに含まれている。 いくつかのプロパティは、レポート自体からのものです。 配信レポートの場合、必要な情報はレポートの受信者テーブルといくつかのレポート プロパティに含まれる。 
  
レポートは、送信されたメッセージのクラスに基づいて、個別のメッセージ クラスを持つメッセージです。 ほとんどのサービス プロバイダーは名前付け規則を使用します。この場合、メッセージ クラスはピリオドで区切られた複数の部分で構成されます。 最初の部分は "Report" で、最後のパーツはレポートの種類を表す定数です。 中央の部分は、送信されたメッセージのクラス用に予約されています。 たとえば、配信レポートは定数 DR を使用します。IPM に関する配信レポートのメッセージ クラスです。メモ メッセージは **Report.IPM.Note.DR です**。
  
次の表に、レポートの種類を表す定数を示します。
  
|**レポートの種類**|**メッセージ クラスで使用される定数**|
|:-----|:-----|
|Read  <br/> |IPNRN  <br/> |
|Nonread  <br/> |IPNNRN  <br/> |
|Delivery  <br/> |DR  <br/> |
|Nondelivery  <br/> |NDR  <br/> |
   
対話型クライアントは、MAPI によって提供される標準フォーム、またはレポートのメッセージ クラスのフォーム マネージャーに登録されているカスタム フォームを使用して、レポート メッセージを表示できます。 IPM の非送信レポートを受け取るクライアント。メモ メッセージは、たとえば、失敗した受信者の一覧と、失敗の推奨される理由を示す標準の MAPI フォームを表示できます。 フォームを使用すると、必要に応じてメッセージを再送信できます。 
  
## <a name="see-also"></a>関連項目



[MAPI メッセージ](mapi-messages.md)

