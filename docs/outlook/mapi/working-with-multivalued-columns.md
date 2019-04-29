---
title: 複数値列の処理
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
# <a name="working-with-multivalued-columns"></a><span data-ttu-id="87ca4-103">複数値列の処理</span><span class="sxs-lookup"><span data-stu-id="87ca4-103">Working with Multivalued Columns</span></span>

  
  
<span data-ttu-id="87ca4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87ca4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87ca4-105">複数値列には複数値プロパティのデータが含まれています。これは、単一値の代わりに基本型の値の配列を持つプロパティです。</span><span class="sxs-lookup"><span data-stu-id="87ca4-105">A multivalued column contains the data of a multivalued property, which is a property that has an array of values of the base type instead of a single value.</span></span> <span data-ttu-id="87ca4-106">既定の列セットに複数値プロパティが含まれていないテーブルがあるので、テーブルのユーザーがテーブルを要求した場合にのみ、複数値プロパティがテーブルに含まれます。</span><span class="sxs-lookup"><span data-stu-id="87ca4-106">Because none of the tables include multivalued properties in their default column sets, multivalued properties are included in a table only if the user of the table requests it.</span></span> 
  
<span data-ttu-id="87ca4-107">複数値列をテーブルに表示できます。</span><span class="sxs-lookup"><span data-stu-id="87ca4-107">Multivalued columns can be displayed in tables:</span></span>
  
- <span data-ttu-id="87ca4-108">1つの行で、すべてのプロパティ値が1つの列のインスタンスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="87ca4-108">In a single row, with all of the property values appearing in the single column instance.</span></span> <span data-ttu-id="87ca4-109">これは既定値です。</span><span class="sxs-lookup"><span data-stu-id="87ca4-109">This is the default.</span></span>
    
    - <span data-ttu-id="87ca4-110">や</span><span class="sxs-lookup"><span data-stu-id="87ca4-110">Or -</span></span>
    
- <span data-ttu-id="87ca4-111">一連の行で、各プロパティ値に1つの行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="87ca4-111">In a series of rows, with one row for each of the property values.</span></span> <span data-ttu-id="87ca4-112">それぞれの一意の値は、1つの列にそれぞれの行に表示され、複数値プロパティに値があるとしても行数が多くなります。</span><span class="sxs-lookup"><span data-stu-id="87ca4-112">Each unique value appears in the column in its own row with there being as many rows as there are values in the multivalued property.</span></span> <span data-ttu-id="87ca4-113">各行には、 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティの一意の値がありますが、その他の列には同じ値があります。</span><span class="sxs-lookup"><span data-stu-id="87ca4-113">Each row has a unique value for the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property, but the same values for the other columns.</span></span> <span data-ttu-id="87ca4-114">1つの行に複数の値を持つ複数の列が含まれている場合、たとえば、2つの列にそれぞれ_m_と_N_の値がある場合、テーブルにはその行の_\*M N 個_のインスタンスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="87ca4-114">If a row contains more than one column with multiple values, for example, two columns with  _M_ and  _N_ values respectively, then  _M\*N_ instances of the row appear in the table.</span></span> 
    
<span data-ttu-id="87ca4-115">複数値列のプロパティの種類で、MVI_FLAG フラグを設定して[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出すことにより、table ユーザーが既定以外の種類の表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="87ca4-115">A table user requests the nondefault type of display by calling the [IMAPITable::SetColumns](imapitable-setcolumns.md) method with the MVI_FLAG flag set in the property type of the multivalued column.</span></span> <span data-ttu-id="87ca4-116">MVI_FLAG フラグは、MV_FLAG と MV_INSTANCE のフラグを論理**OR**演算で結合した結果として定義される定数です。</span><span class="sxs-lookup"><span data-stu-id="87ca4-116">The MVI_FLAG flag is a constant defined as the result of combining the MV_FLAG and MV_INSTANCE flags with a logical **OR** operation.</span></span> <span data-ttu-id="87ca4-117">SetColumns で使用されているだけでなく、MVI_FLAG [](imapitable-restrict.md)を\*\*\*\* の_lp:_ : [sorttable](imapitable-sorttable.md)に渡すこともできます。このパラメーターには、 _lpRestriction_の**ulPropTag**メンバーを指定します。parameter.</span><span class="sxs-lookup"><span data-stu-id="87ca4-117">In addition to being used in **SetColumns**, MVI_FLAG can also be passed to [IMAPITable::SortTable](imapitable-sorttable.md) in the  _lpSortCriteria_ parameter and [IMAPITable::Restrict](imapitable-restrict.md) in the **ulPropTag** member of the  _lpRestriction_ parameter.</span></span> <span data-ttu-id="87ca4-118">MVI_FLAG を通過すると、 **sorttable**は**SetColumns**に対して同様に実行し、複数値列の値ごとに1つの行を追加し、インスタンスの単一の値を並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="87ca4-118">When passed the MVI_FLAG, **SortTable** performs similarly to **SetColumns**, adding one row for each value in the multivalued column and sorting on the single values in the instances.</span></span> <span data-ttu-id="87ca4-119">値ごとに1つの行が追加されます。</span><span class="sxs-lookup"><span data-stu-id="87ca4-119">One row is added for each value.</span></span> 
  
 <span data-ttu-id="87ca4-120">ただし、[**制限**] では、複数値列が他の計算行に展開されることはありません。</span><span class="sxs-lookup"><span data-stu-id="87ca4-120">**Restrict**, however, does not expand the multivalued column into additional computed rows.</span></span> <span data-ttu-id="87ca4-121">MVI_FLAG セットを持つ複数値列は、この列を使用してテーブルを制限することをサービスプロバイダーに指示します。</span><span class="sxs-lookup"><span data-stu-id="87ca4-121">A multivalued column with the MVI_FLAG set instructs the service provider to use that column in restricting the table.</span></span> <span data-ttu-id="87ca4-122">制限内にプロパティ値がある場合、その値は、列に対して[IMAPITable:: QueryRows](imapitable-queryrows.md)によって返される1つの値のプロパティタグと同一である必要があります。</span><span class="sxs-lookup"><span data-stu-id="87ca4-122">If there is a property value in the restriction, it must be a single value property tag identical to the one that would be returned by [IMAPITable::QueryRows](imapitable-queryrows.md) for the column.</span></span> 
  
<span data-ttu-id="87ca4-123">表実装者は、既定の種類の表示をサポートするためにのみ必要であり、発信者が他の方法を要求したときに MAPI_E_TOO_COMPLEX 値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="87ca4-123">Table implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative.</span></span> <span data-ttu-id="87ca4-124">両方の種類の表示をサポートする機能は、フォルダーコンテンツテーブルを実装するメッセージストアプロバイダーにとって最も重要です。</span><span class="sxs-lookup"><span data-stu-id="87ca4-124">The ability to support both types of display is most important for message store providers implementing folder contents tables.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="87ca4-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="87ca4-125">See also</span></span>



[<span data-ttu-id="87ca4-126">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="87ca4-126">MAPI Tables</span></span>](mapi-tables.md)

