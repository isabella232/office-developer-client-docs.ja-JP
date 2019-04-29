---
title: メッセージ ストアの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7eca0e1f-a855-4ef7-b892-0bddee59de5e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 933dbd95a4b2f82d78e6e8035936eb2be4ba09ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407544"
---
# <a name="handling-a-message-store"></a><span data-ttu-id="561dd-103">メッセージ ストアの処理</span><span class="sxs-lookup"><span data-stu-id="561dd-103">Handling a message store</span></span>
  
<span data-ttu-id="561dd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="561dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="561dd-105">メッセージストアの処理は、クライアントの一連のタスクの重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="561dd-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="561dd-106">これらのタスクには、フォルダーとメッセージのオープン、コピー、移動、追加、および削除、さまざまなテーブルの表示、プロパティの設定、アクセスレベルの制御などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="561dd-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="561dd-107">[メッセージストアを開く](opening-a-message-store.md): セッション中に1つ以上のメッセージストアを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="561dd-108">[既定のメッセージストアを開く](opening-the-default-message-store.md): 既定のメッセージストアを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="561dd-109">[メッセージストアの検証と初期化](validating-and-initializing-a-message-store.md): メッセージストアを初期化して検証する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="561dd-110">[メッセージストアの検索](searching-a-message-store.md): 1 つまたは複数のフォルダーを調べて、検索条件に一致するメッセージを検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="561dd-111">[受信フォルダーの選択](selecting-a-receive-folder.md): 受信フォルダーを作成する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="561dd-112">[メッセージストアフォルダーを開く](opening-a-message-store-folder.md): フォルダーを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="561dd-113">[フォルダコンテンツテーブルの表示](displaying-a-folder-contents-table.md): すべてのメッセージの概要情報を含むフォルダコンテンツテーブルを表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="561dd-114">[受信トレイフォルダーのスキャン](traversing-the-inbox-folder.md): 受信トレイ内のすべてのメッセージを順番に処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="561dd-115">[メッセージまたはフォルダーのコピーまた](copying-or-moving-a-message-or-a-folder.md)は移動: 1 つまたは複数のメッセージをコピーまたは移動する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="561dd-116">[メッセージ](opening-a-message.md)を開く: メッセージを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="561dd-117">[メッセージのアイコンの検索](finding-the-icon-for-a-message.md): メッセージに関連付けられているアイコンを検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="561dd-118">[ビュー記述子](opening-a-view-descriptor.md)を開く: ビュー記述子を開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="561dd-119">[メッセージの削除](deleting-a-message.md): メッセージを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="561dd-120">[受信トレイ](saving-a-message-in-the-inbox.md)へのメッセージの保存: 受信トレイにメッセージを保存する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="561dd-121">[送信または保存](finding-sent-or-saved-messages.md)されたメッセージの検索: 保存または送信されたすべての送信メッセージを検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="561dd-122">[会話の追跡](tracking-conversations.md): 会話を追跡する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="561dd-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

