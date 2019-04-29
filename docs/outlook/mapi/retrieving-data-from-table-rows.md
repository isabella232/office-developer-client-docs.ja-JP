---
title: テーブルの行からデータを取得する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2f389d26ec80b9af3ed28c5eb85b589c9cbb26c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405255"
---
# <a name="retrieving-data-from-table-rows"></a><span data-ttu-id="d59c2-103">テーブルの行からデータを取得する</span><span class="sxs-lookup"><span data-stu-id="d59c2-103">Retrieving Data from Table Rows</span></span>

  
  
<span data-ttu-id="d59c2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d59c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d59c2-105">テーブルから行を取得するには、次の処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="d59c2-105">Retrieving rows from a table involves:</span></span>
  
- <span data-ttu-id="d59c2-106">すべての列のプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d59c2-106">Obtaining the property values for all the columns.</span></span>
    
- <span data-ttu-id="d59c2-107">現在の位置を変更します。</span><span class="sxs-lookup"><span data-stu-id="d59c2-107">Modifying the current position.</span></span>
    
<span data-ttu-id="d59c2-108">ほとんどのテーブルで必要な列の1つはエントリ識別子 ( \*\*\*\* [PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティで、これを使用して行を表すオブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="d59c2-108">One of the required columns in most tables is an entry identifier — the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property — that can be used to open the object that represents the row.</span></span> <span data-ttu-id="d59c2-109">このエントリ識別子は、通常、短い用語のエントリ識別子です。これは、テーブルの有効期間を超えて保持されないものです。</span><span class="sxs-lookup"><span data-stu-id="d59c2-109">This entry identifier is usually a short-term entry identifier, one that does not persist past the lifetime of the table.</span></span> <span data-ttu-id="d59c2-110">ただし、テーブルを実装するサービスプロバイダーが1つの種類のエントリ識別子のみをサポートする場合は、長期の識別子になることがあります。</span><span class="sxs-lookup"><span data-stu-id="d59c2-110">However, it can be a long-term identifier if the service provider implementing the table only supports one type of entry identifier.</span></span>
  
<span data-ttu-id="d59c2-111">クライアントとサービスプロバイダーは、次のいずれかの呼び出しを行って行を取得できます。</span><span class="sxs-lookup"><span data-stu-id="d59c2-111">Clients and service providers can make one of the following calls to retrieve rows:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="d59c2-112">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="d59c2-112">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="d59c2-113">前方または後方のどちらかの方向に、現在の行から始まる指定された数の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="d59c2-113">Retrieves a specified number of rows starting with the current row in either a forward or backward direction.</span></span>  <br/> |
|[<span data-ttu-id="d59c2-114">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="d59c2-114">HrQueryAllRows</span></span>](hrqueryallrows.md) <br/> |<span data-ttu-id="d59c2-115">テーブル内のすべての行を取得します。</span><span class="sxs-lookup"><span data-stu-id="d59c2-115">Retrieves all of the rows in a table.</span></span>  <br/> |
|[<span data-ttu-id="d59c2-116">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="d59c2-116">ITableData::HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="d59c2-117">インデックス列の値に従って、テーブル内の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="d59c2-117">Retrieves a row in a table according to the value of its index column.</span></span> <span data-ttu-id="d59c2-118">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) は、通常、テーブルのインデックス列です。</span><span class="sxs-lookup"><span data-stu-id="d59c2-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) is usually the index column for a table.</span></span>  <br/> |
   
<span data-ttu-id="d59c2-119">オプションのプロパティがテーブルの列の1つとして含まれている場合、一部の行には列に有効な値が含まれている場合がありますが、それ以外の場合もあります。</span><span class="sxs-lookup"><span data-stu-id="d59c2-119">When an optional property is included as one of the columns in a table, some of the rows might have valid values for the column while others might not.</span></span> <span data-ttu-id="d59c2-120">列に有効な値が存在するかどうかは、その行の情報を提供するオブジェクトがプロパティを設定するかどうかによって決まります。</span><span class="sxs-lookup"><span data-stu-id="d59c2-120">Whether a valid value exists for a column depends on whether the object providing the information for the row sets the property.</span></span> <span data-ttu-id="d59c2-121">オブジェクトの実装によっては、存在しないプロパティをテーブルで**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) または任意の値として表すことができます。</span><span class="sxs-lookup"><span data-stu-id="d59c2-121">Depending on the implementation of the object, a non-existent property can be represented in the table as **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) or an arbitrary value.</span></span> <span data-ttu-id="d59c2-122">テーブルのユーザーは、存在しないプロパティと、存在しない値および有効な値を持つプロパティを慎重に区別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d59c2-122">Users of tables must be careful to differentiate between properties that are nonexistent and have meaningless values and properties that do exist and have valid values.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d59c2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="d59c2-123">See also</span></span>



[<span data-ttu-id="d59c2-124">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="d59c2-124">MAPI Tables</span></span>](mapi-tables.md)

