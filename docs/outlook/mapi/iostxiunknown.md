---
title: IOSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9fd43e4a0e01e774231ddd250a5f20df175f6981
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556337"
---
# <a name="iostx--iunknown"></a>IOSTX : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
同期メソッドを提供します。 このインターフェイスは、サーバーとサーバーの変更をローカル ストアにレプリケートするために必要な情報を取得します。
  
|||
|:-----|:-----|
|提供元:  <br/> |[IPSTX::GetSyncObject](iostx-setsyncresult.md) <br/> |
|インターフェイス識別子:  <br/> |IID_IOSTX  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetLastError](iostx-getlasterror.md) <br/> |最後のエラーに関する拡張情報を取得します。  <br/> |
|[InitSync](iostx-initsync.md) <br/> |同期が始まるとローカル ストアに通知します。  <br/> |
|[SyncBeg](iostx-syncbeg.md) <br/> |特定の状態での同期のためにローカル ストアを準備し、レプリケートに必要な情報を取得します。  <br/> |
|[SyncEnd](iostx-syncend.md) <br/> |現在の状態で同期を終了し、その状態を終了します。  <br/> |
|[SyncHdrBeg](iostx-synchdrbeg.md) <br/> |メッセージ ヘッダーの同期を開始します。  <br/> |
|[SyncHdrEnd](iostx-synchdrend.md) <br/> |メッセージ ヘッダーの同期を終了します。  <br/> |
|[SetSyncResult](iostx-setsyncresult.md) <br/> |同期の結果を設定します。  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
   
## <a name="remarks"></a>注釈

クライアントは、ローカル ストア上のフォルダーとフォルダーの内容をアップロードまたは同期するときに、レプリケーションステート マシンについての状態遷移図に示されている状態から別の状態にローカル ストアを [移動します](about-the-replication-state-machine.md)。 クライアントがローカル ストアをある状態から別の状態に移動するイベントの順序を次に示します。
  
1. クライアントは **IOSTX::InitSync** を呼び出して、レプリケーションが開始されるローカル ストアに通知します。 
    
2. レプリケーションの方向とレプリケートするオブジェクトに応じて、クライアントは **IOSTX::SyncBeg** を呼び出して、適切な状態でレプリケーションを開始します。 Outlook必要な情報をクライアントに提供し、クライアントがレプリケーションを実行します。 
    
3. クライアントは **IOSTX::SetSyncResult** を呼び出して、レプリケーションの結果を返します。 
    
4. クライアントは **IOSTX::SyncEnd** を呼び出してレプリケーションを終了し、Outlookに必要な情報を提供します。 
    
特に、メッセージ アイテムをダウンロードする場合、クライアントは **IOSTX::SyncHdrBeg** と **IOSTX::SyncHdrEnd** を使用して、ローカル ストアのメッセージ ヘッダーを使用して完全なメッセージ アイテムを更新します。 
  
1. **IOSTX::SyncHdrBeg** の場合、ローカル ストアはダウンロード メッセージ ヘッダーの状態に移行します。 Outlook、クライアントにローカル ストアの現在のメッセージ ヘッダーを提供します。
    
2. クライアントは、メッセージ ヘッダーと共に完全なメッセージ アイテムをダウンロードします。
    
3. Outlook完全なメッセージ アイテムを使用してローカル ストアのアイテムを更新します。
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI 定数](mapi-constants.md)

