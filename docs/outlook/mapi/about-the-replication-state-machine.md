---
title: レプリケーション状態マシンについて
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9ea18f8e5c7eb758780727829fb1e18d2a19ec92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799611"
---
# <a name="about-the-replication-state-machine"></a>レプリケーション状態マシンについて

  
  
**適用されます**: Outlook 
  
このトピックには、Microsoft Outlook 2013 および Microsoft Outlook 2010 のデータ ・ レプリケーションのステート マシンの概要が含まれています。
  
> [!NOTE]
> やサポートされているに使用するためにこのトピックの説明に従って、レプリケーション API を完全に実装する必要があります。 レプリケーション API は、サーバーとの間に 2013 の Outlook または Outlook 2010 の変更をレプリケートするには、排他的に使用できます。 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX とステート マシン

クライアントは、Outlook 2013 または Outlook 2010 のフォルダーとローカル ストアとサーバ間で項目を同期する順序で**[IOSTX::SyncBeg](iostx-syncbeg.md)**、 **[IOSTX::SyncEnd](iostx-syncend.md)**、 **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**、および**[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** を呼び出します。 呼び出しの実際の手順が異なります (例、2013 の Outlook または Outlook 2010 のフォルダーの階層、Outlook 2013 または Outlook 2010 のフォルダー、メール アイテム、予定表アイテム、およびなど) を複製する必要のあるデータと同期 (かどうかの方向ローカル ストアから、サーバーにアップロードまたはローカル ストアに、サーバーからダウンロード) します。 以下は、典型的な呼び出しシーケンスです。 
  
1. クライアントでは、状態の識別子および対応するデータ構造体のアドレスへのポインターを指定する、レプリケーションを開始するのには**IOSTX::SyncBeg**を呼び出します。 
    
2. 2013 の outlook または Outlook 2010 のデータ構造体、クライアントに必要な情報を持つデータ構造を初期化します。 
    
3. クライアントは、ローカル ストアをレプリケーションに関する必要な情報を伝えるためにデータ構造を更新する、レプリケーションを行います。
    
4. レプリケーションを実行すると、クライアントは、ローカル ストアの特定のレプリケーションの完了を通知するには、 **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** と**IOSTX::SyncEnd**を呼び出します。 
    
> [!NOTE]
> クライアントは、常にクライアントが特定の状態を開始するレプリケーションを終了するのには**IOSTX::SyncEnd**を呼び出します。 によって、全体のデータを同期する必要のあるクライアントは、クライアントが、 **IOSTX::SyncBeg**および**IOSTX::SyncEnd**の呼び出しのペアを 2 回以上呼び出すことがあります。 
  
## <a name="state-table"></a>状態テーブル

> [!NOTE]
> レプリケーション状態機械の状態の対応する識別子とデータ構造体に有効なすべての状態を次の表に一覧します。 **データのレプリケート**] 列で [アイテム] という用語には、メール、予定表、連絡先、メモ、ジャーナル、および作業項目が含まれています。 ローカル ストアからの変更をレプリケートするサーバーに、ときに、上のプレフィックス (たとえば、 **LR_SYNC_UPLOAD_HIERARCHY** 、 **[UPHIER](uphier.md)** ) で状態識別子の [アップロード] を指定してデータ構造体を使用します。 ローカル ストアに、サーバーから変更をレプリケートする、ときに、"DN"のプレフィックス (たとえば、 **LR_SYNC_DOWNLOAD_HIERARCHY** 、 **[DNHIER](dnhier.md)** ) で状態識別子をダウンロードする] を指定してデータ構造体を使用します。 
  
|||||
|:-----|:-----|:-----|:-----|
|**State** <br/> |**レプリケートされたデータ** <br/> |**状態識別子** <br/> |**データ構造体** <br/> |
|[アイドル状態](idle-state.md) <br/> | *None*  <br/> |**LR_SYNC_IDLE** <br/> | *None*  <br/> |
|[状態を同期します。](synchronize-state.md) <br/> |フォルダーまたはアイテム  <br/> |**LR_SYNC** <br/> |**[同期](sync.md)** <br/> |
|[階層の状態をアップロードします。](upload-hierarchy-state.md) <br/> |フォルダー  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[アップロード フォルダーの状態](upload-folder-state.md) <br/> |Folder  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[内容の状態を同期します。](synchronize-contents-state.md) <br/> |アイテム  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[テーブルの状態をアップロードします。](upload-table-state.md) <br/> |アイテム  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[メッセージの状態をアップロードします。](upload-message-state.md) <br/> |Item  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[読み取りステータスをアップロードします。](upload-read-status-state.md) <br/> |アイテム  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[削除ステータスをアップロードします。](upload-delete-status-state.md) <br/> |アイテム  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[階層の状態をダウンロードします。](download-hierarchy-state.md) <br/> |フォルダー  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[テーブルの状態をダウンロードします。](download-table-state.md) <br/> |アイテム  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[メッセージ ヘッダーの状態をダウンロードします。](download-message-header-state.md) <br/> |メッセージのヘッダー  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>状態遷移図

次の図では、アップロードするか、フォルダーまたはフォルダー (メール、予定表、連絡先、メモ、タスク、または仕訳帳の項目) の内容の完全な同期 (アップロード後にダウンロード) を実行するときに発生する状態の遷移を示します。 
  
挿入アートをここでは不足しているに @@@NEED。
  
## <a name="example-uploading-a-folder-hierarchy"></a>アップロードするフォルダー階層の例。

 フォルダーの階層構造をアップロードすると、次の一連の手順が実行されます。 
  
|||||
|:-----|:-----|:-----|:-----|
|**手順** <br/> |**アクション** <br/> |**State** <br/> |**関連するデータ構造体** <br/> |
|1。  <br/> |クライアントは、 **IOSTX::SyncBeg**と階層構造のアップロードを開始します。  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2。  <br/> |2013 の outlook または Outlook 2010 は、クライアントの情報が**UPHIER**に表示されます。 [Out] パラメーターの初期化が含まれます: *iEnt*は、0、およびアップロードする必要がある階層内のフォルダーの数には、*セント*に設定されています。  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3。  <br/> |クライアントには、実際の階層構造のアップロードが行われます。 たとえば、*セント*が、10 個のフォルダーのそれぞれについて、10 の場合、クライアントは**IOSTX::SyncBeg**、適切な状態の識別子およびフォルダーをアップロードするデータ構造体を指定するを呼び出します。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4。  <br/> |2013 の outlook または Outlook 2010 は、フォルダーのアップロード、フォルダー オブジェクトへのポインターの理由と、フォルダーのエントリ ID を含む、[out] パラメーターを初期化することによって**UPFLD**を設定します。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5。  <br/> |クライアントは、指定したフォルダーをアップロードします。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6。  <br/> |クライアントは、ローカル ストアのフォルダーのアップロードの完了を通知: 成功すると、クライアントの設定、[in] パラメーター *ulFlags*を**UPF_OK**、および、 **IOSTX::SetSyncResult (S_OK)** の呼び出しと**UPFLD**と**IOSTX::SyncEnd**. 障害時に、クライアントの場合は、 **UPF_OK**フラグを使って*ulFlags*に未設定。 **IOSTX::SetSyncResult**、 **HRESULT**の値、および**IOSTX::SyncEnd**を渡して呼び出します。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7。  <br/> |**UPF_OK**を設定すると、Outlook 2013 または Outlook 2010 は、フォルダーをアップロードするための内部要求がクリアされます。 *UlFlags*の状態に関係なくをクリーンアップします、内部のブックキーピング情報です。 残っている状態のフォルダーをアップロードするのには階層構造で (*iEnt* 、*セント*よりも小さく)、クライアントと Outlook 2013 または Outlook 2010 は、手順 3 ~ 7 を繰り返します。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8。  <br/> |クライアントは、ローカル ストアの階層構造のアップロードの完了を通知: 成功すると、クライアントの設定、[in] **IOSTX::SetSyncResult (S_OK)** と**IOSTX::SyncEnd**で**UPH_OK**、およびその後の呼び出しでは、 **UPHIER**フラグを設定します。 障害時に、クライアント設定はありません**UPH_OK**のフラグ。 **IOSTX::SetSyncResult**、 **HRESULT**の値、および**IOSTX::SyncEnd**を渡して呼び出します。  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9。  <br/> |**UPH_OK**が設定されている場合は、Outlook 2013 または Outlook 2010 と階層をアップロードするための内部要求がクリアされます。 *UlFlags*の状態に関係なくをクリーンアップします、内部のブックキーピング情報です。  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[同期状態](syncstate.md)

