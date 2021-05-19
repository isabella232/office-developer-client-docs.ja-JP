---
title: フォルダー テーブルの受信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417351"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="e52b7-103">フォルダー テーブルの受信</span><span class="sxs-lookup"><span data-stu-id="e52b7-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="e52b7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e52b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e52b7-105">受信フォルダー テーブルには、メッセージ ストアの受信フォルダーとして指定されているすべてのフォルダーの情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e52b7-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="e52b7-106">受信フォルダーは、特定のメッセージ クラスの受信メッセージが配置されるフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="e52b7-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="e52b7-107">メッセージ ストア プロバイダーは受信フォルダー テーブルを実装し、クライアント アプリケーションは [、IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) メソッドを呼び出して使用します。</span><span class="sxs-lookup"><span data-stu-id="e52b7-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="e52b7-108">次のプロパティは、受信フォルダー テーブルで必要な列セットを構成します。</span><span class="sxs-lookup"><span data-stu-id="e52b7-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="e52b7-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e52b7-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="e52b7-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e52b7-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="e52b7-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e52b7-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e52b7-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="e52b7-112">See also</span></span>



[<span data-ttu-id="e52b7-113">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="e52b7-113">MAPI Tables</span></span>](mapi-tables.md)

