---
title: 配信ステータス レポートの受信者のプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9b2e287e-1cf8-4b8f-b92c-a065ed264d02
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a6ff82fa3cc4a7ad243285e9eb93b0ec880a3bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803712"
---
# <a name="recipient-properties-for-delivery-status-reports"></a>配信ステータス レポートの受信者のプロパティ

  
  
**適用されます**: Outlook 
  
受信者に対する配信状態レポートの次のプロパティが存在します。 **PR_DELIVER_TIME**([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) は、配信不能レポートでは使用されません。 **PR_NDR_DIAG_CODE**([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md)) **PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md)) は、配信不能レポートでのみ使用しています。
  
**テーブルのタイトル**

|**プロパティ**|**説明**|
|:-----|:-----|
|**PR_DELIVER_TIME**([PidTagDeliverTime](pidtagdelivertime-canonical-property.md))  <br/> |元のメッセージが配信されたときの日時が含まれています。  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |特定の MAPI オブジェクトの表示名が含まれています。  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |開き、特定の MAPI オブジェクトのプロパティを編集するに使用される MAPI エントリの識別子が含まれています。  <br/> |
|**PR_NDR_DIAG_CODE**([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md))  <br/> |配信不能レポートの一部を形成する診断コードが含まれています。  <br/> |
|**PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |IPM などのメッセージの送信者が定義されているクラスを識別する文字列が含まれています。注意してください。  <br/> |
|**PR_NDR_REASON_CODE**([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md))  <br/> |配信不能、配信不能レポートの一部を形成するためにエンコードが含まれています。  <br/> |
|**PR_ORIGINAL_DISPLAY_NAME**([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))  <br/> |個人用アドレス帳またはその他の書き込み可能なアドレス帳をアドレス帳からコピーされるエントリの元の表示名が含まれています。  <br/> |
|**PR_ORIGINAL_ENTRYID**([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md))  <br/> |個人用アドレス帳にアドレス帳やその他の書き込み可能なアドレス帳からコピーしたエントリの元のエントリ id が含まれています。  <br/> |
|**PR_ORIGINAL_SEARCH_KEY**([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md))  <br/> |個人用アドレス帳にアドレス帳やその他の書き込み可能なアドレス帳からコピーしたエントリの元の検索キーが含まれています。  <br/> |
|**PR_RECIPIENT_TYPE**([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |メッセージの受信者の受信者の種類が含まれています。  <br/> |
|**PR_REPORT_TEXT**([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |メッセージング システムによって生成されたレポートのオプションの文字列が含まれています。  <br/> |
|**PR_REPORT_TIME**([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |メッセージング システムにレポートが生成されたときの日時が含まれています。  <br/> |
|**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |検索の相関関係を持つオブジェクトを識別するバイナリの比較可能なキーが含まれています。  <br/> |
|**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |テーブルの特定の行にアイコンを関連付けるに使用する値が含まれています。  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |オブジェクトの種類が含まれています。  <br/> |
   
