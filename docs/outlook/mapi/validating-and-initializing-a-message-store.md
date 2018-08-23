---
title: メッセージ ストアの検証と初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7a5a5045594e87953d967fddbdeefd5ac18c8a3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581973"
---
# <a name="validating-and-initializing-a-message-store"></a>メッセージ ストアの検証と初期化

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MDB_NO_MAIL フラグを設定せずには、 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)メソッドで、メッセージ ストアを開く、MAPI はいくつかのフォルダーを作成し、それらに既定の名前とロールを割り当てます。 MAPI は、クライアントまたはメッセージ ストア プロバイダーの作成を担当する場合としない発生する必然的に非互換性を避けるためにこれらのフォルダーを作成する必要があります。 
  
適切なフォルダーが作成されていると、有効であることを確認する必要があります。 [HrValidateIPMSubtree](hrvalidateipmsubtree.md)関数は、この目的のために使用できます。 既定のメッセージ ストアを検査する場合は、MAPI_FULL_IPM_TREE フラグを渡します。 フォルダーのより広範なグループは、既定のメッセージ ストアに作成されます。 **HrValidateIPMSubtree**は、MAPI_FULL_IPM_TREE フラグを受信すると、次のフォルダーをチェックします。 
  
- IPM サブツリーのルート フォルダー
    
- IPM のルート フォルダー内の削除済みアイテム フォルダー
    
- IPM ルート フォルダー内の [受信トレイ] フォルダー
    
- IPM のルート フォルダー内のフォルダーを [送信トレイ] します。
    
- IPM のルート フォルダー内のアイテム] フォルダーの送信
    
- メッセージ ストアのルート フォルダーにフォルダーの表示
    
- メッセージ ストアのルート フォルダー内の共通のビュー
    
- メッセージ ストアのルート フォルダーにフォルダーを検索
    
メッセージ ・ ストアが既定値でない場合は、設定か、MAPI_FULL_IPM_TREE フラグが設定されていません。 このフラグが設定されていない場合、 **HrValidateIPMSubtree**が、サブツリーのルート フォルダーだけをチェック、削除済みアイテム フォルダー、およびメッセージのルート フォルダーは、検索結果を格納します。 
  
メッセージ ストアを初期化するためにすぐに利用できるように、次のプロパティをメモリに格納します。
  
- **PR_VALID_FOLDER_MASK**([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK**([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
これらのプロパティは、メッセージ ・ ストアの機能を記述するビットマスクです。 **PR_VALID_FOLDER_MASK**では、1 ビットがメッセージ ・ ストアに存在し、有効なエントリが割り当てられている識別子を持つすべての特別なフォルダーの設定があります。 これらのフォルダーおよびそれらのエントリの識別子へのアクセスの詳細については、[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md)を参照してください。 
  
 **PR_STORE_SUPPORT_MASK**では、1 ビットがメッセージ ・ ストアでサポートされているすべての機能の設定があります。 たとえば、メッセージ ・ ストアでは、通知、および書式設定されたテキストをサポートする場合、 **PR_STORE_SUPPORT_MASK**は、STORE_NOTIFY_OK と STORE_RTF_OK のビットを設定があります。 
  
ローカルに格納する必要があるその他のプロパティには、 **PR_VALID_FOLDER_MASK**プロパティを有効なものとして説明するフォルダーのエントリ id が含まれます。 受信トレイ] フォルダー以外のこれらの特別なフォルダーには、それに関連するエントリの識別子プロパティがあります。 たとえば、[送信トレイ] フォルダーのエントリ id は、その**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) のプロパティです。 これらのフォルダーが頻繁に開かれるフォルダーであるためが、エントリ id をすぐに利用することをお勧めします。
  

