---
title: '[ComplexScriptFont] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
localization_priority: Normal
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: 合成テキストの書式設定に使用するフォントの番号が含まれます。フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。
ms.openlocfilehash: 5ec8deb59b875a01592b6d7b652204089ecf11e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359382"
---
# <a name="complexscriptfont-cell-character-section"></a><span data-ttu-id="0ddd3-104">[ComplexScriptFont] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="0ddd3-104">ComplexScriptFont Cell (Character Section)</span></span>

<span data-ttu-id="0ddd3-p102">合成テキストの書式設定に使用するフォントの番号が含まれます。フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-p102">Contains the number of the font used to format text composed of complex script characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0ddd3-107">解説</span><span class="sxs-lookup"><span data-stu-id="0ddd3-107">Remarks</span></span>

<span data-ttu-id="0ddd3-108">コンプレックススクリプトのフォントサイズは、[**テキスト**] ダイアログボックスの [**フォント**] タブに表示されます ([**ホーム**] タブの [**フォント**] で矢印をクリック)。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-108">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="0ddd3-109">この一覧は、[ **Microsoft Office 言語設定**] ダイアログボックスで、アジアまたはコンプレックススクリプト文字を含む言語を追加した場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="0ddd3-110">([**スタート**]、 **[すべてのプログラム**]、[ **microsoft office**]、[ **microsoft office ツール**]、[ **microsoft office の言語設定**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="0ddd3-111">番号 0 (ゼロ) は、フォントが指定されていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-111">The number 0 (zero) means no font is specified.</span></span> <span data-ttu-id="0ddd3-112">ラテン フォントまたは既定のフォントが使われます。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-112">The Latin font or default fonts are used.</span></span>
  
<span data-ttu-id="0ddd3-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ComplexScriptSize] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-113">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ddd3-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="0ddd3-114">Cell name:</span></span>  <br/> |<span data-ttu-id="0ddd3-115">文字 complexscriptfont [ *i* ] = <1> \*\* 、2、3...</span><span class="sxs-lookup"><span data-stu-id="0ddd3-115">Char.ComplexScriptFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0ddd3-116">プログラムから、インデックスによって [ComplexScriptFont] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0ddd3-116">To get a reference to the ComplexScriptFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ddd3-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0ddd3-117">Section index:</span></span>  <br/> |<span data-ttu-id="0ddd3-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="0ddd3-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="0ddd3-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0ddd3-119">Row index:</span></span>  <br/> |<span data-ttu-id="0ddd3-120">**visRowCharacter** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="0ddd3-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0ddd3-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0ddd3-121">Cell index:</span></span>  <br/> |<span data-ttu-id="0ddd3-122">**visCharacterComplexScriptFont**</span><span class="sxs-lookup"><span data-stu-id="0ddd3-122">**visCharacterComplexScriptFont**</span></span> <br/> |
   

