---
title: レプリケーション状態のマシンについて
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c0f0f61c53fa868bfabd29cdb3cfaf278bcd846d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564485"
---
# <a name="about-the-replication-state-machine"></a>レプリケーション状態のマシンについて

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、データレプリケーションを実行および管理するMicrosoft Outlook 2013のMicrosoft Outlook 2010について説明します。
  
> [!NOTE]
> レプリケーション API は、有用またはサポートするために、このトピックの指示に従って完全に実装する必要があります。 レプリケーション API は、2013 年または 2010 年Outlook 2010 年Outlookサーバー間の変更をレプリケートするために排他的に使用できます。 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX とステート マシン

クライアントは、IOSTX::SyncBeg、IOSTX:::SyncEnd、IOSTX::SyncHdrBeg、**[および IOSTX::SyncHdrEnd](iostx-synchdrend.md)** をシーケンスで呼び出して、Outlook 2013 または Outlook 2010 のフォルダーとアイテムをローカル ストアとサーバー間で同期します。 **[](iostx-syncbeg.md)** **[](iostx-syncend.md)** **[](iostx-synchdrbeg.md)** 実際の呼び出しの順序は、レプリケートする必要があるデータ (たとえば、Outlook 2013 または Outlook 2010 フォルダーの階層、Outlook 2013 または Outlook 2010 フォルダー、メール アイテム、予定表アイテムなど) と同期の方向 (ローカル ストアからサーバーへのアップロード、またはサーバーからローカル ストアへのダウンロードなど) によって異なります。 一般的な呼び出しのシーケンスを次に示します。 
  
1. クライアントは **IOSTX::SyncBeg** を呼び出してレプリケーションを開始し、状態識別子と対応するデータ構造のアドレスへのポインターを指定します。 
    
2. Outlook 2013 または Outlook 2010 は、データ構造を割り当て、クライアントに必要な情報を使用してデータ構造を初期化します。 
    
3. クライアントはレプリケーションを実行し、データ構造を更新して、レプリケーションに関する必要な情報をローカル ストアに伝える。
    
4. レプリケーションを実行した後、クライアントは **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** と **IOSTX::SyncEnd** を呼び出して、特定のレプリケーションの完了をローカル ストアに通知します。 
    
> [!NOTE]
> クライアントは常に **IOSTX::SyncEnd** を呼び出して、クライアントが特定の状態で開始したレプリケーションを終了します。 クライアントが同期する必要がある全体的なデータに応じて、クライアントは **IOSTX::SyncBeg** と **IOSTX::SyncEnd** の 2 つの呼び出しを 2 回以上呼び出す場合があります。 
  
## <a name="state-table"></a>状態テーブル

> [!NOTE]
> 次の表に、レプリケーションステート マシンのすべての有効な状態と、対応する状態識別子とデータ構造を示します。 [ **データレプリケート] 列の** 用語 "items" には、メール、予定表、連絡先、メモ、ジャーナル、およびタスク アイテムが含まれます。 ローカル ストアからサーバーに変更をレプリケートする場合は、"UPLOAD" を指定する状態識別子と、"UP" プレフィックスを持つデータ構造 (LR_SYNC_UPLOAD_HIERARCHY や **[UPHIER](uphier.md)** など)**を** 使用します。 サーバーからローカル ストアに変更をレプリケートする場合は、"DOWNLOAD" を指定する状態識別子と、"DN" プレフィックスを持つデータ構造 (LR_SYNC_DOWNLOAD_HIERARCHY や **[DNHIER](dnhier.md)** など)**を** 使用します。 
  
|||||
|:-----|:-----|:-----|:-----|
|**State** <br/> |**レプリケートされるデータ** <br/> |**状態識別子** <br/> |**データ構造** <br/> |
|[アイドル状態](idle-state.md) <br/> | *なし*  <br/> |**LR_SYNC_IDLE** <br/> | *なし*  <br/> |
|[同期状態](synchronize-state.md) <br/> |フォルダーまたはアイテム  <br/> |**LR_SYNC** <br/> |**[SYNC](sync.md)** <br/> |
|[アップロード階層の状態](upload-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[アップロードの状態](upload-folder-state.md) <br/> |フォルダー  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[コンテンツの状態を同期する](synchronize-contents-state.md) <br/> |アイテム  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[アップロード状態](upload-table-state.md) <br/> |アイテム  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[アップロード状態](upload-message-state.md) <br/> |アイテム  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[アップロード状態を読み取る](upload-read-status-state.md) <br/> |アイテム  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[アップロード状態の削除](upload-delete-status-state.md) <br/> |アイテム  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[階層状態のダウンロード](download-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[テーブルの状態をダウンロードする](download-table-state.md) <br/> |アイテム  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[メッセージ ヘッダーの状態をダウンロードする](download-message-header-state.md) <br/> |メッセージ ヘッダー  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>状態遷移図

次の図は、フォルダーまたはフォルダーの内容 (メール、予定表、連絡先、メモ、タスク、またはジャーナル アイテム) の完全同期 (ダウンロード後にアップロード) をアップロードまたは実行するときに発生する状態遷移を示しています。 
  
@@@@@NEED欠けているアートをここに挿入する方法@@@@@@
  
## <a name="example-uploading-a-folder-hierarchy"></a>例: フォルダー階層のアップロード

 フォルダーの階層をアップロードする場合、次の一連の手順が実行されます。 
  
|||||
|:-----|:-----|:-----|:-----|
|**手順** <br/> |**操作** <br/> |**State** <br/> |**関連するデータ構造** <br/> |
|1.  <br/> |クライアントは **、IOSTX::SyncBeg を使用して階層アップロードを開始します**。  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2.  <br/> |Outlook 2013 または Outlook 2010 は **、UPHIER** にクライアントの情報を設定します。 これには、[out] パラメーターの初期化が含まれます  *。iEnt*  は 0 に設定され  *、cEnt*  はアップロードが必要な階層内のフォルダーの数に設定されます。  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3。  <br/> |クライアントは、実際の階層アップロードを実行します。 たとえば  *、cEnt*  が 10 の場合、10 フォルダーごとに、クライアントは **IOSTX::SyncBeg** を呼び出し、フォルダーをアップロードする適切な状態識別子とデータ構造を指定します。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4.  <br/> |Outlook 2013 または Outlook 2010 は、フォルダーのアップロード理由、フォルダー オブジェクトへのポインター、フォルダーのエントリ ID など、その [out] パラメーターを初期化することで **UPFLD** を設定します。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5.  <br/> |クライアントは、指定したフォルダーをアップロードします。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6.  <br/> |クライアントは、フォルダーアップロードの完了をローカル ストアに通知します。成功すると、クライアントは **upFLD** の **[in]** パラメーター *ulFlags* を UPF_OK で設定し **、IOSTX::SetSyncResult (S_OK)** と **IOSTX::SyncEnd** を呼び出します。 失敗した場合、クライアントは  *ulFlags*  にフラグを **設定UPF_OKできません** 。 **IOSTX::SetSyncResult** を呼び出し **、HRESULT** 値を渡し **、IOSTX::SyncEnd を渡します**。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7.  <br/> |この **UPF_OK** 設定されている場合、Outlook 2013 または Outlook 2010 は、フォルダーのアップロードに関する内部要求をクリアします。 その後  *、ulFlags*  の状態に関係なく、内部の簿記情報がクリーンアップされます。 階層内にアップロードするフォルダー *(iEnt* はまだ *cEnt* より小さい) が残っている間、クライアントと Outlook 2013 または Outlook 2010 は手順 3 ~ 7 を繰り返します。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8.  <br/> |クライアントは、階層アップロードの完了をローカル ストアに通知します。成功すると、クライアントは **UPHIER** で **[in]** フラグを UPH_OK で設定し **、IOSTX::SetSyncResult (S_OK)** と **IOSTX::SyncEnd** を呼び出します。 エラーが発生した場合、クライアントはメッセージ **フラグUPH_OKできません** 。 **IOSTX::SetSyncResult** を呼び出し **、HRESULT** 値を渡し **、IOSTX::SyncEnd を渡します**。  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9.  <br/> |この **UPH_OK** 設定されている場合、Outlook 2013 または Outlook 2010 は階層のアップロードに関する内部要求をクリアします。 その後  *、ulFlags*  の状態に関係なく、内部の簿記情報がクリーンアップされます。  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[SYNCSTATE](syncstate.md)

