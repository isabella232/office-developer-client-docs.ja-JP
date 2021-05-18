---
title: メッセージ サービス テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422496"
---
# <a name="message-service-tables"></a>メッセージ サービス テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ サービス テーブルには、現在のプロファイルのメッセージ サービスに関する情報が含まれている。 MAPI によって実装され、構成サポートを提供する特別な目的のクライアント アプリケーションによって使用される、MAPI セッションごとに 1 つのメッセージ サービス テーブルがあります。 
  
メッセージ サービス テーブルは静的テーブルです。
  
クライアントは [、IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) メソッドを呼び出して、メッセージ サービス テーブルにアクセスします。 
  
次のプロパティは、メッセージ サービス テーブルで必要な列セットを構成します。
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** は、メッセージ サービスの表示可能な名前と既定の並べ替えキー列です。 
  
 **PR_INSTANCE_KEY** テーブルのインデックス列として機能し、行を一意に識別します。 
  
 **PR_RESOURCE_FLAGS** サービスの機能について説明します。 
  
 **PR_SERVICE_DLL_NAME** は、メッセージ サービスの実装を含む DLL の名前です。 
  
 **PR_SERVICE_ENTRY_NAME** は [、MSGSERVICEENTRY](msgserviceentry.md) プロトタイプに準拠するメッセージ サービスのエントリ ポイント関数の名前です。 
  
 **PR_SERVICE_NAME** MAPISVC.INF の **[サービス] セクションの** 必須エントリです。 このプロパティの値は、変更またはローカライズされません。 **PR_SERVICE_NAME** メッセージ サービスをプログラムで識別するために使用できます。 
  
 **PR_SERVICE_SUPPORT_FILES** は、メッセージ サービスと一緒にインストールする必要があるファイルの一覧です。 
  
 **PR_SERVICE_UID** は、メッセージ サービスの一意の識別子です。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

