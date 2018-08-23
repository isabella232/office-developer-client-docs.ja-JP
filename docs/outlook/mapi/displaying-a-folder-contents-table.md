---
title: フォルダーの内容のテーブルを表示します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 51c88e8c062a409db305e893b82f43d8c8ac7094
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580797"
---
# <a name="displaying-a-folder-contents-table"></a><span data-ttu-id="6254c-103">フォルダーの内容のテーブルを表示します。</span><span class="sxs-lookup"><span data-stu-id="6254c-103">Displaying a folder contents table</span></span>

<span data-ttu-id="6254c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6254c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6254c-105">フォルダーの内容のテーブルには、そのメッセージのすべてについての概要情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6254c-105">The contents table of a folder contains summary information about all of its messages.</span></span> <span data-ttu-id="6254c-106">メッセージ クラスに対応する受信フォルダーの内容のテーブルで、新しい着信メッセージについての概要情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6254c-106">Summary information about new incoming messages appears in the contents table of the receive folder for the message class.</span></span> <span data-ttu-id="6254c-107">この情報をユーザーが利用できるように、テーブルを取得し、適切な列と行を表示します。</span><span class="sxs-lookup"><span data-stu-id="6254c-107">To make this information available to users, retrieve the table and display the columns and rows as appropriate.</span></span>
  
<span data-ttu-id="6254c-108">**フォルダーの内容のテーブルを表示するには**</span><span class="sxs-lookup"><span data-stu-id="6254c-108">**To display a folder contents table**</span></span>
  
1. <span data-ttu-id="6254c-109">[IMsgStore::OpenEntry](imsgstore-openentry.md)テーブルを含むフォルダーのエントリ id を渡すことを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6254c-109">Call [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the entry identifier of the folder containing the table.</span></span>
    
2. <span data-ttu-id="6254c-110">その内容のテーブルを開くにはフォルダーの[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6254c-110">Call the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table.</span></span> 
    
3. <span data-ttu-id="6254c-111">特定の列を指定するテーブルの[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、必要な場合は、内容のテーブルの表示を制限します。</span><span class="sxs-lookup"><span data-stu-id="6254c-111">Limit your view of the contents table if desired by calling the table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to specify particular columns.</span></span> 
    
4. <span data-ttu-id="6254c-112">特定の行をフィルター選択するテーブルの[IMAPITable::Restrict](imapitable-restrict.md)メソッドを呼び出して、必要な場合は、内容のテーブルの表示を制限します。</span><span class="sxs-lookup"><span data-stu-id="6254c-112">Limit your view of the contents table if desired by calling the table's [IMAPITable::Restrict](imapitable-restrict.md) method to filter particular rows.</span></span> <span data-ttu-id="6254c-113">場合は、たとえば、読み取ることがまだ設定されて、特定のメッセージ クラスのメッセージだけを表示するのには。</span><span class="sxs-lookup"><span data-stu-id="6254c-113">If, for example, you want to show only messages with a specific message class that have yet to be read:</span></span> 
    
    1. <span data-ttu-id="6254c-114">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))、目的のメッセージ クラス プロパティに一致する[SPropertyRestriction](spropertyrestriction.md)構造体にプロパティ制約を作成します。</span><span class="sxs-lookup"><span data-stu-id="6254c-114">Create a property restriction in an [SPropertyRestriction](spropertyrestriction.md) structure that matches the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property with the desired message class.</span></span> 
        
    2. <span data-ttu-id="6254c-115">プロパティ タグと MSGFLAG_UNREAD の値として**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) をマスクとして使用する[SBitMaskRestriction](sbitmaskrestriction.md)構造体では、ビットマスクの制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="6254c-115">Create a bitmask restriction in an [SBitMaskRestriction](sbitmaskrestriction.md) structure that uses **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) as the property tag and the MSGFLAG_UNREAD value as the mask.</span></span>
        
    3. <span data-ttu-id="6254c-116">プロパティは、ビットマスクの制限を結合する[SAndRestriction](sandrestriction.md)構造に制約を作成します。</span><span class="sxs-lookup"><span data-stu-id="6254c-116">Create a restriction in an [SAndRestriction](sandrestriction.md) structure that joins the property and bitmask restrictions.</span></span> 
    
5. <span data-ttu-id="6254c-117">テーブルの[IMAPITable::SortTable](imapitable-sorttable.md)メソッドを呼び出して、必要な場合は、内容のテーブルを並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="6254c-117">Sort the contents table if desired by calling the table's [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
6. <span data-ttu-id="6254c-118">処理の内容のテーブルからすべての行を取得するために[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6254c-118">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows from the contents table for processing.</span></span> 
    

