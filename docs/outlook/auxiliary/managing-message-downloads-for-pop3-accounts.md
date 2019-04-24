---
title: 管理メッセージは POP3 アカウントをダウンロードします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b4218aa6-1591-49db-9782-f286135fc79a
description: このセクションでは、 Outlookの POP3 プロバイダーでの使用方法の固有 ID リスト (UIDL) 履歴、POP3 アカウントのプロバイダーがダウンロードまたは複数回、同じメッセージのダウンロードを避けるために、POP3 サーバーから削除するメッセージを識別するについて説明します。
ms.openlocfilehash: 35c50d83c317ebefa52fd9bfcb348c8411a06f25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322247"
---
# <a name="managing-message-downloads-for-pop3-accounts"></a>管理メッセージは POP3 アカウントをダウンロードします。

このセクションでは、 Outlookの POP3 プロバイダーでの使用方法の固有 ID リスト (UIDL) 履歴、POP3 アカウントのプロバイダーがダウンロードまたは複数回、同じメッセージのダウンロードを避けるために、POP3 サーバーから削除するメッセージを識別するについて説明します。
  
## <a name="introduction-to-pop"></a>ポップアップの概要

ポスト Office プロトコル (POP) は、電子メール クライアントがメール サーバーから電子メール メッセージをダウンロードするOutlookなどのアプリケーション層プロトコルを指定します。ユーザーにサーバー上のコピーをローカル デバイス (スマート フォン、コンピューター)、し、いずれかのままにする、電子メール メッセージのコピーをダウンロードしたり、削除したりできます。プロトコルは、メールボックスに同時に接続する 1 つのメール クライアントをサポートします。それを取得する必要がなく、メール サーバーから電子メール メッセージを送信する方法のみを指定します。POP を使用する場合メール クライアント通常新しい電子メール メッセージをチェックするには、だけの時間と新着メールの通知を取得するのには、サーバーへの接続を維持しませんが、新しいメッセージをダウンロードするには、メール サーバーに接続します。POP は、電子メールにカプセル化しない限り、電子メール メッセージだけがいない項目など他の種類の連絡先との予定をサポートします。POP3 は、プロトコルのバージョン 3 です。
  
POP アカウントのメッセージは、一意の識別子 (Uid) で識別されます。電子メール クライアントがメール サーバーに残ります UIDL マップを関連付けるその UID をメールボックスに送信された各メッセージを取得するために、UIDL コマンドを使用します。クライアントはダウンロードまたはクライアント上で受信トレイを削除するメッセージの UIDL 履歴も取得します。クライアントは、UIDL 履歴に基づき、メッセージは新しいをダウンロードするかを確認できます。

- [pop3 アカウントのメッセージダウンロード履歴の検索](locating-the-message-download-history-for-a-pop3-account.md): このトピックでは、メールクライアントが[PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx)プロパティにアクセスして、pop3 アカウントのクライアント受信トレイ内のメッセージの UIDL 履歴を取得する方法について説明します。 
    
- [[pop3 アカウントのメッセージのダウンロード履歴を解析](parsing-the-message-download-history-for-a-pop3-account.md)する]: このトピックでは、pop3 アカウントのクライアント受信トレイ内のメッセージの UIDL 履歴を表す pop3 BLOB を解析し、そのメッセージに対してダウンロードまたは削除されたメッセージを特定する方法について説明します。分割払.
    
## <a name="see-also"></a>関連項目

- [Outlook アカウントの管理](outlook-account-management.md)    
- [POP3 アカウントのメッセージのダウンロードの履歴を検索します。](locating-the-message-download-history-for-a-pop3-account.md) 
- [POP3 アカウントのメッセージのダウンロードの履歴の解析](parsing-the-message-download-history-for-a-pop3-account.md)   
- [PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)    
- [プロパティ (アカウント管理 API)](properties-account-management-api.md)
    

