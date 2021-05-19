---
title: Status Table オブジェクトと Status オブジェクト
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
# <a name="status-table-and-status-objects"></a>Status Table オブジェクトと Status オブジェクト

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、MAPI サブシステム、MAPI スプーラー、アドレス帳、または特定のサービス プロバイダーの状態に関する情報を表に提供します。 このテーブルにアクセスするには [、IMAPISession::GetStatusTable を呼び出します](imapisession-getstatustable.md)。
  
状態テーブルの各行は、MAPI またはサービス プロバイダーによって実装された状態オブジェクトを表します。 status オブジェクトを使用して、プロバイダーの構成プロパティ シートを表示したり、プロバイダー のパスワードを変更したり、メッセージをアップロードまたはダウンロードしたり、特定のトランスポート プロバイダーと通信することができます。 
  
状態オブジェクトにアクセスするには、次の 2 つの方法があります。
  
- 状態テーブルを使用する
    
- ログオン オブジェクトの **OpenStatusEntry メソッドを使用** する 
    
ログオン オブジェクトはクライアントでは使用できないので、状態オブジェクトにアクセスするには、状態テーブルを使用する必要があります。 状態テーブルのアプローチは間接的であり、status オブジェクトを開く前にいくつかの呼び出しが必要であり **、IMAPIStatus** 実装へのポインターが返されます。 
  
 **状態テーブルを使用して状態オブジェクトを開く方法**
  
1. **IMAPIStatus::GetStatusTable** を呼び出して [IMAPITable ポインターを取得](imapitableiunknown.md)します。 
    
2. 状態テーブルの [IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列セットを **PR_ENTRYID** [(PidTagEntryId)、PR_RESOURCE_TYPE](pidtagentryid-canonical-property.md)[(PidTagResourceType)、](pidtagresourcetype-canonical-property.md)および **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)に制限します。 
    
3. テーブル ビューを特定の状態オブジェクトに制限します。 MAPI の実装では、クライアントはプロパティの制限を使用して定義 **PR_RESOURCE_TYPE。** サービス プロバイダーの実装では、クライアントは **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)、プロバイダーの名前、または **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)、プロバイダー DLL ファイルの名前を制限できます。
    
4. [IMAPITable::Restrict を呼び出して](imapitable-restrict.md)制限を設定します。 
    
5. [HrQueryAllRows](hrqueryallrows.md)を呼び出し[、SPropertyRestriction](spropertyrestriction.md)構造体を渡して、プロバイダーの状態を表す行を取得します。 
    
6. STATUS オブジェクトを開き **、IMAPIStatus** ポインターを取得するには、状態テーブル行からエントリ識別子を指定して [、IMAPISession::OpenEntry](imapisession-openentry.md)を呼び出します。 
    
プロパティ シートを表示するには、ターゲット プロバイダーの [status オブジェクトの IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) メソッドを呼び出します。 **SettingsDialog は** 、プロバイダーの構成プロパティを変更して表示するプロパティ シートを表示し、場合によっては表示します。 
  
トランスポート プロバイダーと通信するには、その状態オブジェクトの [IMAPIStatus::ValidateState メソッドを呼び出](imapistatus-validatestate.md) します。 **ValidateState** では、トランスポート プロバイダーを再構成し、プロバイダーがユーザー インターフェイスを表示し、渡すフラグに応じて、リモート サーバーからメッセージ ヘッダーをダウンロードするセッションを制御できます。 たとえば、リモート ヘッダーのダウンロードを取り消す場合は、ABORT_XP_HEADER_OPERATION **ValidateState に渡します**。 リモート サーバーに接続または切断するには、リモート サーバー FORCE_XP_CONNECTまたはFORCE_XP_DISCONNECT。 プロバイダーを再構成するには、次のCONFIG_CHANGED。 
  
オンデマンドでメッセージの送受信を実装するクライアントは、トランスポート プロバイダーまたは MAPI スプーラーの [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) メソッドを呼び出します。 メソッドに 3 つのフラグを渡FLUSH_UPLOAD、FLUSH_DOWNLOAD、FLUSH_FORCE。 FLUSH_UPLOADは、プロバイダーまたは MAPI スプーラーに、FLUSH_DOWNLOAD がプロバイダーまたは MAPI スプーラーに受信メッセージを受信するように指示している間に、出力キューで待機しているメッセージを送信するように指示します。 FLUSH_FORCEフラグを設定すると、タイミングに関係なく status オブジェクトがフラッシュを実行します。 
  
MAPI サブシステム、MAPI スプーラー、またはアドレス帳の状態オブジェクトで **SettingsDialog** または [ChangePassword](imapistatus-changepassword.md) を呼び出せない。 サブシステムとアドレス帳の状態オブジェクトはどちらも **ValidateState のみをサポートします**。MAPI スプーラー状態オブジェクトは **ValidateState に加えて FlushQueues** **をサポートします**。
  
## <a name="see-also"></a>関連項目



[状態テーブル](status-tables.md)
  
[MAPI 状態オブジェクト](mapi-status-objects.md)

