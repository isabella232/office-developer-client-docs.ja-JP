---
title: 表示テーブルと関連する構造体の作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 350272324c3827f4630f0cf35e3ade0ff213ac4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416245"
---
# <a name="creating-display-tables-and-related-structures"></a><span data-ttu-id="d64fc-103">表示テーブルと関連する構造体の作成</span><span class="sxs-lookup"><span data-stu-id="d64fc-103">Creating display tables and related structures</span></span>
  
<span data-ttu-id="d64fc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d64fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d64fc-105">表示テーブルの作成は、スクリプト言語を使用したプログラムの作成に似ています。</span><span class="sxs-lookup"><span data-stu-id="d64fc-105">Creating a display table is similar to writing a program with a scripting language.</span></span> <span data-ttu-id="d64fc-106">表示テーブルを作成するには [、BuildDisplayTable](builddisplaytable.md) を呼び出すか、カスタム コードを記述してテーブルの行と列を設定します。</span><span class="sxs-lookup"><span data-stu-id="d64fc-106">You can create a display table either by calling [BuildDisplayTable](builddisplaytable.md) or writing custom code to populate the rows and columns of the table.</span></span> <span data-ttu-id="d64fc-107">一般に **、BuildDisplayTable** の手法は、より簡単なので使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d64fc-107">In general, you should use the **BuildDisplayTable** technique because it is simpler.</span></span> 
  
<span data-ttu-id="d64fc-108">**BuildDisplayTable** を呼び出して MAPI に表示テーブルの作成を求める前に、構築する必要がある構造の階層があります。</span><span class="sxs-lookup"><span data-stu-id="d64fc-108">Before you can call **BuildDisplayTable** to prompt MAPI to create a display table, there is a hierarchy of structures that you must build.</span></span> <span data-ttu-id="d64fc-109">トップ レベルの構造 [DTPAGE は](dtpage.md)、単一のタブ付きプロパティ ページを表します。</span><span class="sxs-lookup"><span data-stu-id="d64fc-109">The top-level structure, [DTPAGE](dtpage.md), describes a single tabbed property page.</span></span> <span data-ttu-id="d64fc-110">すべての **DTPAGE 構造** では、編集ボックスやオプション ボタンなど、1 つのコントロールを記述する [DTCTL](dtctl.md) 構造です。</span><span class="sxs-lookup"><span data-stu-id="d64fc-110">In every **DTPAGE** structure is a [DTCTL](dtctl.md) structure that describes a single control, such as an edit box or an option button.</span></span> <span data-ttu-id="d64fc-111">各 **DTCTL** 構造には、コントロールの種類に固有の構造が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d64fc-111">Each **DTCTL** structure contains a structure that is specific to the type of control.</span></span> <span data-ttu-id="d64fc-112">たとえば **、DTCTL 構造体に編集** ボックス コントロールが記述されている場合 **、DTBLEDIT 構造が含まれるとします** 。</span><span class="sxs-lookup"><span data-stu-id="d64fc-112">For example, if the **DTCTL** structure describes an edit box control, it will contain a **DTBLEDIT** structure.</span></span> <span data-ttu-id="d64fc-113">オプション **ボタンの DTCTL** 構造には **、DTBLRADIOBUTTON 構造が含** まれる。</span><span class="sxs-lookup"><span data-stu-id="d64fc-113">The **DTCTL** structure for an option button contains a **DTBLRADIOBUTTON** structure.</span></span> 
  
<span data-ttu-id="d64fc-114">これらの構造体は **、BuildDisplayTable に直接関連しています**。この関数のコンテキストの外側には意味はありません。</span><span class="sxs-lookup"><span data-stu-id="d64fc-114">These structures relate directly to **BuildDisplayTable**; they have no meaning outside the context of this function.</span></span> <span data-ttu-id="d64fc-115">**BuildDisplayTable を呼び出す場合** は、1 つ以上の **DTPAGE** 構造体を入力パラメーターとして渡します。</span><span class="sxs-lookup"><span data-stu-id="d64fc-115">When you call **BuildDisplayTable**, you pass one or more **DTPAGE** structures as input parameters.</span></span> <span data-ttu-id="d64fc-116">**DTPAGE 構造体には\*\*\*\*、DTCTL** 構造体の配列と、配列内の **DTCTL** 構造体の数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d64fc-116">The **DTPAGE** structures contain an array of **DTCTL** structures and a count of the number of **DTCTL** structures in the array.</span></span> <span data-ttu-id="d64fc-117">ダイアログ ボックスに表示するコントロールごとに 1 つの構造があります。</span><span class="sxs-lookup"><span data-stu-id="d64fc-117">There is one structure for every control to display in the dialog box.</span></span> <span data-ttu-id="d64fc-118">**DTPAGE** 構造体には、対応するヘルプ ファイルとダイアログ ボックス リソースの名前を表す文字列も含まれています。</span><span class="sxs-lookup"><span data-stu-id="d64fc-118">**DTPAGE** structures also have a character string that represents the name of a corresponding Help file and dialog box resource.</span></span> 
  
<span data-ttu-id="d64fc-119">DTPAGE **構造体内** の **各 DTCTL** 構造には、コントロールのプロパティを設定するために使用される次のデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d64fc-119">Each **DTCTL** structure in a **DTPAGE** structure contains the following data that is used to set properties for the control:</span></span> 
  
- <span data-ttu-id="d64fc-120">コントロールの種類 ([PidTagControlType](pidtagcontroltype-canonical-property.md) **)** PR_CONTROL_TYPE設定するコントロールの種類です。</span><span class="sxs-lookup"><span data-stu-id="d64fc-120">The control type for setting **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)).</span></span>
    
- <span data-ttu-id="d64fc-121">[(PidTagControlFlags)](pidtagcontrolflags-canonical-property.md)PR_CONTROL_FLAGS設定のコントロール フラグ。 </span><span class="sxs-lookup"><span data-stu-id="d64fc-121">Control flags for setting **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).</span></span>
    
- <span data-ttu-id="d64fc-122">設定の通知データ [(PidTagControlId](pidtagcontrolid-canonical-property.md) **PR_CONTROL_ID)**</span><span class="sxs-lookup"><span data-stu-id="d64fc-122">Notification data for setting **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)).</span></span>
    
- <span data-ttu-id="d64fc-123">プロパティ ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) を **PR_CONTROL_STRUCTURE** コントロール構造。</span><span class="sxs-lookup"><span data-stu-id="d64fc-123">The control structure for setting **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).</span></span>
    
<span data-ttu-id="d64fc-124">**DTCTL 構造体** には、リソース識別子と、編集およびコンボ ボックス コントロールの文字フィルターも含まれます。</span><span class="sxs-lookup"><span data-stu-id="d64fc-124">**DTCTL** structures also contain a resource identifier and, for edit and combo box controls, a character filter.</span></span> 
  
<span data-ttu-id="d64fc-125">**DTCTL** 構造体のコントロール構造メンバーは、コントロールの種類に固有のデータを記述します。</span><span class="sxs-lookup"><span data-stu-id="d64fc-125">The control structure member of a **DTCTL** structure describes the data that is unique for the type of control.</span></span> <span data-ttu-id="d64fc-126">MAPI は、コントロールの種類ごとに異なる構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="d64fc-126">MAPI defines a different structure for each control type.</span></span> <span data-ttu-id="d64fc-127">たとえば、編集コントロールのデータは **DTBLEDIT 構造で表** されます。リスト ボックスのデータは **DTBLLBX 構造で表** されます。</span><span class="sxs-lookup"><span data-stu-id="d64fc-127">For example, the data of an edit control is represented by a **DTBLEDIT** structure; the data of a list box is represented by a **DTBLLBX** structure.</span></span> 
  
<span data-ttu-id="d64fc-128">次の図に、3 種類の表示テーブル構造の関係を示します。</span><span class="sxs-lookup"><span data-stu-id="d64fc-128">The relationship between the three types of display table structures is shown in the following illustration.</span></span> <span data-ttu-id="d64fc-129">この表示テーブルで説明するダイアログ ボックスには、ラベルと編集コントロールの 2 つのコントロールがあります。</span><span class="sxs-lookup"><span data-stu-id="d64fc-129">The dialog box described by this display table has two controls: a label and an edit control.</span></span> <span data-ttu-id="d64fc-130">**DTBLLBX** 構造体には、ラベルの文字列の開始位置を示す、いくつかのコントロール構造と同様に、ラベル オフセット メンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="d64fc-130">The **DTBLLBX** structure has a label offset member, as do several of the control structures, that describes where the character string for the label begins.</span></span> <span data-ttu-id="d64fc-131">ラベル文字列は、通常、構造体の直後にメモリに配置されます。</span><span class="sxs-lookup"><span data-stu-id="d64fc-131">Label character strings are typically placed in memory immediately following the structure.</span></span> 
  
<span data-ttu-id="d64fc-132">**表示テーブルの構造**</span><span class="sxs-lookup"><span data-stu-id="d64fc-132">**Display table structures**</span></span>
  
<span data-ttu-id="d64fc-133">![表示テーブル構造](media/dtstruct.gif "テーブル構造の表示")</span><span class="sxs-lookup"><span data-stu-id="d64fc-133">![Display table structures](media/dtstruct.gif "Display table structures")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d64fc-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="d64fc-134">See also</span></span>

- [<span data-ttu-id="d64fc-135">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="d64fc-135">Display table implementation</span></span>](display-table-implementation.md)

