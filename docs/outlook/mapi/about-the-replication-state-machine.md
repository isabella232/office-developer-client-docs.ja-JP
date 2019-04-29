---
title: レプリケーション状態のマシンについて
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a0644e4bf5c6847d61cc59e203d50f61ad142e84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416483"
---
# <a name="about-the-replication-state-machine"></a>レプリケーション状態のマシンについて

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、microsoft outlook 2013 および microsoft outlook 2010 データレプリケーションの状態機械の概要について説明します。
  
> [!NOTE]
> このトピックの手順に従ってレプリケーション API が完全に実装されている必要があります。 レプリケーション API は、outlook 2013 または outlook 2010 の変更をサーバーにレプリケートする場合にのみ使用できます。 
  
## <a name="iostx-and-the-state-machine"></a>iostx およびステートマシン

クライアントは、 **[iostx:: SyncBeg](iostx-syncbeg.md)**、iostx:: **[syncend](iostx-syncend.md)**、iostx: **[: SyncHdrBeg](iostx-synchdrbeg.md)**、 **[iostx:: SyncHdrEnd](iostx-synchdrend.md)** を呼び出して、ローカルストアとサーバーの間で outlook 2013 または outlook 2010 フォルダーとアイテムを同期します。 実際の呼び出しの順序は、レプリケートする必要のあるデータ (たとえば、outlook 2013 または outlook 2010 フォルダーの階層、outlook 2013 または outlook 2010 フォルダー、メールアイテム、予定表アイテムなど)、および同期の方向 (かどうか) によって異なります。ローカルストアからサーバーへのアップロード、またはサーバーからローカルストアへのダウンロード)。 一般的な一連の呼び出しの例を次に示します。 
  
1. クライアントは**iostx:: SyncBeg**を呼び出してレプリケーションを開始し、状態識別子と、対応するデータ構造のアドレスへのポインターを指定します。 
    
2. outlook 2013 または outlook 2010 は、データ構造を割り当て、クライアントに必要な情報を使用してデータ構造を初期化します。 
    
3. クライアントはレプリケーションを実行し、データ構造を更新して、レプリケーションに関する必要な情報をローカルストアに伝達します。
    
4. レプリケーションの実行後、クライアントは**[iostx:: SetSyncResult](iostx-setsyncresult.md)** と**iostx:: syncend**を呼び出して、特定のレプリケーションが完了したことをローカルストアに通知します。 
    
> [!NOTE]
> クライアントは、常に**iostx:: syncend**を呼び出して、クライアントが特定の状態で開始したレプリケーションを終了します。 クライアントは、クライアントが同期する必要のある全体的なデータに応じて、 **iostx:: SyncBeg**と**iostx:: syncend**を複数回呼び出すことができます。 
  
## <a name="state-table"></a>状態テーブル

> [!NOTE]
> 次の表に、レプリケーション状態マシンのすべての有効な状態と、それに対応する状態識別子とデータ構造を示します。 [レプリケートされた**データ**] 列の "アイテム" という用語には、メール、予定表、連絡先、メモ、履歴、およびタスクアイテムが含まれます。 ローカルストアからサーバーに変更をレプリケートする場合は、「アップロード」を指定した状態識別子と「up」プレフィックスを指定したデータ構造 (たとえば、 **LR_SYNC_UPLOAD_HIERARCHY**および**[uphier](uphier.md)** ) を使用します。 サーバーからローカルストアに変更をレプリケートする場合は、"DN" プレフィックスを指定した "DOWNLOAD" とデータ構造を指定する状態識別子を使用します (たとえば、 **LR_SYNC_DOWNLOAD_HIERARCHY**や**[dnhier](dnhier.md)** )。 
  
|||||
|:-----|:-----|:-----|:-----|
|**State** <br/> |**レプリケートされるデータ** <br/> |**状態識別子** <br/> |**データ構造** <br/> |
|[アイドル状態](idle-state.md) <br/> | *None*  <br/> |**LR_SYNC_IDLE** <br/> | *None*  <br/> |
|[同期状態](synchronize-state.md) <br/> |フォルダーまたはアイテム  <br/> |**LR_SYNC** <br/> |**[SYNC](sync.md)** <br/> |
|[階層のアップロード状態](upload-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[フォルダーの状態をアップロードする](upload-folder-state.md) <br/> |フォルダー  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[コンテンツの状態の同期](synchronize-contents-state.md) <br/> |アイテム  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[テーブルの状態をアップロードする](upload-table-state.md) <br/> |アイテム  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[メッセージアップロードの状態](upload-message-state.md) <br/> |アイテム  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[読み取り状態のアップロードの状態](upload-read-status-state.md) <br/> |アイテム  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[削除の状態の状態をアップロードする](upload-delete-status-state.md) <br/> |アイテム  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[階層のダウンロード状態](download-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[テーブルの状態をダウンロードする](download-table-state.md) <br/> |アイテム  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[メッセージヘッダーの状態をダウンロードする](download-message-header-state.md) <br/> |メッセージ ヘッダー  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>状態遷移図

次の図は、フォルダーまたはフォルダーの内容 (メール、予定表、連絡先、メモ、タスク、またはジャーナルアイテム) の完全同期 (ダウンロード後にアップロード) をアップロードまたは実行する際に発生する状態の移行を示しています。 
  
@ @ @ @ @ @ がない場合に、@ @ @ @ @NEED してアートを挿入する
  
## <a name="example-uploading-a-folder-hierarchy"></a>例: フォルダー階層のアップロード

 フォルダーの階層をアップロードする場合は、次の手順を実行します。 
  
|||||
|:-----|:-----|:-----|:-----|
|**手順** <br/> |**操作** <br/> |**State** <br/> |**関連データ構造** <br/> |
|1.  <br/> |クライアントは**iostx:: SyncBeg**で階層のアップロードを開始します。  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2.  <br/> |outlook 2013 または outlook 2010 は、 **uphier**にクライアントの情報を設定します。 これには、[out] パラメーターの初期化が含まれます。 *ient*は0に設定され、アップロードする必要がある階層内のフォルダー数になります。 **  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3.  <br/> |クライアントは、実際の階層をアップロードします。 たとえば、*セント*が10の場合、クライアントは**iostx:: SyncBeg**を呼び出して、フォルダーをアップロードするための適切な状態識別子とデータ構造を指定します。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4.  <br/> |outlook 2013 または outlook 2010 は、フォルダーのアップロードの理由、folder オブジェクトへのポインター、フォルダーのエントリ ID など、[out] パラメーターを初期化することによって**UPFLD**に設定します。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5.  <br/> |クライアントは指定されたフォルダーをアップロードします。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6.  <br/> |クライアントは、フォルダーアップロードの完了をローカルストアに通知します。成功した場合、クライアントは**UPFLD**の [in] パラメーター *ulflags*を**UPF_OK**に設定し、 **iostx:: SetSyncResult (S_OK)** および**iostx:: syncend を呼び出します。**. エラーが発生した場合、クライアントは**UPF_OK**フラグを持つ*ulflags*を設定しません。 **iostx:: SetSyncResult**を呼び出し、 **HRESULT**値を渡して、および**iostx:: syncend**を呼び出します。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7.  <br/> |**UPF_OK**が設定されている場合、outlook 2013 または outlook 2010 は、フォルダーをアップロードするための内部要求をクリアします。 *ulflags*の状態に関係なく、すべての内部ブック情報がクリーンアップされます。 アップロードする階層にフォルダーがまだ存在してい** ますが、クライアントと outlook ** 2013 または outlook 2010 は、手順3から7を繰り返します。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8.  <br/> |クライアントは、階層アップロードの完了をローカルストアに通知します。成功した場合、クライアントは**uphier**で**UPH_OK**を使用して [in] フラグを設定し、 **iostx::: SetSyncResult (S_OK)** と**iostx:: syncend**を呼び出します。 エラー発生時に、クライアントは**UPH_OK**フラグを設定しません。 **iostx:: SetSyncResult**を呼び出し、 **HRESULT**値を渡して、および**iostx:: syncend**を呼び出します。  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9.  <br/> |**UPH_OK**が設定されている場合、outlook 2013 または outlook 2010 は、階層をアップロードするための内部要求をクリアします。 *ulflags*の状態に関係なく、すべての内部ブック情報がクリーンアップされます。  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[SYNCSTATE](syncstate.md)

