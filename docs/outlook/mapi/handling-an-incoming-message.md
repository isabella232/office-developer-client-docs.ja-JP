---
title: 受信メッセージを処理します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d45d5ed9-41cd-4aaf-91d2-1e4a27bb16d4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5705af6c8efaf42ae27d1b39bb28d162971ebf9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800175"
---
# <a name="handling-an-incoming-message"></a>受信メッセージを処理します。

**適用対象**: Outlook 
  
受信メッセージは、1 つまたは複数のメッセージング システム間で送信されたメッセージです。 送られた場合にのみ、または他の多くの受信者にします。 受信メッセージは、特定のクラスのメッセージを保持するために指定された受信フォルダーに配置されます。 設定することができます、さまざまな処理または、すべてのクラスの 1 つのフォルダーを使用するメッセージ クラスごとにフォルダーが表示されます。
  
場合はメッセージ ・ ストアに新しいメールの通知を登録すると、受信フォルダー内にメッセージを配置するたびに通知されます。 新着メール通知を登録していない状態で開く必要があります、適切なフォルダーを手動で新着メッセージの到着を確認するには、定期的に受信します。
  
クライアントは、次のように[IMsgStore::Advise](imsgstore-advise.md)にパラメーターを設定することで新着メール通知の登録します。 
  
- _CbEntryID_を 0 に設定します。 
    
- _LpEntryID_を NULL に設定されます。 
    
- _UlEventMask_を fnevNewMail に設定します。 
    
**IMAPIAdviseSink::OnNotify**メソッドの呼び出し内の_lpNotifications_パラメーターが指す、 **NEWMAIL\_通知**のエントリのメッセージ クラスなど、着信メッセージについての情報を格納する構造体識別子では、その親フォルダーのエントリ id と、 **PR_MESSAGE_FLAGS**プロパティの内容です。 登録して、通知を処理する方法の詳細については、 [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)、 [NEWMAIL_NOTIFICATION](newmail_notification.md)、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))、および[通知の処理](handling-notifications.md)を参照してください。 
  
ユーザーに受信したメッセージを表示する前に、メッセージ クラスは、クライアントをサポートするクラスを決定します。 それ以外の場合は、メッセージを無視します。 クラスをサポートする場合は、開くし、メッセージのメッセージ クラスに適切なフォームを使用してメッセージを表示できます。 フォームの選択は、メッセージ クラスに基づいています。 IPM クラスに属しているメッセージは、MAPI によって実装されている既定のフォームを使用します。 クライアントが定義されているカスタムのクラスに属しているメッセージには、特別な形式のクライアント定義または MAPI の既定のフォームのいずれかを使用できます。
  
## <a name="open-and-display-an-incoming-message"></a>開き、受信したメッセージを表示
  
1. メッセージのメッセージ クラスに対応する受信フォルダーのエントリ id を取得し、フォルダーを開くには、 **IMsgStore::OpenEntry**にこのエントリの識別子を渡す**IMsgStore::GetReceiveFolder**を呼び出します。 詳細については、 [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)、 [IMsgStore::OpenEntry](imsgstore-openentry.md)、および[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md)を参照してください。
    
2. コンテンツ テーブルを取得するために、受信フォルダーの**IMAPIContainer::GetContentsTable**メソッドを呼び出します。 詳細については、 [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)を参照してください。 テーブル内のすべての行を取得するためにテーブルの**IMAPITable::QueryRows**メソッドを呼び出します。 詳細については、 [IMAPITable::QueryRows](imapitable-queryrows.md)と[内容のテーブル](contents-tables.md)を参照してください。 コンテンツ テーブルを表示する方法についての詳細については、[フォルダーの内容のテーブルを表示する](displaying-a-folder-contents-table.md)を参照してください。
    
3. クライアントが対話型の場合は、テーブルからメッセージを選択し、そのメッセージを表示に使用する形式を決定するユーザーを許可します。 クライアントは、MAPI またはユーザー設定のフォームで提供される既定のフォームを使用できます。 詳細については、 [MAPI フォームの処理](handling-mapi-forms.md)を参照してください。
    
4. メッセージを開くには、 **IMsgStore::OpenEntry**を呼び出します。 詳細については、[メッセージを開く](opening-a-message.md)を参照してください。
    
5. メッセージのテキストを処理します。 詳細については、[開始メッセージのテキスト](opening-message-text.md)を参照してください。
    
6. 各メッセージの添付ファイルをレンダリングします。 詳細については、[テキスト形式の添付ファイルを表示](rendering-an-attachment-in-plain-text.md)または[rtf 形式のテキストの添付ファイルのレンダリング](rendering-an-attachment-in-rtf-text.md)を参照してください。
    
7. 必要な場合は、添付ファイルを開きます。 詳細については、[添付ファイルを開く](opening-an-attachment.md)を参照してください。
    
## <a name="in-this-section"></a>このセクションの内容

- [開始メッセージ テキスト](opening-message-text.md): メッセージのテキストを開く方法について説明します。
    
- [テキスト形式の添付ファイルを表示](rendering-an-attachment-in-plain-text.md): テキスト形式の添付ファイルをレンダリングする方法について説明します。
    
- [Rtf 形式のテキストの添付ファイルを表示](rendering-an-attachment-in-rtf-text.md): 書式設定されたテキストの添付ファイルをレンダリングする方法について説明します。
    
- [添付ファイルを開く](opening-an-attachment.md): 添付ファイルを開く方法について説明します。
    

