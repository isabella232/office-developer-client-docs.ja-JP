---
title: 受信トレイ フォルダーを通過します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 87fcde5a28a30f08bc2fd5f28fb692a4b4251fbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804139"
---
# <a name="traversing-the-inbox-folder"></a><span data-ttu-id="d7480-103">受信トレイ フォルダーを通過します。</span><span class="sxs-lookup"><span data-stu-id="d7480-103">Traversing the Inbox Folder</span></span>

  
  
<span data-ttu-id="d7480-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7480-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="d7480-105">**すべての受信トレイのメッセージを順番に表示**</span><span class="sxs-lookup"><span data-stu-id="d7480-105">**To cycle through all of the messages in the Inbox**</span></span>
  
1. <span data-ttu-id="d7480-106">受信トレイのエントリ id を取得するために[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d7480-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="d7480-107">受信トレイを開くには、 **IMAPIFolder::OpenEntry**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d7480-107">Call **IMAPIFolder::OpenEntry** to open the Inbox.</span></span> 
    
3. <span data-ttu-id="d7480-108">コンテンツ テーブルを取得するために、受信トレイの[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d7480-108">Call the Inbox's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to retrieve the contents table.</span></span> 
    
4. <span data-ttu-id="d7480-109">内容**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) に設定する列および必要なその他の任意の列を制限するテーブルの[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d7480-109">Call the contents table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and any other columns you require.</span></span> 
    
5. <span data-ttu-id="d7480-110">行のグループを取得するために[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d7480-110">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve a group of rows.</span></span> 
    
6. <span data-ttu-id="d7480-111">まで、内容のテーブルには不要になったすべての行があります。</span><span class="sxs-lookup"><span data-stu-id="d7480-111">Until there are no longer any rows in the contents table:</span></span>
    
1. <span data-ttu-id="d7480-112">各行からのエントリの識別子によって表されるメッセージを開くには、 [IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d7480-112">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the message represented by the entry identifier from each row.</span></span> 
    
2. <span data-ttu-id="d7480-113">ローカル**IMessage**インターフェイス ポインターには、 _lppUnk_パラメーターを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d7480-113">Assign the  _lppUnk_ parameter to a local **IMessage** interface pointer.</span></span> 
    
3. <span data-ttu-id="d7480-114">メッセージのプロパティを操作します。</span><span class="sxs-lookup"><span data-stu-id="d7480-114">Work with the properties of the message.</span></span>
    
4. <span data-ttu-id="d7480-115">_LppUnk_パラメーターで指定されたポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="d7480-115">Release the pointer pointed to by the  _lppUnk_ parameter.</span></span> 
    
5. <span data-ttu-id="d7480-116">行の次のグループを取得するために[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d7480-116">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the next group of rows.</span></span> 
    
7. <span data-ttu-id="d7480-117">コンテンツ テーブルを解放します。</span><span class="sxs-lookup"><span data-stu-id="d7480-117">Release the contents table.</span></span>
    

