---
title: MAPI レポートメッセージ
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
# <a name="mapi-report-messages"></a>MAPI レポートメッセージ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
レポートメッセージには、メッセージに関する状態情報が送信者に表示されます。
  
次の2種類の一般的なレポートメッセージがあります。
  
- 進捗レポートを読み取ります。
    
- 配信状態レポート
    
## <a name="read-status-reports"></a>進捗レポートの読み取り

読み取り状態レポートは、 [imapisupport:: readreceipt](imapisupport-readreceipt.md)メソッドへの呼び出しによって、メッセージストアプロバイダーによって開始され、 **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) のエントリ id で表される受信者に送信されます。プロパティ. 読み取り状態レポートは自動的に生成されません。それらを受信するクライアントアプリケーションは、明示的に要求する必要があります。
  
読み取りレポートは、メッセージの読み取りフラグが設定されていることを示します。これは、メッセージを開く、印刷、移動、またはコピーするときに発生する可能性があります。 メッセージストアプロバイダーが移動またはコピー操作に対する応答で読み取りレポートを生成するかどうかは、メッセージの送信先によって異なります。 別のメッセージストアに移動またはコピーされている場合、読み取りレポートは常に送信される可能性があります。 現在のメッセージストアで移動またはコピーされている場合は、読み取りレポートが送信される場合もあります。 
  
非開封レポートは、メッセージの読み取りフラグが設定されていないこと、およびメッセージが [削除済みアイテム] フォルダーに配置される前、または期限切れになる前に開かれていないことを示します。 クライアントは、 [IMessage:: setreadflag](imessage-setreadflag.md)または[imapifolder:: setreadflag](imapifolder-setreadflags.md)メソッドを呼び出して、メッセージの読み取りフラグを設定またはクリアすることができます。 
  
## <a name="delivery-status-reports"></a>配信状態レポート

配信状態は、メッセージが目的の受信者に達したときに送信される配信レポート、およびメッセージが受信者に到達できなかった場合に送信される配信不能レポートに反映されます。 配信状態レポートは、 **PR_REPORT_ENTRYID**プロパティのエントリ識別子で表される受信者、またはこのプロパティが存在しない場合は送信者に送信されます。 
  
配信レポートは、要求のみで送信され、元のメッセージは含まれません。 配信不能レポートは、非表示にする要求が行われない限り、自動的に送信されます。 配信不能レポートには、配信が問題なくなった場合に、レポートの受信者がメッセージを再送信できるように、元のメッセージが添付ファイルとして含まれています。 添付されたメッセージは、最初に送信するために[IMessage:: submitmessage](imessage-submitmessage.md)メソッドが呼び出されたときの元の状態と似ています。 
  
1つまたは複数の配信状態レポートは、 [imapisupport:: StatusRecips](imapisupport-statusrecips.md)メソッドを呼び出すと、トランスポートプロバイダーによって生成されます。 トランスポートプロバイダーは、メッセージの受信者のリストを作成します。 受信者がレポートを受信するかどうか、生成されるレポートの種類は、以下によって決まります。 
  
- 配信レポートメッセージがメッセージストアに置かれる前に、 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) プロパティが TRUE に設定されている受信者に移動します。
    
- 配信不能レポートは、 **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) プロパティが FALSE に設定されていない受信者に移動します。 
    
配信不能レポートを表示するために必要な情報のほとんどは、添付されたメッセージの recipient テーブルに含まれています。 レポート自体のプロパティはいくつかあります。 配信レポートの場合、必要な情報はレポートの recipient テーブルと、いくつかのレポートプロパティに含まれています。 
  
レポートは、送信されたメッセージのクラスに基づいて、個別のメッセージクラスを持つメッセージです。 ほとんどのサービスプロバイダーは、メッセージクラスがピリオドで区切られた複数の部分で構成される名前付け規則を使用します。 最初の部分は "report" で、最後の部分はレポートの種類を表す定数です。 中央の部分は、送信されたメッセージのクラスに対して予約されています。 たとえば、配信レポートは、IPM に関する配信レポートのメッセージクラスである定数 DR を使用しているためです。注意メッセージは、「**報告**されることを示しています。
  
次の表に、レポートの種類を表す定数を示します。
  
|**レポートの種類**|**メッセージクラスで使用される定数**|
|:-----|:-----|
|読み取り  <br/> |IPNRN  <br/> |
|未開封  <br/> |ipnnrn  <br/> |
|Delivery  <br/> |DR  <br/> |
|配信不能  <br/> |NDR  <br/> |
   
対話クライアントは、MAPI で提供される標準のフォームまたはレポートのメッセージクラスに対してフォームマネージャーに登録されているユーザー設定フォームを使用して、レポートメッセージを表示できます。 IPM の配信不能レポートを受信するクライアント。注メッセージでは、エラーが発生した受信者の一覧を示す標準の MAPI 形式と、エラーの提案された理由を表示することができます。 また、必要に応じて、ユーザーがメッセージを再送信することもできます。 
  
## <a name="see-also"></a>関連項目



[MAPI メッセージ](mapi-messages.md)

