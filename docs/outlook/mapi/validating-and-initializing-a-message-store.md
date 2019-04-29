---
title: メッセージストアの検証と初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 77b3f707fc36a868de5acd7c7ba4642a1da4e3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433690"
---
# <a name="validating-and-initializing-a-message-store"></a>メッセージストアの検証と初期化

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MDB_NO_MAIL フラグを設定せずに[imapisession:: openmsgstore](imapisession-openmsgstore.md)メソッドを使用してメッセージストアを開くと、MAPI によって複数のフォルダーが作成され、それらに既定の名前と役割が割り当てられます。 MAPI は、クライアントまたはメッセージストアプロバイダーのいずれかが作成を担当した場合に必然的に発生する非互換性を回避するために、これらのフォルダーを作成する責任があります。 
  
適切なフォルダーが作成され、それらが有効であることを確認する必要がある場合があります。 このためには、 [hrvalidateipmsubtree](hrvalidateipmsubtree.md)関数を使用できます。 既定のメッセージストアを検証する場合は、MAPI_FULL_IPM_TREE フラグを渡します。 既定のメッセージストア用に、より広範なフォルダーのグループが作成されます。 **hrvalidateipmsubtree**が MAPI_FULL_IPM_TREE フラグを受け取ると、次のフォルダーがあるかどうかがチェックされます。 
  
- IPM サブツリーのルートフォルダー
    
- IPM ルートフォルダーの削除済みアイテムフォルダー
    
- IPM ルートフォルダーの受信トレイフォルダー
    
- IPM ルートフォルダーの送信トレイフォルダー
    
- [送信済みアイテム] フォルダー (IPM ルートフォルダー内)
    
- メッセージストアのルートフォルダー内のフォルダービュー
    
- メッセージストアのルートフォルダー内の共通ビュー
    
- メッセージストアのルートフォルダー内の検索フォルダー
    
メッセージストアが既定ではない場合は、MAPI_FULL_IPM_TREE フラグを設定するかどうかを設定できます。 このフラグが設定されていない場合、 **hrvalidateipmsubtree**はサブツリーのルートフォルダー、削除済みアイテムフォルダー、およびメッセージストア検索結果のルートフォルダーだけをチェックします。 
  
メッセージストアを初期化するには、次のプロパティをメモリに格納して、簡単に使用できるようにします。
  
- **PR_VALID_FOLDER_MASK**([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK**([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
これらのプロパティは、メッセージストアの機能を記述するビットマスクです。 **PR_VALID_FOLDER_MASK**には、メッセージストアに存在し、有効なエントリ識別子が割り当てられているすべての特別なフォルダーに対して1ビットが設定されています。 これらのフォルダーおよびそのエントリ識別子へのアクセスの詳細については、「[メッセージストアフォルダーを開く](opening-a-message-store-folder.md)」を参照してください。 
  
 **PR_STORE_SUPPORT_MASK**には、メッセージストアでサポートされているすべての機能に対して1ビットが設定されています。 たとえば、メッセージストアが通知と書式設定されたテキストをサポートしている場合、その**PR_STORE_SUPPORT_MASK**には STORE_NOTIFY_OK と STORE_RTF_OK のビットが設定されます。 
  
ローカルに格納する必要があるその他のプロパティには、 **PR_VALID_FOLDER_MASK**プロパティが有効として記述するフォルダーのエントリ識別子があります。 受信トレイフォルダー以外の各特別なフォルダーには、エントリ識別子プロパティが関連付けられています。 たとえば、送信トレイフォルダーのエントリ識別子は、 **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) プロパティです。 これらのフォルダーは頻繁に開かれるフォルダーなので、エントリ識別子をすぐに使用できるようにすることをお勧めします。
  

