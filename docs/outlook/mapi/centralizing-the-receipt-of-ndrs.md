---
title: Ndr を受信確認を一元化すること。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 16a150105211231af54ccfdc5d1565aeecea729e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579439"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>Ndr を受信確認を一元化すること。

**適用されます**: Outlook 2013 |Outlook 2016 
  
**配信不能レポート (Ndr) が到着したを中心に、クライアントの複数のインスタンスを同時に実行しているとき**
  
1. **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))、 **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) と**PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) を受信するアカウントに適切な値に設定します。レポートします。 必要な場合に[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)を呼び出すことによって、エントリの識別子を作成します。 
    
2. アカウントをレポートの要求の発信者に送信するには、無視するためのメッセージング システムがあることを理解します。 レポートを移動する必要のある管理者に与える影響を減らします。
    
- IPM などの個別のメッセージ クラスでは、元のメッセージを提供します。Note.MSNNews。 クラス Report.IPM.Note.MSNNews.NDR で受信したメッセージを検索し、それら付属するレポートを意図したアカウントに転送します。 同時に、 **PR_REPORT_ENTRYID**プロパティを受け入れる必要があることを通信するために、配信不能レポートのアカウントを無視するためのメッセージング システムに電子メールを送信します。 
    
- **PR_REPORT_ENTRYID**を尊重しませんが、多くのメッセージング システムはこれを無視、MAPI メッセージ クラスの表記規則か。 したがって、メモのような結果が表示されます。 これは、入力が、変数のために対処するために少し困難になります。 件名を見るし、転送する場合は単語のリストから何かその意味を「配信不能」または何か、元の件名から。 時間の経過とともにこれらのリストを調整すること。 
    

