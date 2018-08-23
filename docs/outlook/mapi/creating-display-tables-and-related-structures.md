---
title: 表示のテーブルと関連する構造体を作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 177fe21537e921a4b94a34ad531847701b16c344
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799858"
---
# <a name="creating-display-tables-and-related-structures"></a><span data-ttu-id="56916-103">表示のテーブルと関連する構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="56916-103">Creating display tables and related structures</span></span>
  
<span data-ttu-id="56916-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56916-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56916-105">表示テーブルを作成することは、スクリプト言語でプログラムを記述に似ています。</span><span class="sxs-lookup"><span data-stu-id="56916-105">Creating a display table is similar to writing a program with a scripting language.</span></span> <span data-ttu-id="56916-106">[BuildDisplayTable](builddisplaytable.md)を呼び出すか、またはテーブルの列と行を作成するカスタム コードを作成するか、表示テーブルを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="56916-106">You can create a display table either by calling [BuildDisplayTable](builddisplaytable.md) or writing custom code to populate the rows and columns of the table.</span></span> <span data-ttu-id="56916-107">一般に、簡単であるために、 **BuildDisplayTable**テクニックを使用してください。</span><span class="sxs-lookup"><span data-stu-id="56916-107">In general, you should use the **BuildDisplayTable** technique because it is simpler.</span></span> 
  
<span data-ttu-id="56916-108">表示のテーブルを作成するための MAPI メッセージを表示する**BuildDisplayTable**を呼び出すことができます、前に、階層構造を構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="56916-108">Before you can call **BuildDisplayTable** to prompt MAPI to create a display table, there is a hierarchy of structures that you must build.</span></span> <span data-ttu-id="56916-109">[DTPAGE](dtpage.md)、最上位レベルの構造では、1 つのタブ付きプロパティ ページについて説明します。</span><span class="sxs-lookup"><span data-stu-id="56916-109">The top-level structure, [DTPAGE](dtpage.md), describes a single tabbed property page.</span></span> <span data-ttu-id="56916-110">すべて**DTPAGE**には、構造体は、エディット ボックスやオプション ボタンなど、1 つのコントロールを記述する[DTCTL](dtctl.md)構造です。</span><span class="sxs-lookup"><span data-stu-id="56916-110">In every **DTPAGE** structure is a [DTCTL](dtctl.md) structure that describes a single control, such as an edit box or an option button.</span></span> <span data-ttu-id="56916-111">**DTCTL**の各構造体には、コントロールの種類に固有である構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="56916-111">Each **DTCTL** structure contains a structure that is specific to the type of control.</span></span> <span data-ttu-id="56916-112">たとえば、 **DTCTL**構造体は、エディット ボックス コントロールを記述すると、 **DTBLEDIT**構造体が含まれます。</span><span class="sxs-lookup"><span data-stu-id="56916-112">For example, if the **DTCTL** structure describes an edit box control, it will contain a **DTBLEDIT** structure.</span></span> <span data-ttu-id="56916-113">オプション ボタンの**DTCTL**構造体には、 **DTBLRADIOBUTTON**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="56916-113">The **DTCTL** structure for an option button contains a **DTBLRADIOBUTTON** structure.</span></span> 
  
<span data-ttu-id="56916-114">これらの構造体は、直接**BuildDisplayTable**。この関数のコンテキスト外の意味があるありません。</span><span class="sxs-lookup"><span data-stu-id="56916-114">These structures relate directly to **BuildDisplayTable**; they have no meaning outside the context of this function.</span></span> <span data-ttu-id="56916-115">**BuildDisplayTable**を呼び出すと、入力パラメーターとして 1 つまたは複数の**DTPAGE**構造体を渡します。</span><span class="sxs-lookup"><span data-stu-id="56916-115">When you call **BuildDisplayTable**, you pass one or more **DTPAGE** structures as input parameters.</span></span> <span data-ttu-id="56916-116">**DTPAGE**構造体には、 **DTCTL**構造体の配列と、配列内の**DTCTL**構造体の数のカウントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="56916-116">The **DTPAGE** structures contain an array of **DTCTL** structures and a count of the number of **DTCTL** structures in the array.</span></span> <span data-ttu-id="56916-117">ダイアログ ボックスに表示するすべてのコントロールに対して 1 つの構造があります。</span><span class="sxs-lookup"><span data-stu-id="56916-117">There is one structure for every control to display in the dialog box.</span></span> <span data-ttu-id="56916-118">**DTPAGE**構造体は、対応するヘルプ ファイル、ダイアログ ボックス リソースの名前を表す文字列もあります。</span><span class="sxs-lookup"><span data-stu-id="56916-118">**DTPAGE** structures also have a character string that represents the name of a corresponding Help file and dialog box resource.</span></span> 
  
<span data-ttu-id="56916-119">**DTPAGE**構造内の個々 の**DTCTL**構造体には、コントロールのプロパティを設定するために使用される次のデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="56916-119">Each **DTCTL** structure in a **DTPAGE** structure contains the following data that is used to set properties for the control:</span></span> 
  
- <span data-ttu-id="56916-120">**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) を設定するためのコントロールの種類。</span><span class="sxs-lookup"><span data-stu-id="56916-120">The control type for setting **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)).</span></span>
    
- <span data-ttu-id="56916-121">**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) を設定するためのフラグを制御します。</span><span class="sxs-lookup"><span data-stu-id="56916-121">Control flags for setting **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).</span></span>
    
- <span data-ttu-id="56916-122">**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) を設定するためのデータを通知します。</span><span class="sxs-lookup"><span data-stu-id="56916-122">Notification data for setting **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)).</span></span>
    
- <span data-ttu-id="56916-123">**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) を設定するための制御構造です。</span><span class="sxs-lookup"><span data-stu-id="56916-123">The control structure for setting **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).</span></span>
    
<span data-ttu-id="56916-124">**DTCTL**構造体には、リソース識別子も含まれていると、編集し、コンボ ボックス コントロール、文字のフィルターです。</span><span class="sxs-lookup"><span data-stu-id="56916-124">**DTCTL** structures also contain a resource identifier and, for edit and combo box controls, a character filter.</span></span> 
  
<span data-ttu-id="56916-125">**DTCTL**構造体の制御構造体のメンバーでは、コントロールの種類に対して一意であるデータについて説明します。</span><span class="sxs-lookup"><span data-stu-id="56916-125">The control structure member of a **DTCTL** structure describes the data that is unique for the type of control.</span></span> <span data-ttu-id="56916-126">MAPI では、コントロールの種類ごとに別の構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="56916-126">MAPI defines a different structure for each control type.</span></span> <span data-ttu-id="56916-127">などのエディット コントロールのデータは、 **DTBLEDIT**構造体で表されます。リスト ボックスのデータは、 **DTBLLBX**構造体によって表されます。</span><span class="sxs-lookup"><span data-stu-id="56916-127">For example, the data of an edit control is represented by a **DTBLEDIT** structure; the data of a list box is represented by a **DTBLLBX** structure.</span></span> 
  
<span data-ttu-id="56916-128">表示テーブルの構造体の 3 つのタイプ間の関係は次の図に表示されます。</span><span class="sxs-lookup"><span data-stu-id="56916-128">The relationship between the three types of display table structures is shown in the following illustration.</span></span> <span data-ttu-id="56916-129">表示の次の表に記載されているダイアログ ボックスには 2 つのコントロール: エディット コントロールおよびラベルです。</span><span class="sxs-lookup"><span data-stu-id="56916-129">The dialog box described by this display table has two controls: a label and an edit control.</span></span> <span data-ttu-id="56916-130">**DTBLLBX**構造体といくつかの制御構造体は、ラベルの文字の文字列の開始位置を示すラベルのオフセット メンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="56916-130">The **DTBLLBX** structure has a label offset member, as do several of the control structures, that describes where the character string for the label begins.</span></span> <span data-ttu-id="56916-131">ラベルの文字列は通常、メモリの構造体の直後に配置します。</span><span class="sxs-lookup"><span data-stu-id="56916-131">Label character strings are typically placed in memory immediately following the structure.</span></span> 
  
<span data-ttu-id="56916-132">**表示テーブルの構造**</span><span class="sxs-lookup"><span data-stu-id="56916-132">**Display table structures**</span></span>
  
<span data-ttu-id="56916-133">![テーブルの構造を表示](media/dtstruct.gif "テーブルの構造を表示")</span><span class="sxs-lookup"><span data-stu-id="56916-133">![Display table structures](media/dtstruct.gif "Display table structures")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="56916-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="56916-134">See also</span></span>

- [<span data-ttu-id="56916-135">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="56916-135">Display table implementation</span></span>](display-table-implementation.md)

