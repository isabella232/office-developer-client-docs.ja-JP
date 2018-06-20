---
title: 状態テーブルとオブジェクトの状態
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 774aaea0365066981b9d6426a2579160f6578844
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804008"
---
# <a name="status-table-and-status-objects"></a>状態テーブルとオブジェクトの状態

  
  
**適用されます**: Outlook 
  
MAPI は MAPI のサブシステム、MAPI スプーラー、アドレス帳、または特定のサービス プロバイダーのステータスに関する情報を持つテーブルを提供します。 [IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出すことによってこのテーブルにアクセスできます。
  
状態テーブル内の各行は、MAPI またはサービス プロバイダーによって実装される状態オブジェクトを表します。 アップロードまたはメッセージをダウンロードしてのに、特定のトランスポート プロバイダーと通信するのにプロバイダーのパスワードを変更するのには、プロバイダーの設定] プロパティ シートを表示するのには、状態オブジェクトを使用できます。 
  
状態オブジェクトにアクセスするための 2 つの方法があります。
  
- 状態テーブルを
    
- ログオン オブジェクトの**OpenStatusEntry**メソッドを使用 
    
ログオン オブジェクトがクライアントに使用可能なため、状態オブジェクトにアクセスするのにはステータス ・ テーブルを使わなければなりません。 状態テーブルのアプローチは、いくつかの呼び出しを必要とする状態オブジェクトが開かれ、その**IMAPIStatus**実装へのポインターが返される前に、直接ではありません。 
  
 **開くには、状態オブジェクトの状態テーブルを使用するには**
  
1. [IMAPITable](imapitableiunknown.md)ポインターを取得するために**IMAPIStatus::GetStatusTable**を呼び出します。 
    
2. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) および**PR_DISPLAY_NAME** ([に設定する列を制限するのには、状態テーブルの[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出すPidTagDisplayName](pidtagdisplayname-canonical-property.md))。
    
3. 特定のステータスのオブジェクトをテーブルのビューを制限します。 MAPI 実装では、クライアントは**PR_RESOURCE_TYPE**を使用してプロパティの制限を定義できます。 **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))、プロバイダーの名前や**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) は、プロバイダーの DLL の名前サービス プロバイダー実装では、クライアントを制限することができます。ファイルです。
    
4. 制限を設定するのには[IMAPITable::Restrict](imapitable-restrict.md)を呼び出します。 
    
5. [HrQueryAllRows](hrqueryallrows.md)、 [SPropertyRestriction](spropertyrestriction.md)構造体を渡すことを呼び出し、プロバイダーの状態を表す行を取得します。 
    
6. [IMAPISession::OpenEntry](imapisession-openentry.md)、状態テーブルの行からのエントリ id を指定する状態オブジェクトを開き、 **IMAPIStatus**ポインターを取得するを呼び出します。 
    
プロパティ シートを表示するには、対象のプロバイダーの状態のオブジェクトの[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドを呼び出します。 **SettingsDialog**では、プロバイダーの構成のプロパティを変更する表示のため、場合によっては、プロパティ シートを表示します。 
  
トランスポート プロバイダーとの通信をするには、その状態のオブジェクトの[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドを呼び出します。 **ValidateState**は、トランスポート プロバイダーを再構成品を獲得し、プロバイダーが、ユーザー インターフェイスを表示しないようにするに渡されるフラグの設定により、リモート サーバーからのメッセージ ヘッダーのダウンロードに関連するセッションを制御できます。 たとえば、リモート ヘッダーのダウンロードをキャンセルするには、 **ValidateState**に ABORT_XP_HEADER_OPERATION フラグを渡します。 リモート サーバーから切断、または接続するには、FORCE_XP_CONNECT または FORCE_XP_DISCONNECT を渡します。 プロバイダーを再設定するには、CONFIG_CHANGED を渡します。 
  
要求時にメッセージの送信または受信を実装するクライアントは、トランスポート プロバイダーのまたは MAPI スプーラーのいずれかの[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドを呼び出します。 メソッドに 3 つのフラグを渡すことができます: FLUSH_UPLOAD、FLUSH_DOWNLOAD、および FLUSH_FORCE。 FLUSH_UPLOAD は、着信メッセージを受信するプロバイダーまたは FLUSH_DOWNLOAD プロバイダーを指示するときに、出力キューで待機しているすべてのメッセージを送信するのには、MAPI スプーラーを無効、または MAPI スプーラーに指示します。 FLUSH_FORCE は、タイミングに関係なく、フラッシュを実行する状態オブジェクトが発生する他のフラグのいずれかを設定できます。 
  
呼び出せるように**SettingsDialog**または[パスワードの変更](imapistatus-changepassword.md)を、MAPI サブシステム、MAPI スプーラーを無効、またはアドレスのいずれかの書籍の状態のオブジェクトにされないようにします。 のみ、サブシステムとアドレス帳のステータスのオブジェクトがサポートしている**ValidateState**です。MAPI スプーラーの状態オブジェクトは、 **ValidateState**だけでなく、 **FlushQueues**をサポートします。
  
## <a name="see-also"></a>関連項目



[ステータス ・ テーブル](status-tables.md)
  
[MAPI オブジェクトのステータス](mapi-status-objects.md)

