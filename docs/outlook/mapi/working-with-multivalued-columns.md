---
title: 複数値の列の操作
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 34f19e279c86e0c0856d242cf2aa13d744d46f13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420186"
---
# <a name="working-with-multivalued-columns"></a><span data-ttu-id="d3cb9-103">複数値の列の操作</span><span class="sxs-lookup"><span data-stu-id="d3cb9-103">Working with Multivalued Columns</span></span>

  
  
<span data-ttu-id="d3cb9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3cb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3cb9-105">複数値の列には、複数値プロパティのデータが含まれます。これは、1 つの値ではなく、基本型の値の配列を持つプロパティです。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-105">A multivalued column contains the data of a multivalued property, which is a property that has an array of values of the base type instead of a single value.</span></span> <span data-ttu-id="d3cb9-106">既定の列セットには複数値プロパティが含まれているテーブルはないので、テーブルのユーザーが要求した場合にのみ、複数値プロパティがテーブルに含まれます。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-106">Because none of the tables include multivalued properties in their default column sets, multivalued properties are included in a table only if the user of the table requests it.</span></span> 
  
<span data-ttu-id="d3cb9-107">複数値の列は、次の表に表示できます。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-107">Multivalued columns can be displayed in tables:</span></span>
  
- <span data-ttu-id="d3cb9-108">1 つの行で、すべてのプロパティ値が 1 つの列インスタンスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-108">In a single row, with all of the property values appearing in the single column instance.</span></span> <span data-ttu-id="d3cb9-109">これが既定です。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-109">This is the default.</span></span>
    
    - <span data-ttu-id="d3cb9-110">Or -</span><span class="sxs-lookup"><span data-stu-id="d3cb9-110">Or -</span></span>
    
- <span data-ttu-id="d3cb9-111">一連の行で、プロパティ値ごとに 1 行を指定します。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-111">In a series of rows, with one row for each of the property values.</span></span> <span data-ttu-id="d3cb9-112">各一意の値は、複数値プロパティの値と同じ数の行を持つ、独自の行の列に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-112">Each unique value appears in the column in its own row with there being as many rows as there are values in the multivalued property.</span></span> <span data-ttu-id="d3cb9-113">各行には、PR_INSTANCE_KEY **(** [PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティの一意の値がありますが、他の列の値は同じです。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-113">Each row has a unique value for the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property, but the same values for the other columns.</span></span> <span data-ttu-id="d3cb9-114">複数の値を持つ複数の列が 1 つの行に含まれている場合 (たとえば、  _それぞれ M_ 値と N 値を持つ 2 つの列)、行の  _M_  _\* N_ インスタンスがテーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-114">If a row contains more than one column with multiple values, for example, two columns with  _M_ and  _N_ values respectively, then  _M\*N_ instances of the row appear in the table.</span></span> 
    
<span data-ttu-id="d3cb9-115">テーブル ユーザーは、複数値列のプロパティの種類で MVI_FLAG フラグが設定された [IMAPITable::SetColumns](imapitable-setcolumns.md) メソッドを呼び出すことによって、既定以外の種類の表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-115">A table user requests the nondefault type of display by calling the [IMAPITable::SetColumns](imapitable-setcolumns.md) method with the MVI_FLAG flag set in the property type of the multivalued column.</span></span> <span data-ttu-id="d3cb9-116">このMVI_FLAGフラグは、論理 OR 操作と MV_FLAGとMV_INSTANCEの組み合わせの結果として定義される **定数** です。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-116">The MVI_FLAG flag is a constant defined as the result of combining the MV_FLAG and MV_INSTANCE flags with a logical **OR** operation.</span></span> <span data-ttu-id="d3cb9-117">**SetColumns** で使用されるだけでなく、MVI_FLAG は _lpSortCriteria_ パラメーターの [IMAPITable::SortTable、lpRestriction](imapitable-sorttable.md)パラメーターの **ulPropTag** メンバーでは [IMAPITable::Restrict](imapitable-restrict.md)にも渡されます。 </span><span class="sxs-lookup"><span data-stu-id="d3cb9-117">In addition to being used in **SetColumns**, MVI_FLAG can also be passed to [IMAPITable::SortTable](imapitable-sorttable.md) in the  _lpSortCriteria_ parameter and [IMAPITable::Restrict](imapitable-restrict.md) in the **ulPropTag** member of the  _lpRestriction_ parameter.</span></span> <span data-ttu-id="d3cb9-118">MVI_FLAG を渡した場合 **、SortTable** は **SetColumns** と同様に実行され、複数値列の値ごとに 1 行を追加し、インスタンス内の 1 つの値で並べ替えを行います。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-118">When passed the MVI_FLAG, **SortTable** performs similarly to **SetColumns**, adding one row for each value in the multivalued column and sorting on the single values in the instances.</span></span> <span data-ttu-id="d3cb9-119">値ごとに 1 つの行が追加されます。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-119">One row is added for each value.</span></span> 
  
 <span data-ttu-id="d3cb9-120">**ただし**、複数値の列を追加の計算行に展開することはできません。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-120">**Restrict**, however, does not expand the multivalued column into additional computed rows.</span></span> <span data-ttu-id="d3cb9-121">複数値を持つ列MVI_FLAG、サービス プロバイダーは、その列を使用してテーブルを制限するように指示します。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-121">A multivalued column with the MVI_FLAG set instructs the service provider to use that column in restricting the table.</span></span> <span data-ttu-id="d3cb9-122">制限にプロパティ値がある場合は、列の [IMAPITable::QueryRows](imapitable-queryrows.md) によって返されるプロパティ タグと同じ 1 つの値プロパティ タグである必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-122">If there is a property value in the restriction, it must be a single value property tag identical to the one that would be returned by [IMAPITable::QueryRows](imapitable-queryrows.md) for the column.</span></span> 
  
<span data-ttu-id="d3cb9-123">テーブルの実装者は、既定の種類の表示をサポートするためにのみ必要であり、呼び出し元が他の選択肢を要求MAPI_E_TOO_COMPLEXの値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-123">Table implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative.</span></span> <span data-ttu-id="d3cb9-124">両方の種類の表示をサポートする機能は、フォルダー コンテンツ テーブルを実装するメッセージ ストア プロバイダーにとって最も重要です。</span><span class="sxs-lookup"><span data-stu-id="d3cb9-124">The ability to support both types of display is most important for message store providers implementing folder contents tables.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d3cb9-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="d3cb9-125">See also</span></span>



[<span data-ttu-id="d3cb9-126">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="d3cb9-126">MAPI Tables</span></span>](mapi-tables.md)

