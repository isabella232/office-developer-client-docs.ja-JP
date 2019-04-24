---
title: DisplayHourglassPointer マクロ アクション
TOCTitle: DisplayHourglassPointer macro action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a5635b2b97066394b8596dbcdb50c84abf429719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293834"
---
# <a name="displayhourglasspointer-macro-action"></a><span data-ttu-id="85ac9-102">DisplayHourglassPointer マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="85ac9-102">DisplayHourglassPointer macro action</span></span>


<span data-ttu-id="85ac9-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="85ac9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85ac9-p101">You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running. This action can provide a visual indication that the macro is running. This is especially useful when a macro action or the macro itself takes a long time to run.</span><span class="sxs-lookup"><span data-stu-id="85ac9-p101">You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running. This action can provide a visual indication that the macro is running. This is especially useful when a macro action or the macro itself takes a long time to run.</span></span>

## <a name="setting"></a><span data-ttu-id="85ac9-107">Setting</span><span class="sxs-lookup"><span data-stu-id="85ac9-107">Setting</span></span>

<span data-ttu-id="85ac9-108">"DisplayHourglassPointer/砂時計ポインターの表示" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="85ac9-108">The **DisplayHourglassPointer** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85ac9-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="85ac9-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="85ac9-110">説明</span><span class="sxs-lookup"><span data-stu-id="85ac9-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85ac9-111"><strong>Hourglass On/表示</strong></span><span class="sxs-lookup"><span data-stu-id="85ac9-111"><strong>Hourglass On</strong></span></span></p></td>
<td><p><span data-ttu-id="85ac9-p102">[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションの [<strong>表示</strong>] ボックスで、砂時計のアイコンを表示する場合は [<strong>はい</strong>]、通常のマウス ポインターを表示する場合は [<strong>いいえ</strong>] をクリックします。既定値は [<strong>はい</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="85ac9-p102">Click <strong>Yes</strong> (display the icon) or <strong>No</strong> (display the normal mouse pointer) in the <strong>Hourglass On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="85ac9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="85ac9-114">Remarks</span></span>

<span data-ttu-id="85ac9-115">このアクションは、" **Echo/エコー** " アクションでエコーをオフにした場合によく使用します。</span><span class="sxs-lookup"><span data-stu-id="85ac9-115">You often use this action if you have turned echo off by using the **Echo** action.</span></span> <span data-ttu-id="85ac9-116">エコーがオフの場合、マクロが終了するまで、Access は画面の更新を中断します。</span><span class="sxs-lookup"><span data-stu-id="85ac9-116">When echo is off, Access suspends screen updates until the macro is finished.</span></span>

<span data-ttu-id="85ac9-117">Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.</span><span class="sxs-lookup"><span data-stu-id="85ac9-117">Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.</span></span>

> [!NOTE]
> - <span data-ttu-id="85ac9-p104">Microsoft Windows では、Windows コントロール パネルの [**マウスのプロパティ**] ダイアログ ボックスで [**待ち状態**] に設定されたアイコンが使用されます。すべての Windows オペレーティング システムで、既定の設定は砂時計アイコンです。</span><span class="sxs-lookup"><span data-stu-id="85ac9-p104">In Microsoft Windows, this is the icon you set for **Busy** in the **Mouse Properties** dialog box of Windows Control Panel. The default for all Windows operating systems is an animated hourglass icon.</span></span>
> - <span data-ttu-id="85ac9-120">別のアイコンを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="85ac9-120">You can choose another icon if you want.</span></span>

<span data-ttu-id="85ac9-121">Visual Basic for Applications (VBA) モジュールで "DisplayHourglassPointer/砂時計ポインターの表示" アクションを実行するには、DoCmd オブジェクトの Hourglass メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="85ac9-121">To run the **DisplayHourglassPointer** action in a Visual Basic for Applications (VBA) module, use the **Hourglass** method of the **DoCmd** object.</span></span>

