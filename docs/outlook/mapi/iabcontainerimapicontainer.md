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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348959"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳コンテナーへのアクセスを提供します。 MAPI およびクライアントアプリケーションは、 **IABContainer**のメソッドを呼び出して、名前の解決を行い、受信者の作成、コピー、および削除を行います。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |アドレス帳のコンテナーオブジェクト  <br/> |
|実装元:  <br/> |アドレス帳プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI およびクライアントアプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IABContainer  <br/> |
|ポインターの種類:  <br/> |lpabcont  <br/> |
|トランザクションモデル:  <br/> |一括  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[createentry](iabcontainer-createentry.md) <br/> |新しいエントリを作成します。これは、メッセージングユーザー、配布リスト、または別のコンテナーにすることができます。  <br/> |
|[copyentries](iabcontainer-copyentries.md) <br/> |1つまたは複数のエントリ (通常はメッセージングユーザーまたは配布リスト) をコピーします。  <br/> |
|[「spaudit.deleteentries](iabcontainer-deleteentries.md) <br/> |1つ以上のエントリ (通常、メッセージングユーザー、配布リスト、またはその他のコンテナー) を削除します。  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |1つまたは複数の受信者エントリの名前解決を実行します。  <br/> |
   
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_FLAGS**([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
|**省略可能なプロパティ**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_DEF_CREATE_DL**([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_DEF_CREATE_MAILUSER**([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>解説

**IABContainer**インターフェイスは、 [IMAPIContainer: imapiprop](imapicontainerimapiprop.md)および[imapiprop: iunknown](imapipropiunknown.md)インターフェイスを介して、 [iunknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)インターフェイスから間接的に継承されます。 アドレス帳プロバイダーは**IABContainer**インターフェイスを実装します。 
  
アドレス帳コンテナーには、任意の数のメッセージングユーザーオブジェクト、配布リスト、およびその他のアドレス帳コンテナーを含めることができます。 他のコンテナーと同様に、クライアントまたはサービスプロバイダーは、アドレス帳コンテナーを使用して、そのエントリの1つを開くか、階層テーブルまたは contents テーブルを取得することができます。 また、アドレス帳コンテナーは、プロバイダーによって、エントリの追加、削除、または変更を行うことができる、名前解決を提供します。
  
MAPI は、他のコンテナーからコピーされたエントリを保持する個人用アドレス帳 (PAB) と呼ばれる特別なアドレス帳コンテナーを定義します。 PAB は常に変更可能です。 通常、ユーザーは、最も頻繁に通信する受信者を指定するエントリを PAB に設定します。 また、PAB は、アドレス帳コンテナーの一部ではない、一時アドレスと新しい受信者を保持することもできます。
  
## <a name="see-also"></a>関連項目

- [MAPI のインターフェイス](mapi-interfaces.md)

