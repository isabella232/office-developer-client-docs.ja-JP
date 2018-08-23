---
title: メッセージ ストア プロバイダーでのテーブルのグループ化と制限
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 33c76cdd0e7850f82949349ac2e5bb0dd4e056ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800172"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="29ae0-103">メッセージ ストア プロバイダーでのテーブルのグループ化と制限</span><span class="sxs-lookup"><span data-stu-id="29ae0-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="29ae0-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="29ae0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="29ae0-105">クライアント アプリケーション頻繁にできるように、フォルダーの内容を表示する方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="29ae0-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="29ae0-106">通常、ユーザーはメッセージを 1 つまたは複数のメッセージのプロパティの値に基づいてグループ化することができますか、特定の条件に一致するメッセージを除外することができます。</span><span class="sxs-lookup"><span data-stu-id="29ae0-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="29ae0-107">使用して、これは、 [IMAPITable: IUnknown](imapitableiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="29ae0-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="29ae0-108">クライアント アプリケーションは、ユーザーが指定されている基準に、テーブルから返される行を制限できます。</span><span class="sxs-lookup"><span data-stu-id="29ae0-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="29ae0-109">したがって、メッセージは、次**IMAPITable**メソッドを実装するプロバイダーのニーズを格納します。</span><span class="sxs-lookup"><span data-stu-id="29ae0-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="29ae0-110">* * IMAPITable メソッド * *</span><span class="sxs-lookup"><span data-stu-id="29ae0-110">****IMAPITable** method**</span></span>|<span data-ttu-id="29ae0-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="29ae0-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29ae0-112">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="29ae0-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="29ae0-113">テーブルの指定した条件に一致する行を返します。</span><span class="sxs-lookup"><span data-stu-id="29ae0-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="29ae0-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="29ae0-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="29ae0-115">テーブルまたは現在使用されている列のセット内の列のセットを返します。</span><span class="sxs-lookup"><span data-stu-id="29ae0-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="29ae0-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="29ae0-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="29ae0-117">指定した位置から、テーブルから 1 つまたは複数の行を返します。</span><span class="sxs-lookup"><span data-stu-id="29ae0-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="29ae0-118">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="29ae0-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="29ae0-119">**FindRow**の以降の呼び出しが制限に一致する行だけを返すには、制限テーブルに適用されます。</span><span class="sxs-lookup"><span data-stu-id="29ae0-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="29ae0-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="29ae0-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="29ae0-121">行はテーブルから取得するときに返される列を指定します。</span><span class="sxs-lookup"><span data-stu-id="29ae0-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="29ae0-122">制限を実装するのには複雑になること詳細については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29ae0-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="29ae0-123">テーブルを実装する方法の詳細については、 [MAPI テーブル](mapi-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29ae0-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29ae0-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="29ae0-124">See also</span></span>



<span data-ttu-id="29ae0-125">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="29ae0-125">[Message Store Features](message-store-features.md)</span></span>

