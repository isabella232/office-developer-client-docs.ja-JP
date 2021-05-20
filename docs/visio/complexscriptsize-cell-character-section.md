---
title: '[ComplexScriptSize] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
localization_priority: Normal
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: 合成テキストの書式設定に使用するフォントのサイズです。
ms.openlocfilehash: 38b01c4a0142c7eca2923ee9b13963eaa1a62830
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428439"
---
# <a name="complexscriptsize-cell-character-section"></a><span data-ttu-id="36e69-103">[ComplexScriptSize] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="36e69-103">ComplexScriptSize Cell (Character Section)</span></span>

<span data-ttu-id="36e69-104">合成テキストの書式設定に使用するフォントのサイズです。</span><span class="sxs-lookup"><span data-stu-id="36e69-104">The size of the font used to format text composed of complex script characters.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="36e69-105">注釈</span><span class="sxs-lookup"><span data-stu-id="36e69-105">Remarks</span></span>

<span data-ttu-id="36e69-106">複雑なスクリプトのフォント サイズは、[テキスト] ダイアログボックスの [フォント] タブに表示されます ([ホーム] タブの [フォント] グループの矢印 **をクリック** します)。 </span><span class="sxs-lookup"><span data-stu-id="36e69-106">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="36e69-107">このリストは、[言語の基本設定] ダイアログ ボックスで、アジア文字または複雑なスクリプト文字を含む言語を追加 **Microsoft Office表示されます**。</span><span class="sxs-lookup"><span data-stu-id="36e69-107">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="36e69-108">([**スタート] ボタン、[** すべてのプログラム **]** の順にクリックし、[Microsoft Office]**をクリック** し、[Microsoft Office **ツール**] をクリックし、[言語の基本設定] Microsoft Office **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="36e69-108">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="36e69-p102">この値には、明示的なポイント サイズまたはパーセントを入力することができます。パーセントを指定した場合、[Size] セルの値を基に値が設定されます。既定値の 0 (ゼロ) は 100% を意味します。</span><span class="sxs-lookup"><span data-stu-id="36e69-p102">You can enter this value as an explicit point size or as a percentage. If you specify a percentage, the value is based on the value in the Size cell. A default value of 0 (zero) means 100%.</span></span> 
  
<span data-ttu-id="36e69-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ComplexScriptSize] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="36e69-112">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36e69-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="36e69-113">Cell name:</span></span>  <br/> |<span data-ttu-id="36e69-114">Char.ComplexScriptSize[ i ]*ここで、i* = <1>、2、3... </span><span class="sxs-lookup"><span data-stu-id="36e69-114">Char.ComplexScriptSize[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="36e69-115">プログラムから、インデックスによって [ComplexScriptSize] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="36e69-115">To get a reference to the ComplexScriptSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36e69-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="36e69-116">Section index:</span></span>  <br/> |<span data-ttu-id="36e69-117">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="36e69-117">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="36e69-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="36e69-118">Row index:</span></span>  <br/> |<span data-ttu-id="36e69-119">**visRowCharacter**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="36e69-119">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="36e69-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="36e69-120">Cell index:</span></span>  <br/> |<span data-ttu-id="36e69-121">**visCharacterComplexScriptSize**</span><span class="sxs-lookup"><span data-stu-id="36e69-121">**visCharacterComplexScriptSize**</span></span> <br/> |
   

