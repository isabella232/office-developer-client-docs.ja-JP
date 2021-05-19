---
title: IABContainer IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348959"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳コンテナーへのアクセスを提供します。 MAPI およびクライアント アプリケーションは **、IABContainer** のメソッドを呼び出して、名前解決を実行し、受信者を作成、コピー、および削除します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |アドレス帳コンテナー オブジェクト  <br/> |
|実装元:  <br/> |アドレス帳プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI およびクライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IABContainer  <br/> |
|ポインターの種類:  <br/> |LPABCONT  <br/> |
|トランザクション モデル:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[CreateEntry](iabcontainer-createentry.md) <br/> |メッセージング ユーザー、配布リスト、または別のコンテナーを指定できる新しいエントリを作成します。  <br/> |
|[CopyEntries](iabcontainer-copyentries.md) <br/> |1 つ以上のエントリ (通常はメッセージング ユーザーまたは配布リスト) をコピーします。  <br/> |
|[DeleteEntries](iabcontainer-deleteentries.md) <br/> |1 つ以上のエントリ (通常はメッセージング ユーザー、配布リスト、その他のコンテナー) を削除します。  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |1 つ以上の受信者エントリの名前解決を実行します。  <br/> |
   
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
|**省略可能なプロパティ**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

**IABContainer** インターフェイスは [、IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)と [IMAPIProp : IUnknown](imapipropiunknown.md)インターフェイスを介して [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)インターフェイスから間接的に継承します。 アドレス帳プロバイダーは **、IABContainer インターフェイスを実装** します。 
  
任意の数のメッセージング ユーザー オブジェクト、配布リスト、その他のアドレス帳コンテナーは、アドレス帳コンテナーに存在できます。 任意のコンテナーと同様に、クライアントまたはサービス プロバイダーはアドレス帳コンテナーを使用して、エントリの 1 つを開く、または階層テーブルまたはコンテンツ テーブルを取得できます。 アドレス帳コンテナーは、名前解決を提供し、プロバイダーに応じて、エントリを追加、削除、または変更する機能も提供します。
  
MAPI は、他のコンテナーからコピーされたエントリを保持する個人用アドレス帳 (PAB) と呼ばれる特別なアドレス帳コンテナーを定義します。 PAB は常に変更可能です。 通常、ユーザーは PAB に、最も頻繁に通信する受信者を指定するエントリを設定します。 PAB は、アドレス帳コンテナーの一部ではない 1 回のアドレスと新しい受信者を保持することもできます。
  
## <a name="see-also"></a>関連項目

- [MAPI のインターフェイス](mapi-interfaces.md)

