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
ms.openlocfilehash: 7024734b09544042fa58b8cd95127d8195e5788a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479005"
---
# <a name="beep-macro-action"></a><span data-ttu-id="d8438-102">"Beep/警告音" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="d8438-102">Beep Macro Action</span></span>


<span data-ttu-id="d8438-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8438-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d8438-104">コンピューターのスピーカーからビープ音を鳴らす、**ビープ音が**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d8438-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="d8438-105">設定値</span><span class="sxs-lookup"><span data-stu-id="d8438-105">Setting</span></span>

<span data-ttu-id="d8438-106">**ビープ音を鳴らす**アクション引数はありません。</span><span class="sxs-lookup"><span data-stu-id="d8438-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8438-107">解説</span><span class="sxs-lookup"><span data-stu-id="d8438-107">Remarks</span></span>

<span data-ttu-id="d8438-108">次のような場合に、**ビープ音を鳴らす**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d8438-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="d8438-109">重要な画面変更があったとき。</span><span class="sxs-lookup"><span data-stu-id="d8438-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="d8438-p101">不適切なデータがコントロールに入力されたとき。たとえば、テキスト ボックス コントロールに数値データが入力された場合などです。</span><span class="sxs-lookup"><span data-stu-id="d8438-p101">The wrong kind of data has been entered in a control. For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="d8438-112">マクロが特定のポイントに達したときや、マクロのアクションが完了したとき。</span><span class="sxs-lookup"><span data-stu-id="d8438-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="d8438-113">警告音の周波数と継続時間は、ハードウェアに依存するので、コンピューターの機種によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d8438-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="d8438-114">Visual Basic for Applications (VBA) モジュールで**ビープ音を鳴らす**アクションを実行するには、 **DoCmd**オブジェクトの**Beep**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d8438-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

