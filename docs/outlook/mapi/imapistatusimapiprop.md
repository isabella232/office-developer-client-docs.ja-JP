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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e36a987174ffb2abb4c0f5fc95bf695f31af942e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800719"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus : IMAPIProp

  
  
**適用対象**: Outlook 
  
MAPI サブシステム、内蔵のアドレス帳、および MAPI スプーラーに関するステータス情報を提供します。 サービス プロバイダーは、独自のステータスに関する情報を提供する**IMAPIStatus**を実装します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |ステータス オブジェクト  <br/> |
|によって実装されます。  <br/> |サービス プロバイダーおよび MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIStatus  <br/> |
|ポインターの型。  <br/> |LPMAPISTATUS  <br/> |
|トランザクション モデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |MAPI リソースまたはサービス プロバイダーの使用可能な外部のステータス情報を確認します。  <br/> |
|[SettingsDialog](imapistatus-settingsdialog.md) <br/> |サービス プロバイダーの構成を変更するユーザーを有効にするプロパティ シートを表示します。  <br/> |
|[パスワードの変更](imapistatus-changepassword.md) <br/> |ユーザー インターフェイスを表示せずには、サービス プロバイダーのパスワードを変更します。  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |送信またはアップロードまたはダウンロードをすぐに受信を待機しているすべてのメッセージを強制的にします。  <br/> |
   
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_PROVIDER_DLL_NAME**([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RESOURCE_METHODS**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_STATUS_CODE**([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

MAPI が実装している状態のオブジェクトでは、次のメソッドをサポートします。
  
|**ステータス オブジェクト**|**サポートされている方法**|
|:-----|:-----|
|MAPI サブシステム  <br/> |**ValidateState**のみ  <br/> |
|MAPI アドレス帳  <br/> |**ValidateState**のみ  <br/> |
|MAPI スプーラー  <br/> |**ValidateState**と**FlushQueues** <br/> |
   
MAPI を実装する状態オブジェクトは、 [IMAPIProp](imapipropiunknown.md)インターフェイスのメソッドの読み取り専用バージョンが存在し、 **ValidateState**メソッドをサポートするためには必要です。 トランスポート プロバイダーでは、 **FlushQueues**もサポートする必要があります。 すべてのプロバイダーは、 **SettingsDialog**; をサポートする必要があります。**パスワードの変更**はオプションをサポートします。 
  
クライアントは、構成を実行して、セッションの状態については、状態オブジェクトを使用します。 状態オブジェクトにアクセスするには、ログオンするサービス プロバイダー オブジェクトの**OpenStatusEntry**メソッドまたは状態オブジェクトを取得するために[IMAPISession::GetStatusTable](imapisession-getstatustable.md)メソッドを呼び出すことです。 
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

