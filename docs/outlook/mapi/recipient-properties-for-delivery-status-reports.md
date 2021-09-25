---
title: 配信状態レポートの受信者プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9b2e287e-1cf8-4b8f-b92c-a065ed264d02
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1063d1a7a062b8b07d9ff66958efc5e65ef8737e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591312"
---
# <a name="recipient-properties-for-delivery-status-reports"></a>配信状態レポートの受信者プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者の配信状態レポートには、次のプロパティがあります。 **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) は配信不可レポートでは使用されません。 **PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md)) と **PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md)) は配信不可レポートでのみ使用されます。
  
**表のタイトル**

|**プロパティ**|**説明**|
|:-----|:-----|
|**PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md))  <br/> |元のメッセージが配信された日時を格納します。  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |特定の MAPI オブジェクトの表示名を格納します。  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |特定の MAPI オブジェクトのプロパティを開いて編集するために使用される MAPI エントリ識別子が含まれる。  <br/> |
|**PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md))  <br/> |配信不可レポートの一部を形成する診断コードが含まれる。  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |IPM.Note など、送信者が定義したメッセージ クラスを識別するテキスト文字列が含まれます。  <br/> |
|**PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md))  <br/> |配信不可レポートの一部を形成する配信不可のエンコードされた理由が含まれる。  <br/> |
|**PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))  <br/> |アドレス帳から個人用アドレス帳または他の書き込み可能なアドレス帳にコピーされたエントリの元の表示名を含む。  <br/> |
|**PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md))  <br/> |アドレス帳から個人用アドレス帳または他の書き込み可能なアドレス帳にコピーされたエントリの元のエントリ識別子が含まれる。  <br/> |
|**PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md))  <br/> |アドレス帳から個人用アドレス帳または他の書き込み可能なアドレス帳にコピーされたエントリの元の検索キーを格納します。  <br/> |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |メッセージ受信者の受信者の種類を含む。  <br/> |
|**PR_REPORT_TEXT** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |メッセージング システムによって生成されたレポートのオプションのテキストが含まれる。  <br/> |
|**PR_REPORT_TIME** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |メッセージング システムがレポートを生成した日時を格納します。  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |検索の関連オブジェクトを識別するバイナリ比較可能なキーが含まれています。  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |アイコンをテーブルの特定の行に関連付けるのに使用する値を含む。  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |オブジェクトの種類を格納します。  <br/> |
   

