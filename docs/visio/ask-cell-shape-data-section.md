---
title: '[Ask] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
localization_priority: Normal
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: ユーザーが図形のインスタンスを作成したときや、図形を複製またはコピーしたときに、図形データの入力をユーザーに対して問い合わせるかどうかを指定します。
ms.openlocfilehash: 94e84be4bef5c8c13d5c8ef5108ab89b71f251b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804770"
---
# <a name="ask-cell-shape-data-section"></a><span data-ttu-id="d4a0d-103">[Ask] セル ([図形データ] セクション)</span><span class="sxs-lookup"><span data-stu-id="d4a0d-103">Ask Cell (Shape Data Section)</span></span>

<span data-ttu-id="d4a0d-104">ユーザーが図形のインスタンスを作成したときや、図形を複製またはコピーしたときに、図形データの入力をユーザーに対して問い合わせるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d4a0d-104">Determines whether a user is queried to enter shape data for a shape when an instance is created or the shape is duplicated or copied.</span></span>
  
|<span data-ttu-id="d4a0d-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d4a0d-105">**Value**</span></span>|<span data-ttu-id="d4a0d-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="d4a0d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d4a0d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d4a0d-107">TRUE</span></span>  <br/> |<span data-ttu-id="d4a0d-108">
          [**図形データの定義**] ダイアログ ボックスで図形データを入力するようユーザーに求めます。
</span><span class="sxs-lookup"><span data-stu-id="d4a0d-108">Ask user to enter shape data in the **Define Shape Data** dialog box.</span></span>  <br/> |
|<span data-ttu-id="d4a0d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d4a0d-109">FALSE</span></span>  <br/> |<span data-ttu-id="d4a0d-110">
          ユーザーにデータの入力を求めません。
</span><span class="sxs-lookup"><span data-stu-id="d4a0d-110">Do not ask user to enter data.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4a0d-111">注釈</span><span class="sxs-lookup"><span data-stu-id="d4a0d-111">Remarks</span></span>

<span data-ttu-id="d4a0d-112">このセルの値は、[**図形データの定義**] ダイアログ ボックスの [**ドロップ時に確認**] チェック ボックスに対応しています (このダイアログ ボックスを開くには、図形を右クリックし、[**データ**] をポイントして、[**図形データの定義**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="d4a0d-112">The value in this cell corresponds to the **Ask on drop** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="d4a0d-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Ask] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4a0d-113">To get a reference to the Ask cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4a0d-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="d4a0d-114">Cell name:</span></span>  <br/> |<span data-ttu-id="d4a0d-115">プロペラです。*名*です。確認して、プロペラします。 *名前*は、カスタム プロパティ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="d4a0d-115">Prop. *name*  .Verify            where Prop.  *name*  is the name of the custom property row.</span></span>  <br/> |
   
<span data-ttu-id="d4a0d-116">プログラムから、インデックスによって [Ask] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d4a0d-116">To get a reference to the Ask cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4a0d-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4a0d-117">Section index:</span></span>  <br/> |<span data-ttu-id="d4a0d-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="d4a0d-118">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="d4a0d-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4a0d-119">Row index:</span></span>  <br/> |<span data-ttu-id="d4a0d-120">**visRowProp** +  *i* 、 *i* = 0、1、2、.</span><span class="sxs-lookup"><span data-stu-id="d4a0d-120">**visRowProp** +  *i*            where  *i*  = 0, 1, 2,...</span></span>  <br/> |
|<span data-ttu-id="d4a0d-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4a0d-121">Cell index:</span></span>  <br/> |<span data-ttu-id="d4a0d-122">**visCustPropsAsk**</span><span class="sxs-lookup"><span data-stu-id="d4a0d-122">**visCustPropsAsk**</span></span> <br/> |
   

