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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335615"
---
# <a name="creating-display-tables-and-related-structures"></a><span data-ttu-id="06b36-103">表示テーブルと関連する構造体の作成</span><span class="sxs-lookup"><span data-stu-id="06b36-103">Creating display tables and related structures</span></span>
  
<span data-ttu-id="06b36-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06b36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06b36-105">表示テーブルの作成は、スクリプト言語を使用してプログラムを記述するのと似ています。</span><span class="sxs-lookup"><span data-stu-id="06b36-105">Creating a display table is similar to writing a program with a scripting language.</span></span> <span data-ttu-id="06b36-106">表示テーブルを作成するには、 [builddisplaytable](builddisplaytable.md)を呼び出すか、カスタムコードを記述して、テーブルの行と列にデータを設定します。</span><span class="sxs-lookup"><span data-stu-id="06b36-106">You can create a display table either by calling [BuildDisplayTable](builddisplaytable.md) or writing custom code to populate the rows and columns of the table.</span></span> <span data-ttu-id="06b36-107">一般に、 **builddisplaytable**手法はより単純なので、使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06b36-107">In general, you should use the **BuildDisplayTable** technique because it is simpler.</span></span> 
  
<span data-ttu-id="06b36-108">**builddisplaytable**を呼び出して MAPI に表示テーブルを作成するようにするには、まず構造の階層構造を構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06b36-108">Before you can call **BuildDisplayTable** to prompt MAPI to create a display table, there is a hierarchy of structures that you must build.</span></span> <span data-ttu-id="06b36-109">トップレベルの構造である[dtpage](dtpage.md)は、1つのタブ付きプロパティページを記述します。</span><span class="sxs-lookup"><span data-stu-id="06b36-109">The top-level structure, [DTPAGE](dtpage.md), describes a single tabbed property page.</span></span> <span data-ttu-id="06b36-110">**dtpage**のすべての構造体は、編集ボックスやオプションボタンなどの1つのコントロールを記述する[DTCTL](dtctl.md)構造体です。</span><span class="sxs-lookup"><span data-stu-id="06b36-110">In every **DTPAGE** structure is a [DTCTL](dtctl.md) structure that describes a single control, such as an edit box or an option button.</span></span> <span data-ttu-id="06b36-111">各**DTCTL**構造体には、コントロールの種類に固有の構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06b36-111">Each **DTCTL** structure contains a structure that is specific to the type of control.</span></span> <span data-ttu-id="06b36-112">たとえば、 **DTCTL**構造体には、編集ボックスコントロールが記述されている場合、 **DTBLEDIT**構造体が含まれます。</span><span class="sxs-lookup"><span data-stu-id="06b36-112">For example, if the **DTCTL** structure describes an edit box control, it will contain a **DTBLEDIT** structure.</span></span> <span data-ttu-id="06b36-113">オプションボタンの**DTCTL**構造体には、 **dtblradiobutton**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06b36-113">The **DTCTL** structure for an option button contains a **DTBLRADIOBUTTON** structure.</span></span> 
  
<span data-ttu-id="06b36-114">これらの構造は、直接**builddisplaytable**に関連しています。この関数のコンテキストの外部では意味がありません。</span><span class="sxs-lookup"><span data-stu-id="06b36-114">These structures relate directly to **BuildDisplayTable**; they have no meaning outside the context of this function.</span></span> <span data-ttu-id="06b36-115">**builddisplaytable**を呼び出す場合は、1つ以上の**dtpage**構造を入力パラメーターとして渡します。</span><span class="sxs-lookup"><span data-stu-id="06b36-115">When you call **BuildDisplayTable**, you pass one or more **DTPAGE** structures as input parameters.</span></span> <span data-ttu-id="06b36-116">**dtpage**構造体には、 **DTCTL**構造体の配列と、配列内の**DTCTL**構造体の数のカウントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="06b36-116">The **DTPAGE** structures contain an array of **DTCTL** structures and a count of the number of **DTCTL** structures in the array.</span></span> <span data-ttu-id="06b36-117">ダイアログボックスに表示するコントロールごとに1つの構造があります。</span><span class="sxs-lookup"><span data-stu-id="06b36-117">There is one structure for every control to display in the dialog box.</span></span> <span data-ttu-id="06b36-118">**dtpage**構造体にも、対応するヘルプファイルおよびダイアログボックスリソースの名前を表す文字列があります。</span><span class="sxs-lookup"><span data-stu-id="06b36-118">**DTPAGE** structures also have a character string that represents the name of a corresponding Help file and dialog box resource.</span></span> 
  
<span data-ttu-id="06b36-119">**dtpage**構造の各**DTCTL**構造体には、コントロールのプロパティを設定するために使用される次のデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="06b36-119">Each **DTCTL** structure in a **DTPAGE** structure contains the following data that is used to set properties for the control:</span></span> 
  
- <span data-ttu-id="06b36-120">**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) を設定するコントロールの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="06b36-120">The control type for setting **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)).</span></span>
    
- <span data-ttu-id="06b36-121">**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) を設定するための制御フラグ。</span><span class="sxs-lookup"><span data-stu-id="06b36-121">Control flags for setting **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).</span></span>
    
- <span data-ttu-id="06b36-122">**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) を設定するための通知データ。</span><span class="sxs-lookup"><span data-stu-id="06b36-122">Notification data for setting **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)).</span></span>
    
- <span data-ttu-id="06b36-123">**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) を設定するためのコントロール構造。</span><span class="sxs-lookup"><span data-stu-id="06b36-123">The control structure for setting **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).</span></span>
    
<span data-ttu-id="06b36-124">**DTCTL**構造体にもリソース識別子が含まれています。また、エディットコントロールおよびコンボボックスコントロールの場合は、文字フィルターを使用します。</span><span class="sxs-lookup"><span data-stu-id="06b36-124">**DTCTL** structures also contain a resource identifier and, for edit and combo box controls, a character filter.</span></span> 
  
<span data-ttu-id="06b36-125">**DTCTL**構造体の control 構造体メンバーは、コントロールの種類に固有のデータを記述します。</span><span class="sxs-lookup"><span data-stu-id="06b36-125">The control structure member of a **DTCTL** structure describes the data that is unique for the type of control.</span></span> <span data-ttu-id="06b36-126">MAPI では、コントロールの種類ごとに異なる構造が定義されています。</span><span class="sxs-lookup"><span data-stu-id="06b36-126">MAPI defines a different structure for each control type.</span></span> <span data-ttu-id="06b36-127">たとえば、編集コントロールのデータは、 **DTBLEDIT**構造体で表されます。リストボックスのデータは、 **dtbllbx**構造体で表されます。</span><span class="sxs-lookup"><span data-stu-id="06b36-127">For example, the data of an edit control is represented by a **DTBLEDIT** structure; the data of a list box is represented by a **DTBLLBX** structure.</span></span> 
  
<span data-ttu-id="06b36-128">次の図は、3種類の表示テーブル構造の関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="06b36-128">The relationship between the three types of display table structures is shown in the following illustration.</span></span> <span data-ttu-id="06b36-129">この表示テーブルで説明されているダイアログボックスには、label および edit コントロールという2つのコントロールがあります。</span><span class="sxs-lookup"><span data-stu-id="06b36-129">The dialog box described by this display table has two controls: a label and an edit control.</span></span> <span data-ttu-id="06b36-130">**dtbllbx**構造体には、ラベルオフセットメンバがあります。これには、ラベルの文字列の開始位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="06b36-130">The **DTBLLBX** structure has a label offset member, as do several of the control structures, that describes where the character string for the label begins.</span></span> <span data-ttu-id="06b36-131">通常、ラベル文字文字列は、構造体のすぐ後のメモリに配置されます。</span><span class="sxs-lookup"><span data-stu-id="06b36-131">Label character strings are typically placed in memory immediately following the structure.</span></span> 
  
<span data-ttu-id="06b36-132">**表示テーブルの構造**</span><span class="sxs-lookup"><span data-stu-id="06b36-132">**Display table structures**</span></span>
  
<span data-ttu-id="06b36-133">![テーブル構造を表示]する(media/dtstruct.gif "テーブル構造を表示")する</span><span class="sxs-lookup"><span data-stu-id="06b36-133">![Display table structures](media/dtstruct.gif "Display table structures")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06b36-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="06b36-134">See also</span></span>

- [<span data-ttu-id="06b36-135">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="06b36-135">Display table implementation</span></span>](display-table-implementation.md)

