---
title: これにより IMAPIContainer
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
ms.openlocfilehash: 0eb6d62b64595474957415e94275d0ac52cc2b6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800331"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**適用対象**: Outlook 
  
アドレス帳コンテナーへのアクセスを提供します。 MAPI およびクライアント アプリケーションの名前解決を実行しを作成するのには次のようにコピーして、**これにより**メソッドを呼び出すし、受信者を削除します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |アドレス帳コンテナー オブジェクト  <br/> |
|によって実装されます。  <br/> |アドレス帳プロバイダー  <br/> |
|によって呼び出されます。  <br/> |MAPI クライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IABContainer  <br/> |
|ポインターの型。  <br/> |LPABCONT  <br/> |
|トランザクション モデル:  <br/> |トランザクション処理  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[CreateEntry](iabcontainer-createentry.md) <br/> |メッセージングのユーザー、配布リスト、または別のコンテナーにすることができますが、新しいエントリを作成します。  <br/> |
|[CopyEntries](iabcontainer-copyentries.md) <br/> |1 つまたは複数のエントリ、メッセージを通常のユーザーまたは配布リストにコピーします。  <br/> |
|[DeleteEntries](iabcontainer-deleteentries.md) <br/> |一般ユーザー、配布リスト、またはその他のコンテナーをメッセージング、1 つまたは複数のエントリを削除します。  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |1 つまたは複数の受信者のエントリの名前解決を実行します。  <br/> |
   
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_FLAGS**([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
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
   
## <a name="remarks"></a>注釈

**これにより**インターフェイス継承しない直接[IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx)インターフェイスを通じて、 [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)と[IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェースです。 アドレス帳プロバイダーは、**これにより**インターフェイスを実装します。 
  
メッセージングのユーザー オブジェクト、配布リスト、およびその他のアドレス帳コンテナーの任意の数は、アドレス帳コンテナー内に存在できます。 同様に任意のコンテナーでは、クライアントまたはサービス プロバイダーを使用できます、アドレス帳コンテナーを開くには、エントリのいずれか、または階層のテーブルまたはテーブルの内容を取得します。 アドレス帳コンテナーも名前解決を提供し、削除、またはエントリを変更する機能を追加するには、プロバイダーによって異なります。
  
MAPI では、他のコンテナーからコピーしたエントリを保持する個人用アドレス帳 (PAB) と呼ばれる特別なアドレス帳コンテナーを定義します。 個人用アドレス帳は、常に変更できます。 ユーザーは、通常、最も頻繁に通信する受信者を指定するエントリを含む、個人用アドレス帳を設定します。 個人用アドレス帳も保持できる一時アドレスと受信者の新しいされていない任意のアドレス帳コンテナーの一部です。
  
## <a name="see-also"></a>関連項目

- [MAPI インターフェイス](mapi-interfaces.md)

