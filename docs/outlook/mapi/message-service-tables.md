---
title: メッセージサービステーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356911"
---
# <a name="message-service-tables"></a>メッセージサービステーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービステーブルには、現在のプロファイルのメッセージサービスに関する情報が含まれています。 mapi によって実装され、構成のサポートを提供する特殊な目的のクライアントアプリケーションによって使用される、すべての mapi セッションに対して1つのメッセージサービステーブルがあります。 
  
メッセージサービステーブルは静的テーブルです。
  
クライアントは、 [IMsgServiceAdmin:: getmsgservicetable](imsgserviceadmin-getmsgservicetable.md)メソッドを呼び出して、メッセージサービステーブルにアクセスします。 
  
次のプロパティは、メッセージサービステーブルで必要な列セットを作成します。
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME**([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME**([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME**([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES**([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID**([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME**は、メッセージサービスの表示名と既定の並べ替えキー列です。 
  
 **PR_INSTANCE_KEY**は、行を一意に識別する、テーブルのインデックス列として機能します。 
  
 **PR_RESOURCE_FLAGS**メッセージサービスの機能について説明します。 
  
 **PR_SERVICE_DLL_NAME**は、メッセージサービスの実装を含む DLL の名前です。 
  
 **PR_SERVICE_ENTRY_NAME**は、 [msgserviceentry](msgserviceentry.md)プロトタイプに準拠したメッセージサービスのエントリポイント関数の名前です。 
  
 **PR_SERVICE_NAME**は、mapisvc.inf の **[Services]** セクションで必須のエントリです。 このプロパティの値は、変更またはローカライズされません。 **PR_SERVICE_NAME**を使用して、メッセージサービスをプログラムで識別できます。 
  
 **PR_SERVICE_SUPPORT_FILES**は、メッセージサービスと共にインストールする必要があるファイルの一覧です。 
  
 **PR_SERVICE_UID**は、メッセージサービスの一意の識別子です。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

