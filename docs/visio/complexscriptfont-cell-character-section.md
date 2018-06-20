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
ms.openlocfilehash: 0aae3a22be26f206763f18107eaced74f1078503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805057"
---
# <a name="complexscriptfont-cell-character-section"></a><span data-ttu-id="7c214-104">[ComplexScriptFont] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="7c214-104">ComplexScriptFont Cell (Character Section)</span></span>

<span data-ttu-id="7c214-p102">合成テキストの書式設定に使用するフォントの番号が含まれます。フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。</span><span class="sxs-lookup"><span data-stu-id="7c214-p102">Contains the number of the font used to format text composed of complex script characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7c214-107">注釈</span><span class="sxs-lookup"><span data-stu-id="7c214-107">Remarks</span></span>

<span data-ttu-id="7c214-108">コンプレックス スクリプトのフォントのサイズは、[**テキスト**] ダイアログ ボックス ([**ホーム**] タブの**フォント**にある矢印をグループ化] をクリック) の [**フォント**] タブに一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="7c214-108">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="7c214-109">このリストは、 **Microsoft Office 言語設定**] ダイアログ ボックスで、アジア言語や複雑なスクリプトの文字を含む言語を追加した場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="7c214-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="7c214-110">([**スタート**] ボタン [**すべてのプログラム**] をクリックして、 **Microsoft Office**、 **Microsoft Office ツール**] をクリックして、 **Microsoft Office 言語設定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c214-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="7c214-111">番号 0 (ゼロ) では、フォントが指定されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="7c214-111">The number 0 (zero) means no font is specified.</span></span> <span data-ttu-id="7c214-112">ラテン フォントまたは既定のフォントが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7c214-112">The Latin font or default fonts are used.</span></span>
  
<span data-ttu-id="7c214-113">取得する、[ComplexScriptSize] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="7c214-113">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c214-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="7c214-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7c214-115">Char.ComplexScriptFont [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="7c214-115">Char.ComplexScriptFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7c214-116">プログラムから、インデックスによって [ComplexScriptFont] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7c214-116">To get a reference to the ComplexScriptFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c214-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7c214-117">Section index:</span></span>  <br/> |<span data-ttu-id="7c214-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="7c214-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="7c214-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7c214-119">Row index:</span></span>  <br/> |<span data-ttu-id="7c214-120">**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="7c214-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7c214-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7c214-121">Cell index:</span></span>  <br/> |<span data-ttu-id="7c214-122">**visCharacterComplexScriptFont**</span><span class="sxs-lookup"><span data-stu-id="7c214-122">**visCharacterComplexScriptFont**</span></span> <br/> |
   

