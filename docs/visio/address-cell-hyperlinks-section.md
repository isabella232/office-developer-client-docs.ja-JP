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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438037"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="d1bc7-103">[Address] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="d1bc7-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="d1bc7-104">移動先の URL アドレス、ファイル名、または UNC パスを指定します。</span><span class="sxs-lookup"><span data-stu-id="d1bc7-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="d1bc7-105">[プロパティ] ダイアログ ボックスの [概要] タブの [ハイパーリンク] ベース ボックスで、ドキュメントに対して定義されている基本パスに基づいて相対パスとしてAddress を指定できます ([ファイル] タブをクリックし、[情報] をクリックし、[\*\* プロパティ \*\*] をクリックし、[高度なプロパティ] をクリックします)。  </span><span class="sxs-lookup"><span data-stu-id="d1bc7-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click \*\* Properties \*\*, and then click **Advanced Properties**).</span></span> <span data-ttu-id="d1bc7-106">図面にベース パスが定義されていない場合は、図面のパスに基づいて移動先が決まります。</span><span class="sxs-lookup"><span data-stu-id="d1bc7-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="d1bc7-107">図面が保存されないと、ハイパーリンクは未定義になります。</span><span class="sxs-lookup"><span data-stu-id="d1bc7-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1bc7-108">注釈</span><span class="sxs-lookup"><span data-stu-id="d1bc7-108">Remarks</span></span>

<span data-ttu-id="d1bc7-109">[Address] セルの値は [**ハイパーリンク**] ダイアログ ボックスでも設定できます (このダイアログ ボックスを表示するには、[**挿入**] タブで [**ハイパーリンク**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="d1bc7-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="d1bc7-110">プログラムから、インデックスによって [Address] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d1bc7-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1bc7-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="d1bc7-111">Cell name:</span></span>  <br/> |<span data-ttu-id="d1bc7-112">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="d1bc7-112">Hyperlink.</span></span> <span data-ttu-id="d1bc7-113">*name*  .ハイパーリンクのアドレス。</span><span class="sxs-lookup"><span data-stu-id="d1bc7-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="d1bc7-114">*name*  はハイパーリンク行の名前です</span><span class="sxs-lookup"><span data-stu-id="d1bc7-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="d1bc7-115">CellsU プロパティを使用して、別の数式またはプログラムから名前によって [アドレス] セルへの参照を **取得** するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d1bc7-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d1bc7-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1bc7-116">Section index:</span></span>  <br/> |<span data-ttu-id="d1bc7-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="d1bc7-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="d1bc7-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1bc7-118">Row index:</span></span>  <br/> |<span data-ttu-id="d1bc7-119">**visRow1stHyperlink**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d1bc7-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d1bc7-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1bc7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d1bc7-121">**visHLinkAddress**</span><span class="sxs-lookup"><span data-stu-id="d1bc7-121">**visHLinkAddress**</span></span> <br/> |
   

