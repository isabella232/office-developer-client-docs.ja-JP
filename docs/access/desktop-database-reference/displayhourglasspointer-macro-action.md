---
title: "\"DisplayHourglassPointer/砂時計ポインターの表示\" マクロ アクション"
TOCTitle: DisplayHourglassPointer Macro Action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4d9f370fdc1ea2100178a489ad1c81225cd05199
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874616"
---
# <a name="displayhourglasspointer-macro-action"></a><span data-ttu-id="96767-102">"DisplayHourglassPointer/砂時計ポインターの表示" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="96767-102">DisplayHourglassPointer Macro Action</span></span>


<span data-ttu-id="96767-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="96767-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="96767-104">砂時計のマウス ポインターを変更するのには、 **DisplayHourglassPointer**アクションを使用することができます (または選択した別のアイコン)、マクロの実行中にします。</span><span class="sxs-lookup"><span data-stu-id="96767-104">You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running.</span></span> <span data-ttu-id="96767-105">このアクションによって、マクロが実行中であることを視覚的に示すことができます。</span><span class="sxs-lookup"><span data-stu-id="96767-105">This action can provide a visual indication that the macro is running.</span></span> <span data-ttu-id="96767-106">マクロ アクションまたはマクロ自体の実行に時間がかかる場合に使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="96767-106">This is especially useful when a macro action or the macro itself takes a long time to run.</span></span>

## <a name="setting"></a><span data-ttu-id="96767-107">設定値</span><span class="sxs-lookup"><span data-stu-id="96767-107">Setting</span></span>

<span data-ttu-id="96767-108">**DisplayHourglassPointer**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="96767-108">The **DisplayHourglassPointer** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96767-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="96767-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="96767-110">説明</span><span class="sxs-lookup"><span data-stu-id="96767-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96767-111"><strong>Hourglass On/表示</strong></span><span class="sxs-lookup"><span data-stu-id="96767-111"><strong>Hourglass On</strong></span></span></p></td>
<td><p><span data-ttu-id="96767-p102">[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションの [<strong>表示</strong>] ボックスで、砂時計のアイコンを表示する場合は [<strong>はい</strong>]、通常のマウス ポインターを表示する場合は [<strong>いいえ</strong>] をクリックします。既定値は [<strong>はい</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="96767-p102">Click <strong>Yes</strong> (display the icon) or <strong>No</strong> (display the normal mouse pointer) in the <strong>Hourglass On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="96767-114">解説</span><span class="sxs-lookup"><span data-stu-id="96767-114">Remarks</span></span>

<span data-ttu-id="96767-115">このアクションは、" **Echo/エコー** " アクションでエコーをオフにした場合によく使用します。</span><span class="sxs-lookup"><span data-stu-id="96767-115">You often use this action if you have turned echo off by using the **Echo** action.</span></span> <span data-ttu-id="96767-116">エコーがオフの場合、アクセスは、マクロが終了するまで画面の更新を中断します。</span><span class="sxs-lookup"><span data-stu-id="96767-116">When echo is off, Access suspends screen updates until the macro is finished.</span></span>

<span data-ttu-id="96767-117">自動的にリセット、**砂時計型インデント マーカーの**引数に [ **No**マクロの実行が完了するとします。</span><span class="sxs-lookup"><span data-stu-id="96767-117">Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.</span></span>

> [!NOTE]
> - <span data-ttu-id="96767-p104">Microsoft Windows では、Windows コントロール パネルの [**マウスのプロパティ**] ダイアログ ボックスで [**待ち状態**] に設定されたアイコンが使用されます。すべての Windows オペレーティング システムで、既定の設定は砂時計アイコンです。</span><span class="sxs-lookup"><span data-stu-id="96767-p104">In Microsoft Windows, this is the icon you set for **Busy** in the **Mouse Properties** dialog box of Windows Control Panel. The default for all Windows operating systems is an animated hourglass icon.</span></span>
> - <span data-ttu-id="96767-120">別のアイコンを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="96767-120">You can choose another icon if you want.</span></span>

<span data-ttu-id="96767-121">Visual Basic for Applications (VBA) モジュールに**DisplayHourglassPointer**アクションを実行するには、 **DoCmd**オブジェクトの**Hourglass**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="96767-121">To run the **DisplayHourglassPointer** action in a Visual Basic for Applications (VBA) module, use the **Hourglass** method of the **DoCmd** object.</span></span>

