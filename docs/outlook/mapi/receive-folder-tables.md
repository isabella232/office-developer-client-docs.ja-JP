---
title: フォルダー受信テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b88545ede6275bd834fad5869d972e2860a6c77e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573181"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="5907f-103">フォルダー受信テーブル</span><span class="sxs-lookup"><span data-stu-id="5907f-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="5907f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5907f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5907f-105">受信フォルダー テーブルには、メッセージ ストアの受信フォルダーとして指定されているすべてのフォルダーの情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5907f-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="5907f-106">受信フォルダーは、特定のメッセージ クラスの着信メッセージが配置されているフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="5907f-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="5907f-107">メッセージ ストア プロバイダーの実装には、フォルダーのテーブルが表示され、 [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)メソッドを呼び出すことによって、クライアント アプリケーションを使用します。</span><span class="sxs-lookup"><span data-stu-id="5907f-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="5907f-108">必要な列セットを次のプロパティには、フォルダーのテーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5907f-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="5907f-109">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5907f-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="5907f-110">**PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5907f-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="5907f-111">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5907f-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5907f-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="5907f-112">See also</span></span>



[<span data-ttu-id="5907f-113">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="5907f-113">MAPI Tables</span></span>](mapi-tables.md)

