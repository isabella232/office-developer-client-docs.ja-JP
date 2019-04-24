---
title: iostx IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6d7de4d6c14179ddaba4e2ad907f1acc1c53b125
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317179"
---
# <a name="iostx--iunknown"></a>IOSTX : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
同期方法を提供します。 このインターフェイスでは、ローカルの変更をサーバーにレプリケートするために必要な情報と、ローカルストアに対するサーバーの変更を取得します。
  
|||
|:-----|:-----|
|提供元:  <br/> |[IPSTX::GetSyncObject](iostx-setsyncresult.md) <br/> |
|インターフェイス識別子:  <br/> |IID_IOSTX  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](iostx-getlasterror.md) <br/> |最新のエラーに関する拡張情報を取得します。  <br/> |
|[initsync](iostx-initsync.md) <br/> |同期が開始されることをローカルストアに通知します。  <br/> |
|[SyncBeg](iostx-syncbeg.md) <br/> |特定の状態の同期用にローカルストアを準備し、レプリケートするために必要な情報を取得します。  <br/> |
|[SyncEnd](iostx-syncend.md) <br/> |現在の状態で同期を終了し、その状態を終了します。  <br/> |
|[SyncHdrBeg](iostx-synchdrbeg.md) <br/> |メッセージヘッダーの同期を開始します。  <br/> |
|[SyncHdrEnd](iostx-synchdrend.md) <br/> |メッセージヘッダーの同期を終了します。  <br/> |
|[SetSyncResult](iostx-setsyncresult.md) <br/> |同期の結果を設定します。  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
   
## <a name="remarks"></a>解説

クライアントがローカルストアのフォルダーとフォルダーの内容をアップロードまたは同期すると、[レプリケーションステートマシンについて](about-the-replication-state-machine.md)の状態遷移図に示されているように、ローカルストアをある状態から別の状態に移動します。 クライアントがローカルストアをある状態から別の状態に移動する際のイベントの順序を次に示します。
  
1. クライアントは**iostx:: initsync**を呼び出して、レプリケーションが開始されようとしていることをローカルストアに通知します。 
    
2. レプリケーションの方向とレプリケートするオブジェクトに応じて、クライアントは**iostx:: SyncBeg**を呼び出して、適切な状態でレプリケーションを開始します。 Outlook はクライアントに必要な情報を提供し、クライアントはレプリケーションを実行します。 
    
3. クライアントは**iostx:: SetSyncResult**を呼び出して、レプリケーションの結果を返します。 
    
4. クライアントは**iostx:: syncend**を呼び出してレプリケーションを終了し、次のレプリケーションに必要な情報を Outlook に提供します。 
    
特に、メッセージアイテムをダウンロードする場合、クライアントは**iostx:: SyncHdrBeg**および**iostx:: SyncHdrEnd**を使用して、完全なメッセージアイテムをローカルストアのメッセージヘッダーで更新します。 
  
1. **iostx:: SyncHdrBeg**では、ローカルストアはダウンロードメッセージヘッダーの状態に遷移します。 Outlook では、最初にクライアントに現在のメッセージヘッダーがローカルストアに提供されます。
    
2. クライアントは、メッセージヘッダーと共にメッセージアイテム全体をダウンロードします。
    
3. Outlook は、ローカルストア上のアイテムを完全なメッセージアイテムで更新します。
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI 定数](mapi-constants.md)

