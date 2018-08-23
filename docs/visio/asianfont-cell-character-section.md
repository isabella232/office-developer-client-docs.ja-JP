---
title: '[AsianFont] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
localization_priority: Normal
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: アジア系文字を含むテキストの書式設定に使用するフォントの番号が含まれます。フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。
ms.openlocfilehash: 1fbaa0b27a0c639519c302129142dcefe5708115
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804778"
---
# <a name="asianfont-cell-character-section"></a><span data-ttu-id="31da1-104">[AsianFont] セル ([文字] セクション)</span><span class="sxs-lookup"><span data-stu-id="31da1-104">AsianFont Cell (Character Section)</span></span>

<span data-ttu-id="31da1-p102">アジア系文字を含むテキストの書式設定に使用するフォントの番号が含まれます。フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。</span><span class="sxs-lookup"><span data-stu-id="31da1-p102">Contains the number of the font used to format the text containing Asian characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="31da1-107">注釈</span><span class="sxs-lookup"><span data-stu-id="31da1-107">Remarks</span></span>

<span data-ttu-id="31da1-p103">アジア系フォントの一覧は、[**テキスト**] ダイアログ ボックスの [**フォント**] タブにあります (このタブを開くには、[**ホーム**] タブの [**フォント**] グループの矢印をクリックします)。この一覧が表示されるのは、[**Microsoft Office 言語設定**] ダイアログ ボックスにアジア系の文字または合成テキストが含まれている言語を追加した場合だけです (このダイアログ ボックスを開くには、[**スタート**] ボタンをクリックし、[**すべてのプログラム**]、[**Microsoft Office**]、[**Microsoft Office ツール**]、[**Microsoft Office 言語設定**] の順にクリックします)。</span><span class="sxs-lookup"><span data-stu-id="31da1-p103">Asian fonts are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab). This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box. (Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="31da1-p104">番号 0 は、フォントが指定されていないことを意味します。ラテン フォントまたは既定値のフォントが必要な文字を含む場合はそれが使用されます。</span><span class="sxs-lookup"><span data-stu-id="31da1-p104">The number 0 means no font is specified. The Latin font or default fonts are used if they contain the necessary characters.</span></span>
  
<span data-ttu-id="31da1-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AsianFont] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="31da1-113">To get a reference to the AsianFont cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31da1-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="31da1-114">Cell name:</span></span>  <br/> |<span data-ttu-id="31da1-115">Char.AsianFont [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="31da1-115">Char.AsianFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="31da1-116">プログラムから、インデックスによって [AsianFont] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="31da1-116">To get a reference to the AsianFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31da1-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="31da1-117">Section index:</span></span>  <br/> |<span data-ttu-id="31da1-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="31da1-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="31da1-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="31da1-119">Row index:</span></span>  <br/> |<span data-ttu-id="31da1-120">**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="31da1-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="31da1-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="31da1-121">Cell index:</span></span>  <br/> |<span data-ttu-id="31da1-122">**visCharacterAsianFont**</span><span class="sxs-lookup"><span data-stu-id="31da1-122">**visCharacterAsianFont**</span></span> <br/> |
   

