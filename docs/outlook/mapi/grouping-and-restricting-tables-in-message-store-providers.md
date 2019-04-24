---
title: メッセージストアプロバイダーでのテーブルのグループ化と制限
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299413"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="234e0-103">メッセージストアプロバイダーでのテーブルのグループ化と制限</span><span class="sxs-lookup"><span data-stu-id="234e0-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="234e0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="234e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="234e0-105">多くの場合、クライアントアプリケーションでは、フォルダーの内容の表示方法をユーザーが制御できます。</span><span class="sxs-lookup"><span data-stu-id="234e0-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="234e0-106">通常、ユーザーは1つまたは複数のメッセージプロパティの値に従ってグループ化されたメッセージを表示するか、または特定の条件に一致するメッセージを除外するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="234e0-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="234e0-107">これは、 [IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスを使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="234e0-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="234e0-108">クライアントアプリケーションは、テーブルから返される行を、ユーザーが指定した条件に制限できます。</span><span class="sxs-lookup"><span data-stu-id="234e0-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="234e0-109">そのため、メッセージストアプロバイダーでは、次の**IMAPITable**メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="234e0-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="234e0-110">IMAPITable \* \* メソッド \* \*</span><span class="sxs-lookup"><span data-stu-id="234e0-110">\*\*\*\*IMAPITable\*\* method\*\*</span></span>|<span data-ttu-id="234e0-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="234e0-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="234e0-112">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="234e0-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="234e0-113">指定した条件に一致するテーブルの行を返します。</span><span class="sxs-lookup"><span data-stu-id="234e0-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="234e0-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="234e0-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="234e0-115">テーブル内の列のセット、または現在使用されている列のセットを返します。</span><span class="sxs-lookup"><span data-stu-id="234e0-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="234e0-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="234e0-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="234e0-117">指定された位置から開始して、1つまたは複数の行をテーブルから返します。</span><span class="sxs-lookup"><span data-stu-id="234e0-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="234e0-118">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="234e0-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="234e0-119">**FindRow**への後続の呼び出しが、制限に一致する行のみを返すようにテーブルに制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="234e0-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="234e0-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="234e0-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="234e0-121">テーブルから行が取得されたときに返される列を指定します。</span><span class="sxs-lookup"><span data-stu-id="234e0-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="234e0-122">制限は、実装するのが複雑な場合があります。詳細については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="234e0-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="234e0-123">テーブルの実装の詳細については、「 [MAPI テーブル](mapi-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="234e0-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="234e0-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="234e0-124">See also</span></span>



<span data-ttu-id="234e0-125">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="234e0-125">[Message Store Features](message-store-features.md)</span></span>

