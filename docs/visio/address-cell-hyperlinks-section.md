---
title: '[Address] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: 移動先の URL アドレス、ファイル名、または UNC パスを指定します。
ms.openlocfilehash: 0fbb89e18a2d7a849e2369c0d41aac4a647f067b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338550"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="671b3-103">[Address] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="671b3-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="671b3-104">移動先の URL アドレス、ファイル名、または UNC パスを指定します。</span><span class="sxs-lookup"><span data-stu-id="671b3-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="671b3-105">Address を相対パスとして指定するには、[**プロパティ**] ダイアログボックスの [ \*\*\*\* **概要**] タブで、[**ファイル**] タブをクリックし、[**情報**] をクリックし、[\* \* Properties \* \*] をクリックします。をクリックし、[**プロパティの詳細**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="671b3-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click \*\* Properties \*\*, and then click **Advanced Properties**).</span></span> <span data-ttu-id="671b3-106">図面にベース パスが定義されていない場合は、図面のパスに基づいて移動先が決まります。</span><span class="sxs-lookup"><span data-stu-id="671b3-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="671b3-107">図面が保存されないと、ハイパーリンクは未定義になります。</span><span class="sxs-lookup"><span data-stu-id="671b3-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="671b3-108">解説</span><span class="sxs-lookup"><span data-stu-id="671b3-108">Remarks</span></span>

<span data-ttu-id="671b3-109">[Address] セルの値は [**ハイパーリンク**] ダイアログ ボックスでも設定できます (このダイアログ ボックスを表示するには、[**挿入**] タブで [**ハイパーリンク**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="671b3-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="671b3-110">プログラムから、インデックスによって [Address] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="671b3-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="671b3-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="671b3-111">Cell name:</span></span>  <br/> |<span data-ttu-id="671b3-112">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="671b3-112">Hyperlink.</span></span> <span data-ttu-id="671b3-113">*名前*です。ハイパーリンクのアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="671b3-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="671b3-114">*name*は、ハイパーリンク行の名前です。</span><span class="sxs-lookup"><span data-stu-id="671b3-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="671b3-115">別の数式または**CellsU**プロパティを使用してプログラムから、名前によって [Address] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="671b3-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="671b3-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="671b3-116">Section index:</span></span>  <br/> |<span data-ttu-id="671b3-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="671b3-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="671b3-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="671b3-118">Row index:</span></span>  <br/> |<span data-ttu-id="671b3-119">**visRow1stHyperlink** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="671b3-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="671b3-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="671b3-120">Cell index:</span></span>  <br/> |<span data-ttu-id="671b3-121">**vishlinkaddress**</span><span class="sxs-lookup"><span data-stu-id="671b3-121">**visHLinkAddress**</span></span> <br/> |
   

