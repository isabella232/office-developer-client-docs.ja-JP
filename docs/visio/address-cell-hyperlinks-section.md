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
ms.openlocfilehash: 840ce0c4ce73da378f80e5d8a185073ac3915daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804780"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="9c584-103">[Address] セル ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="9c584-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="9c584-104">移動先の URL アドレス、ファイル名、または UNC パスを指定します。</span><span class="sxs-lookup"><span data-stu-id="9c584-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="9c584-105">[**プロパティ**] ダイアログ ボックスの [**ハイパーリンクの基点**] ボックス [**概要**] タブでドキュメントに定義された基本パスに基づく相対パスとしてアドレスを指定することができます ([**ファイル**] タブをクリックして、[**情報**] をクリックして、をクリックして * * プロパティ * *、、[**詳細プロパティ**] をクリックし、)。</span><span class="sxs-lookup"><span data-stu-id="9c584-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click ** Properties **, and then click **Advanced Properties**).</span></span> <span data-ttu-id="9c584-106">ドキュメントには、基本パスがなければ、アプリケーションは、文書へのパスに基づいて移動します。</span><span class="sxs-lookup"><span data-stu-id="9c584-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="9c584-107">ドキュメントが保存されていない場合、ハイパーリンクは未定義です。</span><span class="sxs-lookup"><span data-stu-id="9c584-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9c584-108">備考</span><span class="sxs-lookup"><span data-stu-id="9c584-108">Remarks</span></span>

<span data-ttu-id="9c584-109">**[ハイパーリンク**] ダイアログ ボックスで、[Address] セルの値を設定することもできます ([**挿入**] タブで**ハイパーリンク**をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="9c584-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="9c584-110">プログラムから、インデックスによって [Address] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9c584-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c584-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="9c584-111">Cell name:</span></span>  <br/> |<span data-ttu-id="9c584-112">ハイパーリンク</span><span class="sxs-lookup"><span data-stu-id="9c584-112">Hyperlink.</span></span> <span data-ttu-id="9c584-113">*名*です。場所のアドレスのハイパーリンクです。</span><span class="sxs-lookup"><span data-stu-id="9c584-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="9c584-114">*ハイパーリンク行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="9c584-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="9c584-115">取得する、[Address] セルへの参照を名前で別の数式からまたはプログラムでは、 **CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="9c584-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c584-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9c584-116">Section index:</span></span>  <br/> |<span data-ttu-id="9c584-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="9c584-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="9c584-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9c584-118">Row index:</span></span>  <br/> |<span data-ttu-id="9c584-119">**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="9c584-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9c584-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9c584-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9c584-121">**visHLinkAddress**</span><span class="sxs-lookup"><span data-stu-id="9c584-121">**visHLinkAddress**</span></span> <br/> |
   

