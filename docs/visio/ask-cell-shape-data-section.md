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
ms.openlocfilehash: 0aa270ff918866d8f683a6408ccd71b6a22d555d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341441"
---
# <a name="ask-cell-shape-data-section"></a><span data-ttu-id="4ccba-103">[Ask] セル ([Shape Data] セクション)</span><span class="sxs-lookup"><span data-stu-id="4ccba-103">Ask Cell (Shape Data Section)</span></span>

<span data-ttu-id="4ccba-104">ユーザーが図形のインスタンスを作成したときや、図形を複製またはコピーしたときに、図形データの入力をユーザーに対して問い合わせるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="4ccba-104">Determines whether a user is queried to enter shape data for a shape when an instance is created or the shape is duplicated or copied.</span></span>
  
|<span data-ttu-id="4ccba-105">**値**</span><span class="sxs-lookup"><span data-stu-id="4ccba-105">**Value**</span></span>|<span data-ttu-id="4ccba-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="4ccba-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ccba-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4ccba-107">TRUE</span></span>  <br/> |<span data-ttu-id="4ccba-108">[**図形データの定義**] ダイアログ ボックスで図形データを入力するようユーザーに求めます。</span><span class="sxs-lookup"><span data-stu-id="4ccba-108">Ask user to enter shape data in the **Define Shape Data** dialog box.</span></span>  <br/> |
|<span data-ttu-id="4ccba-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4ccba-109">FALSE</span></span>  <br/> |<span data-ttu-id="4ccba-110">ユーザーにデータの入力を求めません。</span><span class="sxs-lookup"><span data-stu-id="4ccba-110">Do not ask user to enter data.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ccba-111">解説</span><span class="sxs-lookup"><span data-stu-id="4ccba-111">Remarks</span></span>

<span data-ttu-id="4ccba-112">このセルの値は、[**図形データの定義**] ダイアログ ボックスの [**ドロップ時に確認**] チェック ボックスに対応しています (このダイアログ ボックスを開くには、図形を右クリックし、[**データ**] をポイントして、[**図形データの定義**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="4ccba-112">The value in this cell corresponds to the **Ask on drop** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="4ccba-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Ask] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4ccba-113">To get a reference to the Ask cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ccba-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="4ccba-114">Cell name:</span></span>  <br/> |<span data-ttu-id="4ccba-115">提案.*名前*です。Prop がどこにあるかを確認します。 *name*は、カスタムプロパティ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="4ccba-115">Prop. *name*  .Verify            where Prop.  *name*  is the name of the custom property row.</span></span>  <br/> |
   
<span data-ttu-id="4ccba-116">プログラムから、インデックスによって [Ask] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ccba-116">To get a reference to the Ask cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ccba-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4ccba-117">Section index:</span></span>  <br/> |<span data-ttu-id="4ccba-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="4ccba-118">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="4ccba-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4ccba-119">Row index:</span></span>  <br/> |<span data-ttu-id="4ccba-120">**visRowProp** +  *i* = \*\* 0、1、2,...</span><span class="sxs-lookup"><span data-stu-id="4ccba-120">**visRowProp** +  *i*            where  *i*  = 0, 1, 2,...</span></span>  <br/> |
|<span data-ttu-id="4ccba-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4ccba-121">Cell index:</span></span>  <br/> |<span data-ttu-id="4ccba-122">**viscustpropsask**</span><span class="sxs-lookup"><span data-stu-id="4ccba-122">**visCustPropsAsk**</span></span> <br/> |
   

