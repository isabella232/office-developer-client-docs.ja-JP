---
title: メッセージ ストア通知の処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d370603dc7cfc015fe7b2757d1cf0525b3092c5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299428"
---
# <a name="handling-message-store-notification"></a>メッセージ ストア通知の処理
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストア通知を登録するには、 [imapisession:: advise](imapisession-advise.md)または[IMsgStore:: advise](imsgstore-advise.md)メソッドを呼び出し、メッセージストア、フォルダー、またはメッセージエントリ識別子を_l tryid_パラメーターの内容に指定します。 メッセージストアプロバイダーは、オブジェクトとテーブルの両方の通知をサポートしています。 特定のメッセージストアオブジェクトを使用して登録するかどうか、これらのオブジェクトを記述するフォルダー階層とコンテンツテーブル、またはオブジェクトとテーブルの両方を使用するかどうかは、表示すると予想される通知、操作を実行するために行う呼び出し、およびメッセージストアプロバイダーが通知をサポートしている。 
  
MAPI では、プロバイダーが通知をサポートする方法に柔軟性があるため、すべてのメッセージストアプロバイダーからの特定のイベントに対する応答で同じ種類の通知を受信することはないことに注意してください。 一部のメッセージストアプロバイダーは、通知をまったくサポートしていません。 使用しているメッセージストアが通知をサポートしているかどうかを確認するには、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティで STORE_NOTIFY_OK ビットを検索します。
  
通知をサポートするメッセージストアプロバイダーの一方の端部には、"リッチ" 通知が生成されるプロバイダーがあります。これらのプロバイダーは、登録されているすべてのアドバイズソースの説明通知を送信します。 もう一方の端には、制限付きの通知をサポートするメッセージストアプロバイダーがあります。これらのプロバイダーは、制限された数のアドバイズソースに関する一般的な通知を送信します。 
  
たとえば、オブジェクトのコピーされた通知とオブジェクトの移動通知の両方を受信するように登録したフォルダーにメッセージをコピーすると、そのオブジェクトのコピーされた通知を受信する場合としない場合があります。 受信したかどうかは、以下によって決まります。
  
- コピーを実行するために呼び出したメソッド。 [imapifolder:: copymessages](imapifolder-copymessages.md)、 [imapifolder:: CopyTo](imapiprop-copyto.md)、 [imapifolder:: copymessages](imapiprop-copyprops.md)の場合があります。
    
- メッセージストアプロバイダーが copy メソッドを実装する方法。
    
- メッセージストアプロバイダーがフォルダーにコピーされたオブジェクトの通知をサポートしているかどうか。
    
メッセージストアプロバイダーのイベント通知を実装する方法を説明する厳密なガイドラインはないため、クライアントは一貫した動作を期待できません。 MAPI では、メッセージストアプロバイダーがイベント通知を実装する方法について、次の表で推奨事項の概要を説明します。 表を次のように読み取ります。最初の列で操作を実行すると、3番目の列にリストされているオブジェクトでその型に対して登録されている場合は、2番目の列にリストされている型の通知を受信することを期待します。 たとえば、フォルダーを作成した後、メッセージストアで_fnevObjectCreated_通知を登録している場合にのみ、 _fnevObjectCreated_通知が表示されます。 
  
|**操作名**|**イベントの種類**|**アドバイズソース**|
|:-----|:-----|:-----|
|フォルダーを作成する  <br/> | _fnevObjectCreated_ <br/> |メッセージストア  <br/> |
|フォルダーを削除する  <br/> | _fnevObjectDeleted_ <br/> |メッセージストアの削除されたフォルダー  <br/> |
|フォルダーをあるフォルダーから別のフォルダーに移動する  <br/> | _fnevObjectMoved_ <br/> |移動されたメッセージストアフォルダー  <br/> |
|フォルダーをあるフォルダーから別のフォルダーにコピーする  <br/> | _fnevObjectCopied_ <br/> |メッセージストアとコピーフォルダー (フォルダーの新しいコピーに対して_fnevObjectCreated_通知は送信されません)  <br/> |
|計算されたフォルダーのプロパティを変更する (**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))、 **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))、 **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> | _fnevObjectModified_ <br/> |メッセージストアの変更されたフォルダー (親フォルダーへの通知なし)  <br/> |
|メッセージを作成する  <br/> | _fnevObjectCreated_ <br/> |メッセージストア  <br/> |
|メッセージを削除して、親フォルダーの**PR_CONTENT_COUNT**プロパティの変更を発生させる  <br/> | _fnevObjectDeleted_ <br/> |メッセージストアが削除されたメッセージ  <br/> |
|あるフォルダーから別のフォルダーにメッセージを移動する  <br/> | _fnevObjectMoved_ <br/> |メッセージストアの移動メッセージ  <br/> |
|あるフォルダーから別のフォルダーにメッセージをコピーする  <br/> | _fnevObjectCopied_ <br/> |メッセージストアでコピーされたメッセージ (メッセージの新しいコピーに対する_fnevObjectCreated_通知なし)  <br/> |
|メッセージを保存し、親フォルダーの**PR_CONTENT_COUNT**プロパティが変更されたことを引き起こします。  <br/> | _fnevObjectCreated_ <br/> |最初に保存するときのみメッセージストア  <br/> |
|メッセージを保存する  <br/> | _fnevObjectModified_ <br/> |最初の保存変更メッセージの後に保存されるメッセージストア (親フォルダーへの通知なし)  <br/> |
|検索操作を完了する  <br/> | _fnevSearchComplete_ <br/> |メッセージストアの検索フォルダー  <br/> |
|新しいメッセージ  <br/> | _fnevNewMail_ <br/> |メッセージストア  <br/> |
   
> [!NOTE]
> オブジェクトが変更された通知を受信した場合は、 **onnotify**呼び出しの lpnotifications パラメーターが指す__ [OBJECT_NOTIFICATION](object_notification.md)構造のプロパティタグ配列部分が NULL であるか、または NULL でないことに注意してください。 メッセージストアプロバイダーは、この配列にプロパティ情報を挿入する必要はありません。 **onnotify**メソッドで、 _lpPropTagArray_ポインターが NULL の場合を処理できることを確認してください。 
  
多くの場合、すべてのオブジェクト通知ではない場合、影響を受けるフォルダーの表示を更新します。
  

