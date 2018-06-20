---
title: 複数値を持つ列の使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ee3307836e8b167efbc2cdc870e698257526ef97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804243"
---
# <a name="working-with-multivalued-columns"></a><span data-ttu-id="ce38e-103">複数値を持つ列の使用</span><span class="sxs-lookup"><span data-stu-id="ce38e-103">Working with Multivalued Columns</span></span>

  
  
<span data-ttu-id="ce38e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce38e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ce38e-105">複数値の列には、1 つの値ではなく基本データ型の値の配列を含むプロパティは、複数値を持つプロパティのデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ce38e-105">A multivalued column contains the data of a multivalued property, which is a property that has an array of values of the base type instead of a single value.</span></span> <span data-ttu-id="ce38e-106">テーブルの [なし] は、複数値を持つプロパティの既定の列セットであるため、テーブルのユーザーが要求した場合のみ複数値を持つプロパティがテーブルに含まれます。</span><span class="sxs-lookup"><span data-stu-id="ce38e-106">Because none of the tables include multivalued properties in their default column sets, multivalued properties are included in a table only if the user of the table requests it.</span></span> 
  
<span data-ttu-id="ce38e-107">複数値を持つ列は、テーブルに表示できます。</span><span class="sxs-lookup"><span data-stu-id="ce38e-107">Multivalued columns can be displayed in tables:</span></span>
  
- <span data-ttu-id="ce38e-108">1 つの行、列の 1 つのインスタンスに表示されるプロパティ値のすべてです。</span><span class="sxs-lookup"><span data-stu-id="ce38e-108">In a single row, with all of the property values appearing in the single column instance.</span></span> <span data-ttu-id="ce38e-109">これは、既定値です。</span><span class="sxs-lookup"><span data-stu-id="ce38e-109">This is the default.</span></span>
    
    - <span data-ttu-id="ce38e-110">または、</span><span class="sxs-lookup"><span data-stu-id="ce38e-110">Or -</span></span>
    
- <span data-ttu-id="ce38e-111">一連の行のプロパティ値ごとに 1 行にします。</span><span class="sxs-lookup"><span data-stu-id="ce38e-111">In a series of rows, with one row for each of the property values.</span></span> <span data-ttu-id="ce38e-112">そこに多数の行は、複数値を持つプロパティの値とする、そこに独自の行の列にそれぞれ一意の値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce38e-112">Each unique value appears in the column in its own row with there being as many rows as there are values in the multivalued property.</span></span> <span data-ttu-id="ce38e-113">各行では、 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティでは、一意の値ですが、ほかの列と同じ値を持ちます。</span><span class="sxs-lookup"><span data-stu-id="ce38e-113">Each row has a unique value for the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property, but the same values for the other columns.</span></span> <span data-ttu-id="ce38e-114">行に複数値を持つ 2 つ以上の列が含まれている場合たとえば、 _M_と_N_の 2 つの列それぞれ値は、[ _M\*N_テーブルの行のインスタンスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce38e-114">If a row contains more than one column with multiple values, for example, two columns with  _M_ and  _N_ values respectively, then  _M\*N_ instances of the row appear in the table.</span></span> 
    
<span data-ttu-id="ce38e-115">テーブルのユーザーは、メソッドを呼び出して、 [IMAPITable::SetColumns](imapitable-setcolumns.md) MVI_FLAG フラグが設定されている複数値の列のプロパティの型での表示の既定値以外の種類を要求します。</span><span class="sxs-lookup"><span data-stu-id="ce38e-115">A table user requests the nondefault type of display by calling the [IMAPITable::SetColumns](imapitable-setcolumns.md) method with the MVI_FLAG flag set in the property type of the multivalued column.</span></span> <span data-ttu-id="ce38e-116">MVI_FLAG フラグは、論理**OR**演算と MV_FLAG と MV_INSTANCE のフラグを組み合わせることの結果として定義されている定数です。</span><span class="sxs-lookup"><span data-stu-id="ce38e-116">The MVI_FLAG flag is a constant defined as the result of combining the MV_FLAG and MV_INSTANCE flags with a logical **OR** operation.</span></span> <span data-ttu-id="ce38e-117">**SetColumns**で使用されているだけでなく MVI_FLAG 渡すこともできます[IMAPITable::SortTable](imapitable-sorttable.md)に、 _lpSortCriteria_パラメーターと[IMAPITable::Restrict](imapitable-restrict.md)の_lpRestriction_の**ulPropTag**のメンバーでパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="ce38e-117">In addition to being used in **SetColumns**, MVI_FLAG can also be passed to [IMAPITable::SortTable](imapitable-sorttable.md) in the  _lpSortCriteria_ parameter and [IMAPITable::Restrict](imapitable-restrict.md) in the **ulPropTag** member of the  _lpRestriction_ parameter.</span></span> <span data-ttu-id="ce38e-118">渡されると、MVI_FLAG、 **SortTable**は**SetColumns**、複数値を持つ列の値ごとに 1 つの行を追加して、インスタンス内の単一の値で並べ替えを同様に実行します。</span><span class="sxs-lookup"><span data-stu-id="ce38e-118">When passed the MVI_FLAG, **SortTable** performs similarly to **SetColumns**, adding one row for each value in the multivalued column and sorting on the single values in the instances.</span></span> <span data-ttu-id="ce38e-119">値ごとに 1 つの行が追加されます。</span><span class="sxs-lookup"><span data-stu-id="ce38e-119">One row is added for each value.</span></span> 
  
 <span data-ttu-id="ce38e-120">**だけに制限する**、ただし、展開されない複数値を持つ列計算行にします。</span><span class="sxs-lookup"><span data-stu-id="ce38e-120">**Restrict**, however, does not expand the multivalued column into additional computed rows.</span></span> <span data-ttu-id="ce38e-121">MVI_FLAG セットを使用して複数値を持つ列は、テーブルを制限することでその列を使用するサービス プロバイダーに指示します。</span><span class="sxs-lookup"><span data-stu-id="ce38e-121">A multivalued column with the MVI_FLAG set instructs the service provider to use that column in restricting the table.</span></span> <span data-ttu-id="ce38e-122">制約のプロパティの値がある場合と同じように列の[IMAPITable::QueryRows](imapitable-queryrows.md)によって返される単一値プロパティ タグがあります。</span><span class="sxs-lookup"><span data-stu-id="ce38e-122">If there is a property value in the restriction, it must be a single value property tag identical to the one that would be returned by [IMAPITable::QueryRows](imapitable-queryrows.md) for the column.</span></span> 
  
<span data-ttu-id="ce38e-123">テーブルの実装側では、既定の表示の種類をサポートするために必要なだけと、呼び出し元が他の選択を要求すると、MAPI_E_TOO_COMPLEX の値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="ce38e-123">Table implementers are only required to support the default type of display and can return the MAPI_E_TOO_COMPLEX value when a caller requests the other alternative.</span></span> <span data-ttu-id="ce38e-124">両方の種類の表示をサポートする機能は、メッセージ ストア プロバイダーがフォルダーの内容テーブルを実装するために最も重要です。</span><span class="sxs-lookup"><span data-stu-id="ce38e-124">The ability to support both types of display is most important for message store providers implementing folder contents tables.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ce38e-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="ce38e-125">See also</span></span>



[<span data-ttu-id="ce38e-126">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="ce38e-126">MAPI Tables</span></span>](mapi-tables.md)

