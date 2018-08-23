---
title: IOSTX IUnknown
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
ms.openlocfilehash: 7419a0df7a2f3b76caeeb1ca564624d437eddd52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801112"
---
# <a name="iostx--iunknown"></a>IOSTX : IUnknown

  
  
**適用対象**: Outlook 
  
同期メソッドを提供します。 このインターフェイスは、サーバーとローカル ストアに変更をサーバーにローカルでの変更をレプリケートするために必要な情報を取得します。
  
|||
|:-----|:-----|
|提供元:  <br/> |[IPSTX::GetSyncObject](iostx-setsyncresult.md) <br/> |
|インターフェイスの識別子。  <br/> |IID_IOSTX  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[発生しました](iostx-getlasterror.md) <br/> |最後のエラーに関する情報を拡張します。  <br/> |
|[InitSync](iostx-initsync.md) <br/> |同期を開始しようとしていますが、ローカル ストアに通知します。  <br/> |
|[SyncBeg](iostx-syncbeg.md) <br/> |特定の状態の同期をローカル ストアを準備し、複製に必要な情報を取得します。  <br/> |
|[SyncEnd](iostx-syncend.md) <br/> |現在の状態で同期を終了し、その状態を終了します。  <br/> |
|[SyncHdrBeg](iostx-synchdrbeg.md) <br/> |メッセージ ヘッダーの同期を開始します。  <br/> |
|[SyncHdrEnd](iostx-synchdrend.md) <br/> |メッセージ ヘッダーの同期を終了します。  <br/> |
|[SetSyncResult](iostx-setsyncresult.md) <br/> |同期の結果を設定します。  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
   
## <a name="remarks"></a>注釈

クライアントは、アップロードまたはフォルダーとローカル ストア上のフォルダーの内容を同期化、ローカル ストア 1 つの状態からに移動別で[レプリケーションの状態マシン](about-the-replication-state-machine.md)の状態遷移図で示されています。 ローカル ストアを別の 1 つの状態に移動するクライアントのイベントの順序は、次のようにします。
  
1. クライアントでは、レプリケーションを開始しようとしていますが、ローカル ストアに通知するために**IOSTX::InitSync**を呼び出します。 
    
2. 、複製し、複製するオブジェクトの方向によっては、クライアントは、適切な状態のレプリケーションを開始するのには**IOSTX::SyncBeg**を呼び出します。 Outlook は、必要な情報をクライアントに提供し、クライアントがレプリケーションを実行します。 
    
3. クライアントは、複製の結果を得るために**IOSTX::SetSyncResult**を呼び出します。 
    
4. クライアントは、Outlook の以降のレプリケーションに必要な情報を提供する、レプリケーションを終了するのには**IOSTX::SyncEnd**を呼び出します。 
    
具体的には、メッセージ アイテムをダウンロードするとき、クライアントを使用して、 **IOSTX::SyncHdrBeg**と**IOSTX::SyncHdrEnd**ローカル ストア内のメッセージ ヘッダーを持つすべてのメッセージ アイテムを更新します。 
  
1. **IOSTX::SyncHdrBeg**、時に、ローカルは、メッセージ ヘッダーのダウンロードの状態に遷移を保存します。 最初に、outlook は、ローカル ストア内の現在のメッセージのヘッダーを使用して、クライアントを提供します。
    
2. クライアントは、メッセージ ヘッダーとメッセージの項目をダウンロードします。
    
3. Outlook では、完全なメッセージ項目にローカル ストア上の項目を更新します。
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)

