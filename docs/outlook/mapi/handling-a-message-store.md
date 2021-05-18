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
# <a name="handling-a-message-store"></a><span data-ttu-id="ba41e-103">メッセージ ストアの処理</span><span class="sxs-lookup"><span data-stu-id="ba41e-103">Handling a message store</span></span>
  
<span data-ttu-id="ba41e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba41e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba41e-105">メッセージ ストアの処理は、クライアントの一連のタスクの重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="ba41e-105">Handling a message store is an important part of any client's set of tasks.</span></span> <span data-ttu-id="ba41e-106">これらのタスクには、フォルダーとメッセージの開き、コピー、移動、追加、削除、さまざまなテーブルの表示、プロパティの設定、アクセス レベルの制御が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ba41e-106">These tasks include opening, copying, moving, adding, and deleting folders and messages, displaying various tables, setting properties, and controlling access levels.</span></span>

- <span data-ttu-id="ba41e-107">[メッセージ ストアを開く](opening-a-message-store.md): セッション中に 1 つ以上のメッセージ ストアを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-107">[Opening a Message Store](opening-a-message-store.md): Describes how to open one or more message stores during a session.</span></span>
    
- <span data-ttu-id="ba41e-108">[既定のメッセージ ストアを開く](opening-the-default-message-store.md): 既定のメッセージ ストアを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-108">[Opening the Default Message Store](opening-the-default-message-store.md): Describes how to open the default message store.</span></span>
    
- <span data-ttu-id="ba41e-109">[メッセージ ストアの検証と初期化](validating-and-initializing-a-message-store.md): メッセージ ストアを初期化して検証する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-109">[Validating and Initializing a Message Store](validating-and-initializing-a-message-store.md): Describes how to initialize and validate a message store.</span></span>
    
- <span data-ttu-id="ba41e-110">[メッセージ ストアの検索](searching-a-message-store.md): 検索条件に一致するメッセージを探している 1 つ以上のフォルダーを検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-110">[Searching a Message Store](searching-a-message-store.md): Describes how to look through one or more folders looking for messages that match search criteria.</span></span>
    
- <span data-ttu-id="ba41e-111">[受信フォルダーの選択](selecting-a-receive-folder.md): 受信フォルダーを作成する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-111">[Selecting a Receive Folder](selecting-a-receive-folder.md): Describes the steps for creating a receive folder.</span></span>
    
- <span data-ttu-id="ba41e-112">[メッセージ ストア フォルダーを開く](opening-a-message-store-folder.md): フォルダーを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-112">[Opening a Message Store Folder](opening-a-message-store-folder.md): Describes how to open a folder.</span></span>
    
- <span data-ttu-id="ba41e-113">[[フォルダーコンテンツ テーブルの表示](displaying-a-folder-contents-table.md)] : すべてのメッセージに関する概要情報を含むフォルダーコンテンツ テーブルを表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-113">[Displaying a Folder Contents Table](displaying-a-folder-contents-table.md): Describes how to display the folder contents table that contains summary information about all of its messages.</span></span>
    
- <span data-ttu-id="ba41e-114">[受信トレイ フォルダーの移動](traversing-the-inbox-folder.md): 受信トレイ内のすべてのメッセージを循環する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-114">[Traversing the Inbox Folder](traversing-the-inbox-folder.md): Describes how to cycle through all the messages in the Inbox.</span></span>
    
- <span data-ttu-id="ba41e-115">[メッセージまたはフォルダーのコピーまたは移動](copying-or-moving-a-message-or-a-folder.md): 1 つ以上のメッセージをコピーまたは移動する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-115">[Copying or Moving a Message or a Folder](copying-or-moving-a-message-or-a-folder.md): Describes how to copy or move one or more messages.</span></span>
    
- <span data-ttu-id="ba41e-116">[メッセージを開く](opening-a-message.md): メッセージを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-116">[Opening a Message](opening-a-message.md): Describes how to open a message.</span></span>
    
- <span data-ttu-id="ba41e-117">[メッセージのアイコンを検索する](finding-the-icon-for-a-message.md): メッセージに関連付けられているアイコンを見つける方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-117">[Finding the Icon for a Message](finding-the-icon-for-a-message.md): Describes how to find an icon that is associated with a message.</span></span>
    
- <span data-ttu-id="ba41e-118">[ビュー記述子を開く](opening-a-view-descriptor.md): ビュー記述子を開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-118">[Opening a View Descriptor](opening-a-view-descriptor.md): Describes how to open a view descriptor.</span></span>
    
- <span data-ttu-id="ba41e-119">[メッセージの削除](deleting-a-message.md): メッセージを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-119">[Deleting a Message](deleting-a-message.md): Describes how to delete a message.</span></span>
    
- <span data-ttu-id="ba41e-120">[受信トレイにメッセージを保存する](saving-a-message-in-the-inbox.md): 受信トレイにメッセージを保存する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-120">[Saving a Message in the Inbox](saving-a-message-in-the-inbox.md): Describes how to store a message in the Inbox.</span></span>
    
- <span data-ttu-id="ba41e-121">[[送信済みメッセージまたは保存](finding-sent-or-saved-messages.md)済みメッセージの検索] : 保存または送信済みのすべての送信メッセージを検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-121">[Finding Sent or Saved Messages](finding-sent-or-saved-messages.md): Describes how to locate all outgoing messages that have been saved or sent.</span></span>
    
- <span data-ttu-id="ba41e-122">[会話の追跡](tracking-conversations.md): 会話を追跡する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba41e-122">[Tracking Conversations](tracking-conversations.md): Describes how to track conversations.</span></span>
    

