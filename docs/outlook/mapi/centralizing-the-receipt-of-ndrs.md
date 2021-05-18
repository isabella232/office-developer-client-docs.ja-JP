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
  
**クライアントの複数のインスタンスが同時に実行されている場合に、非送信レポート (NDRs) を中央の場所に到着するには**
  
1. PR_REPORT_ENTRYID  ([PidTagReportEntryId)](pidtagreportentryid-canonical-property.md) **、PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md))、**および PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) を、レポートを受信するアカウントの適切な値に設定します。 必要に応じて [、IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) を呼び出してエントリ識別子を作成します。 
    
2. レポートに対して要求したアカウントを無視して発信元に送信するメッセージング システムが含まれたと理解します。 次の方法でレポートを移動する必要がある管理者に与える影響を軽減します。
    
- 元のメッセージに IPM などの個別のメッセージ クラスを与える。Note.MSNNews. Report.IPM.Note.MSNNews.NDR クラスの受信メッセージを探し、レポートを作成するアカウントに転送します。 同時に、メッセージ システムに電子メールを送信し、配信以外のレポート アカウントを無視して、PR_REPORT_ENTRYID プロパティ **を尊重する必要PR_REPORT_ENTRYID** します。 
    
- MAPI メッセージ クラスの規則をPR_REPORT_ENTRYIDしないほとんどのメッセージング システム。 したがって、メモのように見えるメッセージが表示されます。 これは、入力が非常に可変なので、処理が少し難しくなります。 件名を見て、"配信不能" を意味する単語のリストから何かを見つけた場合、または元の件名から何かを見つけた場合に転送します。 これらのリストを時間の間に調整する準備をしてください。 
    

