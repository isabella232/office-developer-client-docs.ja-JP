---
title: メッセージ ストア通知の処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d370603dc7cfc015fe7b2757d1cf0525b3092c5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428026"
---
# <a name="handling-message-store-notification"></a>メッセージ ストア通知の処理
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア通知に登録するには [、IMAPISession:::Advise](imapisession-advise.md) メソッドまたは [IMsgStore::Advise](imsgstore-advise.md) メソッドを呼び出し  _、lpEntryID_ パラメーターの内容にメッセージ ストア、フォルダー、またはメッセージ エントリ識別子を指定します。 メッセージ ストア プロバイダーは、オブジェクト通知とテーブル通知の両方をサポートします。 特定のメッセージ ストア オブジェクトに登録するか、これらのオブジェクトを記述するフォルダー階層テーブルとコンテンツ テーブルを使用するか、オブジェクトとテーブルの両方に登録するかは、表示される通知、操作を実行するために行う呼び出し、およびメッセージ ストア プロバイダーが通知をサポートする方法によって異なります。 
  
MAPI を使用すると、プロバイダーが通知をサポートする方法が柔軟に行えるので、すべてのメッセージ ストア プロバイダーから特定のイベントに応答して、常に同じ種類の通知を受け取るとは限りないので注意してください。 一部のメッセージ ストア プロバイダーは、通知を全くサポートしていない。 使用しているメッセージ ストアが通知をサポートしているかどうかを確認するには、STORE_NOTIFY_OK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティで PR_STORE_SUPPORT_MASK ビットを探します。
  
通知をサポートするメッセージ ストア プロバイダーの一端には、"リッチ" 通知を生成するプロバイダーがあります。これらのプロバイダーは、登録済みのすべてのアドバイス ソースに対して説明的な通知を送信します。 もう一方の端には、制限付き通知をサポートするメッセージ ストア プロバイダーがあります。これらのプロバイダーは、制限された数のアドバイス ソースに対して一般的な通知を送信します。 
  
たとえば、コピーされたオブジェクトと移動したオブジェクトの両方の通知を受信するために登録したフォルダーにメッセージをコピーする場合、オブジェクトコピーされた通知を受信する場合と受信しない場合があります。 受け取るかどうかは、次に依存します。
  
- コピーを実行するために呼び出したメソッド。 これは[IMAPIFolder::CopyMessages](imapifolder-copymessages.md) [、IMAPIProp::CopyTo、](imapiprop-copyto.md)[または IMAPIProp::CopyProps です](imapiprop-copyprops.md)。
    
- メッセージ ストア プロバイダーが copy メソッドを実装する方法。
    
- メッセージ ストア プロバイダーがフォルダー上のオブジェクト コピーされた通知をサポートするかどうか。
    
メッセージ ストア プロバイダーのイベント通知を実装する方法を説明する厳密なガイドラインはないので、クライアントは一貫した動作を期待できません。 MAPI では、メッセージ ストア プロバイダーがイベント通知を実装する方法について推奨事項を示し、次の表でこれらの推奨事項の概要を示します。 次のように表を読み取ります。最初の列で操作を実行した後、3 番目の列にリストされているオブジェクトをその型に登録している場合は、2 番目の列にリストされている型の通知を受け取る必要があります。 たとえば、フォルダーを作成した後、メッセージ ストアで  _fnevObjectCreated_ 通知に登録している場合にのみ  _、fnevObjectCreated_ 通知を受け取ります。 
  
|**操作**|**イベントの種類**|**ソースのアドバイス**|
|:-----|:-----|:-----|
|フォルダーの作成  <br/> | _fnevObjectCreated_ <br/> |メッセージ ストア  <br/> |
|フォルダーの削除  <br/> | _fnevObjectDeleted_ <br/> |メッセージ ストア 削除済みフォルダー  <br/> |
|フォルダーをあるフォルダーから別のフォルダーに移動する  <br/> | _fnevObjectMoved_ <br/> |メッセージ ストア移動フォルダー  <br/> |
|フォルダーを 1 つのフォルダーから別のフォルダーにコピーする  <br/> | _fnevObjectCopied_ <br/> |メッセージ ストアとコピーされたフォルダー (フォルダーの新しいコピーに対して送信された  _fnevObjectCreated_ 通知なし)  <br/> |
|計算フォルダー プロパティの変更 (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)) 、 **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) 、 **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |メッセージ ストア 変更されたフォルダー (親フォルダーへの通知なし)  <br/> |
|メッセージを作成する  <br/> | _fnevObjectCreated_ <br/> |メッセージ ストア  <br/> |
|メッセージを削除し、親フォルダーのプロパティ **を変更PR_CONTENT_COUNT** する  <br/> | _fnevObjectDeleted_ <br/> |メッセージ ストア 削除済みメッセージ  <br/> |
|あるフォルダーから別のフォルダーにメッセージを移動する  <br/> | _fnevObjectMoved_ <br/> |メッセージ ストア 移動されたメッセージ  <br/> |
|あるフォルダーから別のフォルダーにメッセージをコピーする  <br/> | _fnevObjectCopied_ <br/> |メッセージ ストア コピーされたメッセージ (メッセージの新しいコピーに対する  _fnevObjectCreated_ 通知なし)  <br/> |
|メッセージを保存し、親フォルダーのプロパティ **に変更を** PR_CONTENT_COUNTする  <br/> | _fnevObjectCreated_ <br/> |最初の保存時のメッセージ ストアのみ  <br/> |
|メッセージを保存する  <br/> | _fnevObjectModified_ <br/> |最初の保存後の保存時のメッセージ ストア変更メッセージ (親フォルダーへの通知なし)  <br/> |
|検索操作を完了する  <br/> | _fnevSearchComplete_ <br/> |メッセージ ストアの検索フォルダー  <br/> |
|新しいメッセージ  <br/> | _fnevNewMail_ <br/> |メッセージ ストア  <br/> |
   
> [!NOTE]
> オブジェクト変更通知を受け取った場合は **、OnNotify** 呼び出しの _lpNotifications_ パラメーターが指す [OBJECT_NOTIFICATION](object_notification.md)構造体のプロパティ タグ配列部分が NULL の場合としない場合があります。 メッセージ ストア プロバイダーは、この配列にプロパティ情報を挿入する必要はありません。 **OnNotify メソッドが** _lpPropTagArray_ ポインターが NULL の場合に対応することを確認します。 
  
ほとんどの場合、すべてのオブジェクト通知ではない場合は、影響を受けるフォルダーまたはフォルダーのビューを更新します。
  

