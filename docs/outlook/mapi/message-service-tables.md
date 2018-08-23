---
title: メッセージ サービス テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 81772115fcd4f081718dd560759f6ab93dc7c11c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801652"
---
# <a name="message-service-tables"></a>メッセージ サービス テーブル

  
  
**適用対象**: Outlook 
  
メッセージ サービス テーブルには、現在のプロファイル内のメッセージ サービスに関する情報が含まれています。 MAPI セッションごとに MAPI によって実装され、構成のサポートを提供する特別な目的のクライアント アプリケーションによって使用されるメッセージ サービスの 1 つのテーブルがあります。 
  
メッセージ サービス テーブルは、静的なテーブルです。
  
クライアントは、 [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)メソッドを呼び出して、メッセージ サービス テーブルをアクセスします。 
  
次のプロパティは、メッセージ サービス テーブルを設定する必要な列を構成します。
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME**([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME**([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME**([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES**([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID**([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME**は、メッセージ サービス、および既定の並べ替えのキー列の表示可能な名前です。 
  
 **PR_INSTANCE_KEY**は、行を一意に識別するテーブルのインデックス列として機能します。 
  
 **PR_RESOURCE_FLAGS**では、メッセージ サービスの機能について説明します。 
  
 **PR_SERVICE_DLL_NAME**は、メッセージ サービスの実装を含む DLL の名前です。 
  
 **PR_SERVICE_ENTRY_NAME**は、 [MSGSERVICEENTRY](msgserviceentry.md)のプロトタイプに準拠しているメッセージ サービスのエントリ ポイント関数の名前です。 
  
 **PR_SERVICE_NAME**は、MAPISVC.INF の **[サービス]** セクションで必要なエントリです。 このプロパティの値の変更またはローカライズされたことはありませんが。 メッセージ サービスをプログラムで識別する**PR_SERVICE_NAME**を使用することができます。 
  
 **PR_SERVICE_SUPPORT_FILES**は、メッセージ サービスをインストールする必要があるファイルの一覧です。 
  
 **PR_SERVICE_UID**は、メッセージ サービスの一意の識別子です。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

