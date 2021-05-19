---
title: メッセージの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97bff16b-dc7c-4eed-8834-d0c076d83ca3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d5ceeb46bded101700aec696a17d690bde80ce6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420933"
---
# <a name="saving-a-message"></a>メッセージの保存

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを保存する前に、クライアントは通常、メッセージの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出して、メッセージ テキストプロパティ、添付ファイルプロパティ、PR_SUBJECT[(PidTagSubject)、](pidtagsubject-canonical-property.md)および受信者リストに関連付けられたプロパティに加えていくつかのプロパティを設定します。 
  
プロパティ **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを IPM などの文字列に設定します。送信メッセージのクラスについて説明します。 クライアントは、すべての送信 **メッセージPR_MESSAGE_CLASS** を設定する必要があります。設定しない場合、既定値はメッセージ ストア プロバイダーによって提供されます。 送信メッセージの既定のメッセージ クラスは IPM です。 
  
プロパティ ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md) **)** MSGFLAG_UNSENTで、PR_MESSAGE_FLAGSフラグを設定します。 必要に応じて、MSGFLAG_READフラグMSGFLAG_UNMODIFIEDします。 メッセージを設定MSGFLAG_UNMODIFIED構成下のメッセージが配信されたメッセージをシミュレートできます。 MSGFLAG_UNMODIFIEDは、メッセージが初めて保存される前にクライアントによってのみ設定できます。 
  
送信されていないメッセージの永続的なコピーを作成する準備ができたら、メッセージとその添付ファイルの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) を呼び出します。 メッセージをすぐ送信する場合は **、SaveChanges** を呼び出す必要があります。 **SubmitMessage の呼び出しは**、メッセージを処理の一部として内部的に保存します。 
  
**SaveChanges** を呼び出す場合は、メッセージを後で変更できる KEEP_OPEN_READWRITE フラグを指定すると良い考えです。 その他の設定可能なフラグには、FORCE_SAVE が含まれます。これは、変更がコミットされた後にメッセージまたは添付ファイルを閉じるべきであり、KEEP_OPEN_READONLY は、これ以上変更を加えなくる必要がない、およびメッセージ ストア プロバイダーがクライアント要求をバッチ処理できるフラグ MAPI_DEFERRED_ERRORS です。
  
メッセージの **SaveChanges** を呼び出す前に、メッセージ内のすべての添付ファイルに対して **SaveChanges** を呼び出す必要があります。 添付ファイルを保存できない場合、添付ファイルは送信時にメッセージに含まれません。メッセージの添付ファイルテーブルには表示されません。 すべての添付ファイルを保存した後にメッセージを保存できなかった場合、メッセージと添付ファイルの両方が失われます。 
  
**SaveChanges が呼** び出された場合、メッセージ ストア プロバイダーは次のプロパティを更新します。 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) は、すべてのプライマリ受信者を一覧表示します。
    
- **PR_DISPLAY_TO** カーボン コピー受信者の一覧を表示します。 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) には、すべてのブラインド カーボン コピー受信者が一覧表示されます。
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** 1 つMSGFLAG_HASATTACH添付ファイルが保存されている場合に、メッセージが変更されたMSGFLAG_UNMODIFIEDをクリアする場合に設定します。 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) には、メッセージの最新サイズが含まれる。
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) は、添付ファイル テーブルへのアクセスを提供します。
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) は、受信者テーブルへのアクセスを提供します。
    
一部のメッセージ プロパティは、通常、メッセージの作成時にクライアントまたはサービス プロバイダーによって提供されます。 クライアントが設定を無視した場合 **、SaveChanges** が呼び出された時点でメッセージ ストア プロバイダーが更新を行う必要があります。 たとえば、メッセージの作成時にメッセージの **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティと **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティが設定されている場合、保存時に変更する必要があります。 ただし、メッセージの作成時に設定を無視するメッセージ ストア プロバイダーは **、SaveChanges** が初めて呼び出された時点で設定する必要があります。 
  
**SaveChanges が** データ を返MAPI_E_CORRUPT_DATA、保存されているデータが失われたと仮定します。 クライアント サーバー モデルを実装に使用するメッセージ ストア プロバイダーは、ネットワーク接続が失われたり、サーバーが実行されていない場合に、この値を返す可能性があります。 ユーザーにエラーを返す前に **、SetProps** を呼び出し、続いて **SaveChanges** を別の呼び出しでデータを書き込み、もう一度保存してみてください。 データがローカルにキャッシュされている場合、これは問題ではありません。 ただし、ローカル キャッシュがない場合、または 2 番目の **SaveChanges** 呼び出しが失敗した場合は、エラーを表示してユーザーに問題を通知します。 
  

