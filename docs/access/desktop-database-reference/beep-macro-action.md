---
title: マクロ アクション (デスクトップ データベース参照のアクセス) の音を鳴らす
TOCTitle: Beep Macro Action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 284be6222d0b81e48a061afd1d87dd32c3985feb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867581"
---
# <a name="beep-macro-action"></a><span data-ttu-id="e469c-102">"Beep/警告音" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="e469c-102">Beep Macro Action</span></span>


<span data-ttu-id="e469c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e469c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e469c-104">コンピューターのスピーカーからビープ音を鳴らす、**ビープ音が**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="e469c-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="e469c-105">設定値</span><span class="sxs-lookup"><span data-stu-id="e469c-105">Setting</span></span>

<span data-ttu-id="e469c-106">**ビープ音を鳴らす**アクション引数はありません。</span><span class="sxs-lookup"><span data-stu-id="e469c-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="e469c-107">解説</span><span class="sxs-lookup"><span data-stu-id="e469c-107">Remarks</span></span>

<span data-ttu-id="e469c-108">次のような場合に、**ビープ音を鳴らす**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="e469c-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="e469c-109">重要な画面変更があったとき。</span><span class="sxs-lookup"><span data-stu-id="e469c-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="e469c-p101">不適切なデータがコントロールに入力されたとき。たとえば、テキスト ボックス コントロールに数値データが入力された場合などです。</span><span class="sxs-lookup"><span data-stu-id="e469c-p101">The wrong kind of data has been entered in a control. For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="e469c-112">マクロが特定のポイントに達したときや、マクロのアクションが完了したとき。</span><span class="sxs-lookup"><span data-stu-id="e469c-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="e469c-113">警告音の周波数と継続時間は、ハードウェアに依存するので、コンピューターの機種によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="e469c-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="e469c-114">Visual Basic for Applications (VBA) モジュールで**ビープ音を鳴らす**アクションを実行するには、 **DoCmd**オブジェクトの**Beep**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e469c-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

