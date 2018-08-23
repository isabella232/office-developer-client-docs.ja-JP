---
title: メッセージの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97bff16b-dc7c-4eed-8834-d0c076d83ca3
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e61a72691309b2ac632b764c0607f5b1e36b291b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803800"
---
# <a name="saving-a-message"></a>メッセージの保存

  
  
**適用対象**: Outlook 
  
クライアントではメッセージのテキストのプロパティ、添付ファイルのプロパティ、**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))、およびプロパティだけでなく、いくつかのプロパティを設定するのには、メッセージの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出す通常メッセージを保存すると、前に受信者のリストに関連付けられています。
  
IPM などの文字の文字列には、 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティを設定します。送信メッセージのクラスを説明する注意してください。 クライアントは、すべての送信メッセージで**PR_MESSAGE_CLASS**を設定する必要があります、それを設定しない場合は、メッセージ ストア プロバイダーによって既定値を指定します。 送信メッセージの既定のメッセージ クラスは、IPM. 
  
**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティでは、MSGFLAG_UNSENT フラグを設定します。 必要な場合も、MSGFLAG_READ と MSGFLAG_UNMODIFIED フラグを設定します。 MSGFLAG_UNMODIFIED を設定すると、配信されたメッセージをシミュレートするコンポジションの下のメッセージができます。 メッセージが最初に保存された前に、MSGFLAG_UNMODIFIED はのみのクライアントで設定できます。 
  
未送信メッセージの永続的なコピーを作成する準備ができたら、メッセージとその添付ファイルのすべての[IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出します。 すぐにメッセージを送信する場合は、 **SaveChanges**の呼び出しにする必要はありません。 **SubmitMessage**への呼び出しは、内部での処理の一部としてメッセージを保存します。 
  
**SaveChanges**メソッドを呼び出すときは、メッセージは後で変更することができる KEEP_OPEN_READWRITE フラグを指定することをお勧めします。 その他の設定可能なフラグは、FORCE_SAVE で、閉じたことを示します、メッセージまたは添付ファイルする必要があります、変更がコミットされた後、KEEP_OPEN_READONLY、さらには、変更されないことを示す、フラグにメッセージ ストア プロバイダーを許可するにはMAPI_DEFERRED_ERRORS のクライアント要求をバッチ処理します。
  
メッセージ**SaveChanges**を呼び出す前に、 **SaveChanges**をメッセージに添付されているすべての呼び出すことが重要です。 失敗した場合、添付ファイルを保存するのには、添付ファイルはできません、メッセージに含まれて送信され、メッセージの添付ファイル テーブルに表示されません。 失敗するとすべての添付ファイルを保存した後、メッセージを保存するのには、メッセージと添付ファイルは失われます。 
  
**SaveChanges**が呼び出されると、メッセージ ストア プロバイダーは、次のプロパティを更新します。 
  
- **PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) は、プライマリのすべての受信者を一覧表示します。
    
- **PR_DISPLAY_TO**は、すべてのカーボン コピー受信者を一覧表示します。 
    
- **PR_DISPLAY_BCC**([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) は、すべてのブラインド カーボン コピー受信者を一覧表示します。
    
- **PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS**は、1 つまたは複数の添付ファイルが保存されている場合に MSGFLAG_HASATTACH を設定し、メッセージが変更を表示するのには MSGFLAG_UNMODIFIED をクリアします。 
    
- **PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) には、メッセージの現在のほとんどのサイズが含まれています。
    
- **PR_MESSAGE_ATTACHMENTS**([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) は、添付ファイル テーブルへのアクセスを提供します。
    
- **PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) は、受信者のテーブルへのアクセスを提供します。
    
いくつかのメッセージ プロパティは、メッセージが作成されるとき、通常クライアントまたはサービス プロバイダーによって提供されます。 クライアントは、これらの設定をしなかった、 **SaveChanges**が呼び出されたときにそれらを更新するメッセージ ストア プロバイダーがあります。 たとえば、メッセージの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) と**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) のプロパティは、メッセージの作成時に設定されている場合、必要がありますに変更時間を節約します。 ただし、メッセージ ストア プロバイダーにメッセージの作成時に設定を無視するこれらの値は**SaveChanges**が呼び出される最初の時間です。 
  
**SaveChanges** MAPI_E_CORRUPT_DATA が返された場合を想定していますが保存されているデータが失われるようになりました。 ネットワーク接続が切断またはサーバーが実行されていない場合、実装する場合のクライアント サーバー モデルを使用するメッセージ ストア プロバイダーはこの値を返す可能性があります。 ユーザーにエラーを返す前に、書き込みおよび**SetProps** **savechanges メソッド**の呼び出しを別の順に呼び出すことによってもう一度データを保存してみてください。 場合は、データをローカルにキャッシュすると、この問題はしないでください。 ただし、ローカル キャッシュがない、または 2 番目の**SaveChanges**の呼び出しが失敗した場合、この問題をユーザーに警告するエラーを表示します。 
  

