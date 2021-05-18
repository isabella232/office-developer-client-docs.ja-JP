---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408300"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI サブシステム、統合アドレス帳、および MAPI スプーラーに関する状態情報を提供します。 サービス プロバイダーは **IMAPIStatus を実装して、** 独自の状態に関する情報を提供します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |状態オブジェクト  <br/> |
|実装元:  <br/> |サービス プロバイダーと MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIStatus  <br/> |
|ポインターの種類:  <br/> |LPMAPISTATUS  <br/> |
|トランザクション モデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |MAPI リソースまたはサービス プロバイダーで使用可能な外部状態情報を確認します。  <br/> |
|[SettingsDialog](imapistatus-settingsdialog.md) <br/> |ユーザーがサービス プロバイダーの構成を変更できるプロパティ シートを表示します。  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |ユーザー インターフェイスを表示せずにサービス プロバイダーのパスワードを変更します。  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |送信または受信を待機しているすべてのメッセージを、すぐにアップロードまたはダウンロードする必要があります。  <br/> |
   
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

MAPI が実装する状態オブジェクトは、次のメソッドをサポートしています。
  
|**Status オブジェクト**|**サポートされているメソッド**|
|:-----|:-----|
|MAPI サブシステム  <br/> |**ValidateState** のみ  <br/> |
|MAPI アドレス帳  <br/> |**ValidateState** のみ  <br/> |
|MAPI スプーラー  <br/> |**ValidateState** と **FlushQueues** <br/> |
   
MAPI が実装する状態オブジェクトは [、IMAPIProp](imapipropiunknown.md) インターフェイスのメソッドの読み取り専用バージョンを持ち **、ValidateState** メソッドをサポートするために必要です。 トランスポート プロバイダーは **、FlushQueues もサポートする必要があります**。 すべてのプロバイダーが **SettingsDialog をサポートする必要があります**。 **ChangePassword のサポートは** オプションです。 
  
クライアントは、状態オブジェクトを使用して構成を実行し、セッションの状態について学習します。 サービス プロバイダー ログオン オブジェクトの **OpenStatusEntry** メソッドまたは [IMAPISession::GetStatusTable](imapisession-getstatustable.md) メソッドを呼び出して、状態オブジェクトにアクセスして、状態オブジェクトを取得します。 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

