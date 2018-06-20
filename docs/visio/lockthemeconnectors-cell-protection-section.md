---
title: '[LockThemeConnectors] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: ConnectorsSchemeIndex、テーマのプロパティの行のセルが、新しいテーマを適用するか、新しいコネクタの設定を選択すると変更するを防ぎます。 でも、ユーザーからシェイプ シート内でこの値を手動で編集します。
ms.openlocfilehash: c74bcf554f0f14de47480397a96680469826d2c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805778"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="af03a-104">[LockThemeConnectors] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="af03a-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="af03a-105">**ConnectorsSchemeIndex** **テーマのプロパティ**の行のセルが、新しいテーマを適用するか、新しいコネクタの設定を選択すると変更するを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="af03a-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="af03a-106">でも、ユーザーからシェイプ シート内でこの値を手動で編集します。</span><span class="sxs-lookup"><span data-stu-id="af03a-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="af03a-107">**値**</span><span class="sxs-lookup"><span data-stu-id="af03a-107">**Value**</span></span>|<span data-ttu-id="af03a-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="af03a-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af03a-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="af03a-109">TRUE</span></span>  <br/> |<span data-ttu-id="af03a-110">シェイプ シートで直接変更しない限り、現在の値から**ConnectorsSchemeIndex**のセルを変更できません。</span><span class="sxs-lookup"><span data-stu-id="af03a-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="af03a-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="af03a-111">FALSE</span></span>  <br/> |<span data-ttu-id="af03a-112">**ConnectorsSchemeIndex**セルは、ui の現在の値から変更できます。</span><span class="sxs-lookup"><span data-stu-id="af03a-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af03a-113">備考</span><span class="sxs-lookup"><span data-stu-id="af03a-113">Remarks</span></span>

<span data-ttu-id="af03a-114">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **LockThemeConnectors** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="af03a-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af03a-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="af03a-115">Cell name:</span></span>  <br/> | <span data-ttu-id="af03a-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="af03a-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="af03a-117">プログラムから、インデックスによって [ **LockThemeConnectors** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="af03a-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af03a-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="af03a-118">Section index:</span></span>  <br/> |<span data-ttu-id="af03a-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="af03a-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="af03a-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="af03a-120">Row index:</span></span>  <br/> |<span data-ttu-id="af03a-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="af03a-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="af03a-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="af03a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="af03a-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="af03a-123">**visLockThemeConnectors**</span></span> <br/> |
   

