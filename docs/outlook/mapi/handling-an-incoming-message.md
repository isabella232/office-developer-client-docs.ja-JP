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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299406"
---
# <a name="handling-an-incoming-message"></a>受信メッセージの処理

**適用対象**: Outlook 2013 | Outlook 2016 
  
受信メッセージは、1つまたは複数のメッセージングシステム間で送信されたメッセージです。 自分または他の多くの受信者にのみ送信されている可能性があります。 受信メッセージは、特定のクラスのメッセージを保持するように指定された受信フォルダーに配置されます。 処理する各メッセージクラスに対して異なる受信フォルダーを設定するか、すべてのクラスに対して1つのフォルダーを使用することができます。
  
メッセージストアでメール通知が新規に登録されている場合は、受信フォルダーにメッセージが配置されるたびに通知されます。 新しいメール通知をまだ登録していない場合は、新しいメッセージが到着したかどうかを手動で確認するために、適切な受信フォルダーを定期的に開く必要があります。
  
クライアントは、 [IMsgStore:: アドバイス](imsgstore-advise.md)を次のように設定して、新しいメール通知を登録します。 
  
- _cbEntryID_を0に設定します。 
    
- _lて tryid_を NULL に設定します。 
    
- _uleventmask_を fnevNewMail に設定します。 
    
**IMAPIAdviseSink:: onnotify**メソッドへの呼び出しの_lpnotifications_パラメーターは、受信メッセージに関する情報 (メッセージクラス、そのエントリなど) を含む**\_NEWMAIL 通知**構造を指します。識別子、親フォルダーのエントリ識別子、およびその**PR_MESSAGE_FLAGS**プロパティの内容。 通知の登録と処理の詳細については、「 [IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))」および「処理」の[通知](handling-notifications.md)を参照してください。 
  
受信メッセージをユーザーに表示する前に、そのメッセージクラスがクライアントがサポートするクラスであるかどうかを確認します。 表示されない場合は、メッセージを無視します。 クラスがサポートしている場合、メッセージを開いて表示し、メッセージのメッセージクラスに適したフォームを表示することができます。 フォームの選択は、メッセージクラスに基づいています。 IPM クラスに属するメッセージは、MAPI で実装されている既定のフォームを使用します。 クライアントによって定義されたカスタムクラスに属するメッセージは、クライアントで定義された特殊なフォームまたは MAPI の既定のフォームのいずれかを使用できます。
  
## <a name="open-and-display-an-incoming-message"></a>受信メッセージを開いて表示する
  
1. **IMsgStore:: getreceivefolder**を呼び出して、メッセージのメッセージクラスの受信フォルダーのエントリ識別子を取得し、このエントリ識別子を**IMsgStore:: openentry**に渡してフォルダーを開きます。 詳細については、「 [IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)」、「 [IMsgStore:: openentry](imsgstore-openentry.md)」、および「[メッセージストアフォルダーを開く](opening-a-message-store-folder.md)」を参照してください。
    
2. 受信フォルダーの**IMAPIContainer:: getcontentstable**メソッドを呼び出して、そのコンテンツテーブルを取得します。 詳細については、「 [IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)」を参照してください。 テーブルの**IMAPITable:: QueryRows**メソッドを呼び出して、テーブル内のすべての行を取得します。 詳細については、「 [IMAPITable:: QueryRows](imapitable-queryrows.md) and [Contents Tables](contents-tables.md)」を参照してください。 コンテンツテーブルの表示の詳細については、「[フォルダーコンテンツの表を表示する](displaying-a-folder-contents-table.md)」を参照してください。
    
3. クライアントが対話型の場合は、ユーザーがテーブルからメッセージを選択できるようにして、そのメッセージの表示に使用するフォームを指定します。 クライアントは、MAPI またはカスタムフォームによって提供される既定のフォームを使用できます。 詳細については、「 [MAPI フォームの処理](handling-mapi-forms.md)」を参照してください。
    
4. **IMsgStore:: openentry**を呼び出して、メッセージを開きます。 詳細については、「[メッセージを開く](opening-a-message.md)」を参照してください。
    
5. メッセージテキストを処理します。 詳細については、「[メッセージテキストを開く](opening-message-text.md)」を参照してください。
    
6. 各メッセージの添付ファイルをレンダリングします。 詳細については、「[添付ファイルをプレーンテキストでレンダリングする](rendering-an-attachment-in-plain-text.md)」または「 [RTF テキスト形式の添付ファイルをレンダリング](rendering-an-attachment-in-rtf-text.md)する」を参照してください。
    
7. 必要に応じて添付ファイルを開きます。 詳細について[は、「添付ファイルを開く](opening-an-attachment.md)」を参照してください。
    
## <a name="in-this-section"></a>このセクションの内容

- [メッセージテキスト](opening-message-text.md)を開く: メッセージテキストを開く方法について説明します。
    
- [添付ファイルをテキスト形式でレンダリング](rendering-an-attachment-in-plain-text.md)する: 添付ファイルをテキスト形式でレンダリングする方法について説明します。
    
- [RTF テキスト形式での添付ファイルのレンダリング](rendering-an-attachment-in-rtf-text.md): 書式設定されたテキストで添付物をレンダリングする方法について説明します。
    
- [添付ファイル](opening-an-attachment.md)を開く方法: 添付ファイルを開く方法について説明します。
    

