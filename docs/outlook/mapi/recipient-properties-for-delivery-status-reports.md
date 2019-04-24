---
title: 配信状態レポートの受信者プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9b2e287e-1cf8-4b8f-b92c-a065ed264d02
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 784cac21aac5de18952f3768af9b8f189f604981
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328435"
---
# <a name="recipient-properties-for-delivery-status-reports"></a>配信状態レポートの受信者プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者の配信状態レポートの場合、次のプロパティが存在します。 **PR_DELIVER_TIME**([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) は、配信不能レポートでは使用されません。 **PR_NDR_DIAG_CODE**([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md)) および**PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md)) は、配信不能レポートでのみ使用されます。
  
**表のタイトル**

|**Property**|**説明**|
|:-----|:-----|
|**PR_DELIVER_TIME**([PidTagDeliverTime](pidtagdelivertime-canonical-property.md))  <br/> |元のメッセージが配信された日付と時刻が含まれます。  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |指定した MAPI オブジェクトの表示名を格納します。  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |特定の mapi オブジェクトのプロパティを開いて編集するために使用する mapi エントリ識別子を含みます。  <br/> |
|**PR_NDR_DIAG_CODE**([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md))  <br/> |配信不能レポートの一部を形成する診断コードが含まれています。  <br/> |
|**PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |送信者が定義したメッセージクラス (IPM など) を識別するテキスト文字列を格納します。こと.  <br/> |
|**PR_NDR_REASON_CODE**([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md))  <br/> |配信不能レポートの一部を構成する、エンコードされていない理由を含みます。  <br/> |
|**PR_ORIGINAL_DISPLAY_NAME**([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))  <br/> |アドレス帳から個人用アドレス帳またはその他の書き込み可能なアドレス帳にコピーされたエントリの元の表示名を含みます。  <br/> |
|**PR_ORIGINAL_ENTRYID**([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md))  <br/> |アドレス帳から個人用アドレス帳またはその他の書き込み可能なアドレス帳にコピーされたエントリの元のエントリ識別子を含みます。  <br/> |
|**PR_ORIGINAL_SEARCH_KEY**([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md))  <br/> |アドレス帳から、個人用アドレス帳またはその他の書き込み可能なアドレス帳にコピーされたエントリの元の検索キーが含まれています。  <br/> |
|**PR_RECIPIENT_TYPE**([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |メッセージ受信者の受信者の種類が含まれます。  <br/> |
|**PR_REPORT_TEXT**([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |メッセージングシステムによって生成されるレポートのオプションのテキストが含まれています。  <br/> |
|**PR_REPORT_TIME**([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |メッセージングシステムがレポートを生成した日付と時刻を含みます。  <br/> |
|**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |検索の相関オブジェクトを識別する2つの比較可能なキーが含まれています。  <br/> |
|**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |表の特定の行にアイコンを関連付けるために使用される値を格納します。  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |オブジェクトの種類を格納します。  <br/> |
   

