---
title: メッセージ ストアの通知を処理します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e0cc2f9-a88d-4cec-bef5-b60f2ec80f1c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 898f8b6ff3d0b0dd42a670596b54171f18b4a5e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800187"
---
# <a name="handling-message-store-notification"></a>メッセージ ストアの通知を処理します。
  
**適用対象**: Outlook 
  
メッセージ ストアの通知を登録するに[IMAPISession::Advise](imapisession-advise.md)または[IMsgStore::Advise](imsgstore-advise.md)のいずれかのメソッドを呼び出すし、 _lpEntryID_パラメーターの内容のメッセージ ・ ストア、フォルダー、またはメッセージのエントリ id を指定します。 メッセージ ストア プロバイダーは、オブジェクトと表の両方の通知をサポートします。 方法および特定のメッセージ ストアのオブジェクトと、これらのオブジェクトを表すフォルダーの階層と内容のテーブルまたは両方のオブジェクトを登録して、テーブルは、表示、操作を実行する呼び出しの通知に依存するかどうかメッセージ ストア プロバイダーは、通知をサポートしています。 
  
MAPI プロバイダーが通知をサポートする方法に柔軟性が許可されているため、常に表示されませんと同じ種類の通知のすべてのメッセージ ストア プロバイダーから特定のイベントに応答してあります。 メッセージ ストア プロバイダーの中では、通知をすべてのサポートの操作を行います。 メッセージ ・ ストアを使用するかどうかを決定するには、通知、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティに STORE_NOTIFY_OK ビットのファイルの場所をサポートしています。
  
メッセージ ・ ストアのスペクトルの一方の端にある通知をサポートするプロバイダーは、「リッチ」通知を生成するプロバイダーです。これらのプロバイダーは、登録されているすべての通知をわかりやすいソースの通知を送信します。 他の最後にはメッセージ ストア プロバイダー制限通知をサポートします。これらのプロバイダーは、一般的なアドバイスのソース数が制限されている通知を送信します。 
  
などのメッセージをフォルダーにコピーする場合は、両方のオブジェクトのコピーを受信する登録すると通知、オブジェクトに移動、するか、コピーされるオブジェクトの通知を受け取らないことがあります。 受信するかどうかによって異なります。
  
- このメソッドは、コピーを実行すると呼ばれます。 [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)、 [IMAPIProp::CopyTo](imapiprop-copyto.md)、または[IMAPIProp::CopyProps](imapiprop-copyprops.md)可能性があります。
    
- 方法、メッセージ ・ ストア プロバイダーの実装、copy メソッドです。
    
- かどうか、メッセージ ストア プロバイダーでは、フォルダーにコピーするオブジェクトの通知をサポートしています。
    
ストア プロバイダーにメッセージに関するイベント通知を実装する方法について説明する厳密なガイドラインはありませんがある、ためクライアントが一貫性のある動作を求めることはできません。 MAPI は、これらの推奨事項、プロバイダー実装のイベント通知と次の表にメッセージを格納する方法に関する推奨事項をことがあります。 テーブルを次のように読み取り: 3 番目の列に記載されているオブジェクトにその型を登録した場合に、2 番目の列に記載されている種類の通知を受信することが最初の列の操作を実行した後。 たとえば、フォルダーを作成した後のメッセージ ・ ストアの_fnevObjectCreated_の通知を登録する場合にのみ、 _fnevObjectCreated_の通知が表示されます。 
  
|**Operation**|**イベントの種類**|**ソースをアドバイスします。**|
|:-----|:-----|:-----|
|フォルダーの作成  <br/> | _fnevObjectCreated_ <br/> |メッセージ ・ ストア  <br/> |
|フォルダーの削除  <br/> | _fnevObjectDeleted_ <br/> |メッセージ ストアの削除済みフォルダー  <br/> |
|1 つのフォルダーから別のフォルダーを移動します。  <br/> | _fnevObjectMoved_ <br/> |メッセージ ストアのフォルダーの移動  <br/> |
|1 つのフォルダーから別のフォルダーをコピーします。  <br/> | _fnevObjectCopied_ <br/> |メッセージを格納し、( _fnevObjectCreated_通知は、フォルダーの新しいコピーを送信)] フォルダーをコピー  <br/> |
|(**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md)) **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))、 **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) は、計算済みのフォルダー プロパティの変更します。  <br/> | _fnevObjectModified_ <br/> |ストアの変更されたフォルダー (親フォルダーに通知がない)  <br/> |
|メッセージを作成する  <br/> | _fnevObjectCreated_ <br/> |メッセージ ・ ストア  <br/> |
|変更されて、親フォルダーの**PR_CONTENT_COUNT**プロパティ、メッセージを削除します。  <br/> | _fnevObjectDeleted_ <br/> |削除済みメッセージのメッセージ ストア  <br/> |
|1 つのフォルダーからメッセージを移動します。  <br/> | _fnevObjectMoved_ <br/> |メッセージが移動されたメッセージを保存します。  <br/> |
|1 つのフォルダーからメッセージをコピーします。  <br/> | _fnevObjectCopied_ <br/> |メッセージのストア コピー メッセージ (ない_fnevObjectCreated_のコピーを新しいメッセージの通知)  <br/> |
|変更されて、親フォルダーの**PR_CONTENT_COUNT**プロパティ、メッセージを保存します。  <br/> | _fnevObjectCreated_ <br/> |最初の保存のみにメッセージ ・ ストア  <br/> |
|メッセージを保存します。  <br/> | _fnevObjectModified_ <br/> |最初の変更されたメッセージ (親フォルダーに通知がない) を保存した後の保存にメッセージ ・ ストア  <br/> |
|検索操作を完了します。  <br/> | _fnevSearchComplete_ <br/> |ストアの検索フォルダー  <br/> |
|新しいメッセージ  <br/> | _fnevNewMail_ <br/> |メッセージ ・ ストア  <br/> |
   
> [!NOTE]
> オブジェクトの変更通知が表示されたら、 **OnNotify**呼び出しの_lpNotifications_パラメーターで指定された[OBJECT_NOTIFICATION](object_notification.md)構造体のプロパティ タグ配列の部分が可能性がありますまたは NULL にできない場合があることに注意してください。 メッセージ ストア プロバイダーは、この配列のプロパティ情報を挿入し、最もしない必要はありません。 **OnNotify**メソッドは、 _lpPropTagArray_のポインターが NULL を大文字と小文字を処理できることを確認します。 
  
通知オブジェクトのすべてではない場合は、ほとんどは、影響を受けるフォルダーまたはフォルダーのビューを更新します。
  

