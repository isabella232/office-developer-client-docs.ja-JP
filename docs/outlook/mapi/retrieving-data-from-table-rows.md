---
title: テーブルの行からデータを所得する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 91b1fa06fd47321e9c19d9751caac793e27e8f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803771"
---
# <a name="retrieving-data-from-table-rows"></a><span data-ttu-id="76d0d-103">テーブルの行からデータを所得する</span><span class="sxs-lookup"><span data-stu-id="76d0d-103">Retrieving Data from Table Rows</span></span>

  
  
<span data-ttu-id="76d0d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76d0d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76d0d-105">テーブルから行を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76d0d-105">Retrieving rows from a table involves:</span></span>
  
- <span data-ttu-id="76d0d-106">すべての列のプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="76d0d-106">Obtaining the property values for all the columns.</span></span>
    
- <span data-ttu-id="76d0d-107">現在の位置を変更します。</span><span class="sxs-lookup"><span data-stu-id="76d0d-107">Modifying the current position.</span></span>
    
<span data-ttu-id="76d0d-108">エントリ id は、ほとんどのテーブルで必要な列のいずれかの- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) は、行を表すオブジェクトを開くことを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="76d0d-108">One of the required columns in most tables is an entry identifier — the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property — that can be used to open the object that represents the row.</span></span> <span data-ttu-id="76d0d-109">このエントリ id は、通常、いずれかのテーブルの有効期間を超えて保持されませんが、短期的なエントリ id です。</span><span class="sxs-lookup"><span data-stu-id="76d0d-109">This entry identifier is usually a short-term entry identifier, one that does not persist past the lifetime of the table.</span></span> <span data-ttu-id="76d0d-110">ただし、テーブルのみを実装するサービス プロバイダーは、エントリの識別子の 1 つの型をサポートしている場合長期的な識別子である、ことができます。</span><span class="sxs-lookup"><span data-stu-id="76d0d-110">However, it can be a long-term identifier if the service provider implementing the table only supports one type of entry identifier.</span></span>
  
<span data-ttu-id="76d0d-111">クライアントとサービス ・ プロバイダーは、以下の行を取得する呼び出しのいずれかで作成できます。</span><span class="sxs-lookup"><span data-stu-id="76d0d-111">Clients and service providers can make one of the following calls to retrieve rows:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="76d0d-112">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="76d0d-112">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="76d0d-113">前方または後方のいずれかの方向の現在の行で始まる行の指定した数を取得します。</span><span class="sxs-lookup"><span data-stu-id="76d0d-113">Retrieves a specified number of rows starting with the current row in either a forward or backward direction.</span></span>  <br/> |
|[<span data-ttu-id="76d0d-114">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="76d0d-114">HrQueryAllRows</span></span>](hrqueryallrows.md) <br/> |<span data-ttu-id="76d0d-115">すべてのテーブルの行を取得します。</span><span class="sxs-lookup"><span data-stu-id="76d0d-115">Retrieves all of the rows in a table.</span></span>  <br/> |
|[<span data-ttu-id="76d0d-116">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="76d0d-116">ITableData::HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="76d0d-117">そのインデックス列の値に基づいてテーブルの行を取得します。</span><span class="sxs-lookup"><span data-stu-id="76d0d-117">Retrieves a row in a table according to the value of its index column.</span></span> <span data-ttu-id="76d0d-118">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) は、通常、テーブルのインデックスの列です。</span><span class="sxs-lookup"><span data-stu-id="76d0d-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) is usually the index column for a table.</span></span>  <br/> |
   
<span data-ttu-id="76d0d-119">オプションのプロパティは、テーブル内の列の 1 つとして含まれているが、他のユーザーは実行できないときに、列の有効な値がいくつかの行のがあります。</span><span class="sxs-lookup"><span data-stu-id="76d0d-119">When an optional property is included as one of the columns in a table, some of the rows might have valid values for the column while others might not.</span></span> <span data-ttu-id="76d0d-120">列の有効な値が存在するかどうかは、行の情報を提供するオブジェクトがプロパティを設定するかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="76d0d-120">Whether a valid value exists for a column depends on whether the object providing the information for the row sets the property.</span></span> <span data-ttu-id="76d0d-121">オブジェクトの実装によって**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) として、テーブル、または任意の値で存在しないプロパティを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="76d0d-121">Depending on the implementation of the object, a non-existent property can be represented in the table as **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) or an arbitrary value.</span></span> <span data-ttu-id="76d0d-122">テーブルのユーザーが存在しないし、無意味な値を持つプロパティとプロパティは存在し、有効な値であることの間で区別するために注意が必要である必要があります。</span><span class="sxs-lookup"><span data-stu-id="76d0d-122">Users of tables must be careful to differentiate between properties that are nonexistent and have meaningless values and properties that do exist and have valid values.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76d0d-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="76d0d-123">See also</span></span>



[<span data-ttu-id="76d0d-124">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="76d0d-124">MAPI Tables</span></span>](mapi-tables.md)

