---
title: 受信メッセージの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d45d5ed9-41cd-4aaf-91d2-1e4a27bb16d4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f3fbe34793e3520b26b984f4bd6b14fbcab7a951
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438982"
---
# <a name="handling-an-incoming-message"></a>受信メッセージの処理

**適用対象**: Outlook 2013 | Outlook 2016 
  
受信メッセージは、1 つ以上のメッセージング システムで送信されたメッセージです。 ユーザーまたは他の多くの受信者にのみ送信されている可能性があります。 受信メッセージは、特定のクラスのメッセージを保持するために指定された受信フォルダーに配置されます。 処理するメッセージ クラスごとに異なる受信フォルダーを設定するか、すべてのクラスに 1 つのフォルダーを使用できます。
  
メッセージ ストアに新しいメール通知を登録している場合は、メッセージが受信フォルダーに配置されるたびに通知されます。 新しいメール通知に登録していない場合は、適切な受信フォルダーを定期的に開き、新しいメッセージの到着を手動で確認する必要があります。
  
クライアントは、パラメーターを [IMsgStore::Advise](imsgstore-advise.md) に次のように設定して、新しいメール通知に登録します。 
  
- _cbEntryID を_ 0 に設定します。 
    
- _lpEntryID を_ NULL に設定します。 
    
- _ulEventMask を_ fnevNewMail に設定します。 
    
**IMAPIAdviseSink::OnNotify** メソッドの呼び出しの _lpNotifications_ パラメーターは、メッセージ クラス、エントリ識別子、親フォルダーのエントリ識別子、および PR_MESSAGE_FLAGS プロパティの内容など、受信メッセージに関する情報を含む **NEWMAIL** **\_ NOTIFICATION** 構造体をポイントします。 通知の登録と処理の詳細[](handling-notifications.md)については[、「IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)」、NEWMAIL_NOTIFICATION [、PR_MESSAGE_FLAGS](newmail_notification.md)[(PidTagMessageFlags)、](pidtagmessageflags-canonical-property.md)および通知の処理を参照してください。  
  
ユーザーに受信メッセージを表示する前に、そのメッセージ クラスがクライアントがサポートするクラスかどうかを確認します。 メッセージが表示されない場合は、メッセージを無視します。 クラスがサポートするクラスの場合は、メッセージのメッセージ クラスに適したフォームでメッセージを開いて表示できます。 フォームの選択は、メッセージ クラスに基づいて行います。 IPM クラスに属するメッセージは、MAPI によって実装された既定のフォームを使用します。 クライアントによって定義されたカスタム クラスに属するメッセージは、クライアント定義の特殊なフォームまたは MAPI 既定のフォームを使用できます。
  
## <a name="open-and-display-an-incoming-message"></a>受信メッセージを開いて表示する
  
1. **IMsgStore::GetReceiveFolder** を呼び出して、メッセージのメッセージ クラスの受信フォルダーのエントリ識別子を取得し、このエントリ識別子を **IMsgStore::OpenEntry** に渡してフォルダーを開きます。 詳細については [、「IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) [、IMsgStore::OpenEntry」、](imsgstore-openentry.md)および「メッセージ ストア フォルダーを開く」 [を参照してください](opening-a-message-store-folder.md)。
    
2. 受信フォルダーの **IMAPIContainer::GetContentsTable** メソッドを呼び出して、そのコンテンツ テーブルを取得します。 詳細については [、「IMAPIContainer::GetContentsTable」を参照してください](imapicontainer-getcontentstable.md)。 テーブルのすべての行を取得するには、テーブル **の IMAPITable::QueryRows** メソッドを呼び出します。 詳細については [、「IMAPITable::QueryRows and Contents](imapitable-queryrows.md) [Tables」を参照してください](contents-tables.md)。 コンテンツ テーブルの表示の詳細については、「フォルダー [コンテンツ テーブルの表示」を参照してください](displaying-a-folder-contents-table.md)。
    
3. クライアントが対話型の場合は、ユーザーがテーブルからメッセージを選択し、そのメッセージの表示に使用するフォームを決定できます。 クライアントは、MAPI またはカスタム フォームによって提供される既定のフォームを使用できます。 詳細については、「MAPI フォームの [処理」を参照してください](handling-mapi-forms.md)。
    
4. **メッセージを開く IMsgStore::OpenEntry** を呼び出します。 詳細については、「メッセージを開 [く」を参照してください](opening-a-message.md)。
    
5. メッセージ テキストを処理します。 詳細については、「メッセージ テキストを開 [く」を参照してください](opening-message-text.md)。
    
6. 各メッセージ添付ファイルをレンダリングします。 詳細については、「プレーン テキストで [添付ファイルをレンダリング](rendering-an-attachment-in-plain-text.md) する」または [「RTF テキストで添付ファイルをレンダリングする」を参照してください](rendering-an-attachment-in-rtf-text.md)。
    
7. 必要に応じて添付ファイルを開きます。 詳細については、「添付ファイルを [開く」を参照してください](opening-an-attachment.md)。
    
## <a name="in-this-section"></a>このセクションの内容

- [メッセージ テキストを開](opening-message-text.md)く : メッセージ テキストを開く方法について説明します。
    
- [プレーン テキストで添付ファイルをレンダリング](rendering-an-attachment-in-plain-text.md)する : プレーン テキストで添付ファイルをレンダリングする方法について説明します。
    
- [RTF テキストで添付ファイルをレンダリング](rendering-an-attachment-in-rtf-text.md)する : 書式設定されたテキストで添付ファイルをレンダリングする方法について説明します。
    
- [添付ファイルを開く](opening-an-attachment.md): 添付ファイルを開く方法について説明します。
    

