---
title: メッセージを保存する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97bff16b-dc7c-4eed-8834-d0c076d83ca3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d5ceeb46bded101700aec696a17d690bde80ce6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283122"
---
# <a name="saving-a-message"></a>メッセージを保存する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを保存する前に、クライアントは通常、メッセージの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、メッセージテキストのプロパティ、attachment プロパティ、 **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))、およびプロパティに加えて、いくつかのプロパティを設定します。宛先リストに関連付けられています。
  
**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを、IPM などの文字列に設定します。送信メッセージのクラスについての説明が記載されています。 クライアントはすべての送信メッセージに**PR_MESSAGE_CLASS**を設定する必要がありますが、設定しないと、メッセージストアプロバイダーによって既定値が提供されます。 送信メッセージの既定のメッセージクラスは IPM です。 
  
**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティで MSGFLAG_UNSENT フラグを設定します。 必要に応じて、MSGFLAG_READ および MSGFLAG_UNMODIFIED フラグも設定します。 MSGFLAG_UNMODIFIED を設定すると、[合成] の下にメッセージが表示され、配信されたメッセージをシミュレートできます。 MSGFLAG_UNMODIFIED は、メッセージが初めて保存される前に、クライアントによってのみ設定できます。 
  
未送信メッセージの永続的コピーを作成する準備ができたら、メッセージとそのすべての添付ファイルに対して、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)を呼び出します。 すぐにメッセージを送信する場合は、 **SaveChanges**を呼び出す必要はありません。 **submitmessage**を呼び出すと、メッセージは内部的に処理の一部として保存されます。 
  
**SaveChanges**を呼び出すときは、KEEP_OPEN_READWRITE フラグを指定することをお勧めします。これにより、後でメッセージを変更できるようになります。 その他の設定可能フラグには FORCE_SAVE が含まれています。これは、変更がコミットされた後に、メッセージまたは添付ファイルを閉じる必要があることを示します。 KEEP_OPEN_READONLY は、変更が行われていないことを示し、メッセージストアプロバイダーに許可するフラグバッチクライアント要求、MAPI_DEFERRED_ERRORS。
  
メッセージに対して**savechanges**を呼び出す前に、メッセージのすべての添付ファイルに対して**savechanges**を呼び出すことが重要です。 添付ファイルの保存に失敗した場合、添付ファイルは送信時にメッセージに含まれず、メッセージの添付ファイルテーブルに表示されません。 すべての添付ファイルを保存した後にメッセージを保存できない場合は、メッセージと添付ファイルの両方が失われます。 
  
**SaveChanges**が呼び出されると、メッセージストアプロバイダーは次のプロパティを更新します。 
  
- **PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) すべてのプライマリ受信者を一覧表示します。
    
- **PR_DISPLAY_TO**カーボンコピーのすべての受信者を一覧表示します。 
    
- **PR_DISPLAY_BCC**([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) すべてのブラインドカーボンコピー受信者を一覧表示します。
    
- **PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS**は、1つ以上の添付ファイルが保存されている場合は MSGFLAG_HASATTACH を設定し、メッセージが変更されたことを示すために MSGFLAG_UNMODIFIED をクリアします。 
    
- **PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) には、メッセージの最新サイズが含まれています。
    
- **PR_MESSAGE_ATTACHMENTS**([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) 添付ファイルテーブルへのアクセスを提供します。
    
- **PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) 受信者テーブルへのアクセスを提供します。
    
通常、一部のメッセージプロパティは、メッセージの作成時にクライアントまたはサービスプロバイダーによって提供されます。 クライアントが戻さを設定する場合は、 **SaveChanges**が呼び出されたときに更新されるメッセージストアプロバイダーになります。 たとえば、メッセージの作成時にメッセージの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) および**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティを設定した場合、保存時に変更する必要はありません。 ただし、メッセージの作成時に設定されていないメッセージストアプロバイダーは、 **SaveChanges**が初めて呼び出されるときに設定する必要があります。 
  
**SaveChanges**が MAPI_E_CORRUPT_DATA を返す場合は、保存されているデータが失われたと仮定します。 実装にクライアントサーバーモデルを使用するメッセージストアプロバイダーは、ネットワーク接続が失われたとき、またはサーバーが実行されていないときにこの値を返すことがあります。 ユーザーにエラーを返す前に、 **setprops**への呼び出しの後に**SaveChanges**の別の呼び出しを行って、データの書き込みと保存をもう一度実行してください。 データがローカルにキャッシュされている場合は、このような問題はありません。 ただし、ローカルキャッシュがない場合、または2番目の**SaveChanges**呼び出しが失敗した場合は、エラーを表示して問題をユーザーに警告します。 
  

