---
title: NDR の受信の集中管理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: af2531076755d1e183409f50fe1a0c97d28063f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405857"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>NDR の受信の集中管理

**適用対象**: Outlook 2013 | Outlook 2016 
  
**クライアントの複数のインスタンスが同時に実行されている場合に、配信不能レポート (ndr) を集中管理する場所に配信するには**
  
1. **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))、 **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md))、および**PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) を受信するアカウントの適切な値に設定します。レポート。 必要に応じて、 [IAddrBook:: createoneoff](iaddrbook-createoneoff.md)を呼び出して、エントリ id を作成します。 
    
2. レポートに対して要求したアカウントを無視するメッセージングシステムがあり、発信者に送信されることを理解します。 次の方法でレポートを移動する必要がある管理者に与える影響を軽減します。
    
- 元のメッセージに、IPM などの別のメッセージクラスを付与します。MSNNews。 MSNNews を使用して受信メッセージを検索し、送信者が報告する予定のアカウントに転送します。 同時に、配信不能レポートアカウントを無視する電子メールをメッセージングシステムに送信して、 **PR_REPORT_ENTRYID**プロパティを優先させる必要があることを伝えます。 
    
- **PR_REPORT_ENTRYID**を優先しないほとんどのメッセージングシステムでは、MAPI メッセージクラスの規則は適用されません。 そのため、メモのような内容が表示されます。 これは、入力が変数になるため、これを処理するのはやや困難です。 件名を参照して、"配信不能" または元の件名から何らかの単語があることを意味しているかどうかを確認します。 これらのリストを時間の経過とともに調整できるようにしておきます。 
    

