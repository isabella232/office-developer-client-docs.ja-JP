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
ms.openlocfilehash: 159e9f1b4cf7beab96a463ff476b4edf577e1371
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926935"
---
# <a name="displayhourglasspointer-macro-action"></a><span data-ttu-id="4e355-102">DisplayHourglassPointer マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="4e355-102">DisplayHourglassPointer macro action</span></span>


<span data-ttu-id="4e355-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4e355-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e355-104">砂時計のマウス ポインターを変更するのには、 **DisplayHourglassPointer**アクションを使用することができます (または選択した別のアイコン)、マクロの実行中にします。</span><span class="sxs-lookup"><span data-stu-id="4e355-104">You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running.</span></span> <span data-ttu-id="4e355-105">このアクションによって、マクロが実行中であることを視覚的に示すことができます。</span><span class="sxs-lookup"><span data-stu-id="4e355-105">This action can provide a visual indication that the macro is running.</span></span> <span data-ttu-id="4e355-106">マクロ アクションまたはマクロ自体の実行に時間がかかる場合に使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="4e355-106">This is especially useful when a macro action or the macro itself takes a long time to run.</span></span>

## <a name="setting"></a><span data-ttu-id="4e355-107">設定値</span><span class="sxs-lookup"><span data-stu-id="4e355-107">Setting</span></span>

<span data-ttu-id="4e355-108">**DisplayHourglassPointer**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="4e355-108">The **DisplayHourglassPointer** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e355-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="4e355-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4e355-110">説明</span><span class="sxs-lookup"><span data-stu-id="4e355-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e355-111"><strong>Hourglass On/表示</strong></span><span class="sxs-lookup"><span data-stu-id="4e355-111"><strong>Hourglass On</strong></span></span></p></td>
<td><p><span data-ttu-id="4e355-p102">[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションの [<strong>表示</strong>] ボックスで、砂時計のアイコンを表示する場合は [<strong>はい</strong>]、通常のマウス ポインターを表示する場合は [<strong>いいえ</strong>] をクリックします。既定値は [<strong>はい</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="4e355-p102">Click <strong>Yes</strong> (display the icon) or <strong>No</strong> (display the normal mouse pointer) in the <strong>Hourglass On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4e355-114">解説</span><span class="sxs-lookup"><span data-stu-id="4e355-114">Remarks</span></span>

<span data-ttu-id="4e355-115">このアクションは、" **Echo/エコー** " アクションでエコーをオフにした場合によく使用します。</span><span class="sxs-lookup"><span data-stu-id="4e355-115">You often use this action if you have turned echo off by using the **Echo** action.</span></span> <span data-ttu-id="4e355-116">エコーがオフの場合、アクセスは、マクロが終了するまで画面の更新を中断します。</span><span class="sxs-lookup"><span data-stu-id="4e355-116">When echo is off, Access suspends screen updates until the macro is finished.</span></span>

<span data-ttu-id="4e355-117">自動的にリセット、**砂時計型インデント マーカーの**引数に [ **No**マクロの実行が完了するとします。</span><span class="sxs-lookup"><span data-stu-id="4e355-117">Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.</span></span>

> [!NOTE]
> - <span data-ttu-id="4e355-p104">Microsoft Windows では、Windows コントロール パネルの [**マウスのプロパティ**] ダイアログ ボックスで [**待ち状態**] に設定されたアイコンが使用されます。すべての Windows オペレーティング システムで、既定の設定は砂時計アイコンです。</span><span class="sxs-lookup"><span data-stu-id="4e355-p104">In Microsoft Windows, this is the icon you set for **Busy** in the **Mouse Properties** dialog box of Windows Control Panel. The default for all Windows operating systems is an animated hourglass icon.</span></span>
> - <span data-ttu-id="4e355-120">別のアイコンを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="4e355-120">You can choose another icon if you want.</span></span>

<span data-ttu-id="4e355-121">Visual Basic for Applications (VBA) モジュールに**DisplayHourglassPointer**アクションを実行するには、 **DoCmd**オブジェクトの**Hourglass**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="4e355-121">To run the **DisplayHourglassPointer** action in a Visual Basic for Applications (VBA) module, use the **Hourglass** method of the **DoCmd** object.</span></span>

