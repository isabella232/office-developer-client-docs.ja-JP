---
title: メッセージ ストアの検証と初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2c8bf46bd9328d1e9da975c9fd39dbdf75605e5a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619485"
---
# <a name="validating-and-initializing-a-message-store"></a>メッセージ ストアの検証と初期化

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MDB_NO_MAIL フラグを設定せずに [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) メソッドを使用してメッセージ ストアを開く場合、MAPI は複数のフォルダーを作成し、既定の名前と役割を割り当てます。 MAPI は、クライアントまたはメッセージ ストア プロバイダーが作成の責任を負った場合に必然的に発生する非互換性を回避するために、これらのフォルダーを作成する責任があります。 
  
適切なフォルダーが作成され、有効なフォルダーを確認する必要がある場合があります。 [HrValidateIPMSubtree](hrvalidateipmsubtree.md)関数は、この目的のために使用できます。 既定のメッセージ ストアを検証する場合は、既定のメッセージ MAPI_FULL_IPM_TREE渡します。 既定のメッセージ ストア用に、フォルダーのより広範なグループが作成されます。 **HrValidateIPMSubtree** が MAPI_FULL_IPM_TREEフラグを受け取った場合、次のフォルダーがチェックされます。 
  
- IPM サブツリーのルート フォルダー
    
- IPM ルート フォルダー内の削除済みアイテム フォルダー
    
- IPM ルート フォルダー内の受信トレイ フォルダー
    
- IPM ルート フォルダー内の送信ボックス フォルダー
    
- IPM ルート フォルダーの [送信されたアイテム] フォルダー
    
- メッセージ ストアのルート フォルダー内のフォルダー ビュー
    
- メッセージ ストアのルート フォルダーの一般的なビュー
    
- メッセージ ストアのルート フォルダー内の検索フォルダー
    
メッセージ ストアが既定ではない場合は、メッセージ ストア フラグを設定または設定MAPI_FULL_IPM_TREEできます。 このフラグを設定しない場合 **、HrValidateIPMSubtree** は、サブツリーのルート フォルダー、削除済みアイテム フォルダー、およびメッセージ ストア検索結果のルート フォルダーのみをチェックします。 
  
メッセージ ストアを初期化するには、次のプロパティをメモリに格納して、すぐに使用できるようにします。
  
- **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
これらのプロパティは、メッセージ ストアの機能を記述するビットマスクです。 **PR_VALID_FOLDER_MASK** ストアに存在する特別なフォルダーごとに 1 ビットが設定され、有効なエントリ識別子が割り当てられます。 これらのフォルダーとそのエントリ識別子へのアクセスの詳細については、「メッセージ ストア フォルダーを開 [く」を参照してください](opening-a-message-store-folder.md)。 
  
 **PR_STORE_SUPPORT_MASK** ストアでサポートされる機能ごとに 1 ビットが設定されています。 たとえば、メッセージ ストアで通知と書式設定されたテキストがサポートされている場合、メッセージ ストアのPR_STORE_SUPPORT_MASKビットとSTORE_NOTIFY_OKビットSTORE_RTF_OK設定されます。 
  
ローカルに保存する必要があるその他のプロパティには、PR_VALID_FOLDER_MASK **プロパティが** 有効と記述するフォルダーのエントリ識別子が含まれます。 受信トレイ フォルダーを除くこれらの特別なフォルダーのそれぞれには、エントリ識別子プロパティが関連付けられている。 たとえば、Outbox フォルダーのエントリ識別子は、PR_IPM_OUTBOX_ENTRYID **(** [PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) プロパティです。 これらのフォルダーは頻繁に開くフォルダーなので、エントリ識別子を簡単に使用できるようにしてください。
  

