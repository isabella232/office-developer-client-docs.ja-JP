---
title: 状態テーブルと状態オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3eb190069b43ea1960c3b6edf30a9e0b782d2c41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425177"
---
# <a name="status-table-and-status-objects"></a>状態テーブルと状態オブジェクト

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi は、mapi サブシステム、mapi スプーラー、アドレス帳、または特定のサービスプロバイダーの状態に関する情報を表として提供します。 このテーブルにアクセスするには、 [imapisession:: getstatustable](imapisession-getstatustable.md)を呼び出します。
  
状態テーブルの各行は、MAPI またはサービスプロバイダーによって実装された状態オブジェクトを表します。 status オブジェクトを使用して、プロバイダーの構成プロパティシートを表示したり、プロバイダーパスワードを変更したり、メッセージをアップロードまたはダウンロードしたり、特定のトランスポートプロバイダーと通信したりすることができます。 
  
status オブジェクトには、次の2つの方法でアクセスできます。
  
- 状態テーブルを使用する
    
- ログオンオブジェクトの**openstatusentry**メソッドを使用する 
    
ログオンオブジェクトはクライアントで使用できないため、状態のオブジェクトにアクセスするには、状態テーブルを使用する必要があります。 状態テーブルの方法は間接的で、status オブジェクトが開かれる前にいくつかの呼び出しを必要とし、 **imapistatus**実装へのポインターが返されます。 
  
 **状態テーブルを使用して status オブジェクトを開くには**
  
1. Call **imapistatus:: getstatustable**が[IMAPITable](imapitableiunknown.md)ポインターを取得することができます。 
    
2. 状態テーブルの[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列セットを**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))、および**PR_DISPLAY_NAME** () に制限します ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. テーブルビューを特定のステータスオブジェクトに制限します。 MAPI 実装の場合、クライアントは**PR_RESOURCE_TYPE**を使用してプロパティ制限を定義できます。 サービスプロバイダーの実装では、クライアントは**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))、プロバイダーの名前、または**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) のプロバイダー DLL の名前を制限できます。拡張子.
    
4. [IMAPITable:: Restrict](imapitable-restrict.md)を呼び出して制限を設定します。 
    
5. プロバイダーの状態を表す行を取得するには、 [hrqueryallrows](hrqueryallrows.md)を呼び出し、 [spropertyrestriction](spropertyrestriction.md)構造を渡します。 
    
6. open [imapisession:: openentry](imapisession-openentry.md)。状態テーブルの行からエントリ識別子を指定して、status オブジェクトを開いて**imapisession**ポインターを取得します。 
    
プロパティシートを表示するには、対象プロバイダーの status オブジェクトの[imapistatus:: settingsdialog](imapistatus-settingsdialog.md)メソッドを呼び出します。 **settingsdialog**表示用のプロパティシートを表示します。場合によっては、プロバイダーの構成プロパティを変更します。 
  
トランスポートプロバイダーと通信するには、状態オブジェクトの[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドを呼び出します。 **validatestate**を使用すると、トランスポートプロバイダーを再構成し、プロバイダーがユーザーインターフェイスを表示できないようにしたり、渡されたフラグに応じてリモートサーバーからのメッセージヘッダーのダウンロードを伴うセッションを制御したりすることができます。 たとえば、リモートヘッダーのダウンロードを取り消すには、ABORT_XP_HEADER_OPERATION フラグを**validatestate**に渡します。 リモートサーバーとの接続または切断を行うには、FORCE_XP_CONNECT または FORCE_XP_DISCONNECT を渡します。 プロバイダーを再構成するには、CONFIG_CHANGED を渡します。 
  
オンデマンドでメッセージの送信または受信を実装するクライアントは、トランスポートプロバイダーまたは MAPI スプーラーの[imapistatus:: flushqueues](imapistatus-flushqueues.md)メソッドのいずれかを呼び出します。 FLUSH_UPLOAD、FLUSH_DOWNLOAD、および FLUSH_FORCE の3つのフラグをメソッドに渡すことができます。 FLUSH_UPLOAD は、プロバイダーまたは mapi スプーラーに対して、出力キューで待機しているメッセージを送信するように指示します。 FLUSH_DOWNLOAD は、受信メッセージを受信するようにプロバイダーまたは mapi スプーラーに指示します。 FLUSH_FORCE は他のフラグのいずれかを使用して設定することができます。この場合、状態オブジェクトは、タイミングに関係なく、フラッシュを実行します。 
  
どの mapi サブシステム、mapi スプーラー、またはアドレス帳状態オブジェクトでも、 **settingsdialog**または[ChangePassword](imapistatus-changepassword.md)を呼び出すことはできません。 サブシステムとアドレス帳の状態オブジェクトの両方が、 **validatestate**のみをサポートしています。MAPI スプーラー status オブジェクトは、 **validatestate**に加えて**flushqueues**をサポートします。
  
## <a name="see-also"></a>関連項目



[状態テーブル](status-tables.md)
  
[MAPI 状態オブジェクト](mapi-status-objects.md)

